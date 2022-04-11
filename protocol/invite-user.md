# 用户邀请
客户端向用户请求要邀请的用户名列表并计算对应的[唯一用户id](../defines.md#唯一用户id)列表

客户端向服务端按照[唯一用户id](../defines.md#唯一用户id)列表[获取对应的用户公钥](get-user-PubKey.md)并把所有ECDSA公钥转换为ECIES公钥

客户端把[聊天邀请包](../struct/chat-invite-decrypted.md#解密后的聊天邀请包结构)(内容在[创建聊天](create-chat.md)中生成)用每个要邀请的人的ECIES公钥加密，后称EncryptedInviteData

客户端向服务端发送

TBC