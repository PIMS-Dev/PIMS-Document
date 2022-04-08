# 获取用户数据
客户端向用户获取用户名和密码，计算[唯一用户id](../defines.md#唯一用户id)和[密码Hash和用户数据ChaCha20密钥](../defines.md#密码hash用户数据和chacha20密钥)

客户端向服务端发起一个连接，发送[用户数据请求包](../struct/get-user-data.md#用户数据请求包)，服务端返回[用户数据下发包](../struct/get-user-data.md#用户数据下发包)

解密获取到的EncryptedUserData，得到用户数据