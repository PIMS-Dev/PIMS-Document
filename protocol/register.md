# 协议握手
客户端向服务端发起一个连接，发送[基础包](../struct/communicate-package.md#基础包)，状态码为0x01

服务端回复[基础包](../struct/communicate-package.md#基础包)， 状态码列表如下

| 状态码 | 说明                                                       |
| ------ | ---------------------------------------------------------- |
| 0x01   | 可以进一步进行用户创建                                     |
| 0x02   | 服务器允许用户创建，但是必须有已有用户的私钥验证(邀请注册) |
| 0x03   | 服务器允许用户创建，但是必须在后端手动操作                 |
| 0x04   | 服务器禁止用户创建                                         |


如果状态码为0x01或0x02可以进行下一步操作

# 开始用户创建
## 服务端返回状态码为0x01
客户端生成一个ECDSA私钥PriKey并获取对应的公钥PubKey，生成[saltPassword](defines.md#各种盐)

客户端向用户获取用户名和用户密码， 计算[唯一用户id](../defines.md#唯一用户id)和[密码Hash和用户数据ChaCha20密钥](../defines.md#密码hash用户数据和ChaCha20密钥)

客户端创建初始的[用户数据](../struct/user-data-decrypted.md#用户数据结构)

随机生成ChaCha20的Nonce，用ChaCha20加密用户数据(后称EncryptedUserData)

客户端向服务端发送[基本注册请求包](../struct/communicate-package.md#基本注册请求包)

服务端回复[基础包](../struct/communicate-package.md#基础包)， 状态码列表如下

| 状态码 | 说明         | 备注 |
| ------ | ------------ | ---- |
| 0x01   | 注册成功     |      |
| 0x02   | 注册失败     |      |
| 0x03   | 请求过于频繁 |      |
 
 ## 服务端返回状态码为0x02
 TBC