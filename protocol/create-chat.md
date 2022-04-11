# 创建聊天
客户端随机生成[ChatID](../defines.md#ChatID)、ChaCha20的密钥ChatKey和一个ECDSA私钥CharPriKey并获取它的公钥ChatPubKey并生成[聊天邀请包](../struct/chat-invite-decrypted.md#解密后的聊天邀请包结构)

客户端向服务端发送[聊天创建包](../struct/communicate-package#聊天创建包)

服务端回复[基础包](../struct/communicate-package.md#基础包)， 状态码列表如下

| 状态码 | 说明         | 备注 |
| ------ | ------------ | ---- |
| 0x01   | 创建成功     |      |
| 0x02   | 创建失败     |      |
| 0x03   | 请求过于频繁 |      |

如果返回0x01可以继续进行[用户邀请](invite-user.md)