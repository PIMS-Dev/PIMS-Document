# PIMS-Document
PIMS的技术文档

<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/"><img alt="知识共享许可协议" style="border-width:0" src="https://i.creativecommons.org/l/by-nc-sa/4.0/88x31.png" /></a><br />本作品采用<a rel="license" href="http://creativecommons.org/licenses/by-nc-sa/4.0/">知识共享署名-非商业性使用-相同方式共享 4.0 国际许可协议</a>进行许可。

# 什么是PIMS
PIMS aka Prometheus Instant Messenger System

它是一个完全加密且开源的即时聊天系统，这个项目通讯协议的文档

PIMS旨在最恶劣的安全条件下也可以保证通讯的安全性和即时性——这意味着它保证信息即使被拦截甚至服务器被完全攻陷也可以保证聊天记录及用户数据的安全。

# 文档结构
文档大体会分为以下几个部分

- [技术概览](overview.md)
- [细节定义](defines.md)
- [通讯协议](protocol)
    - [ ] [注册](protocol/register.md)
    - [x] [获取用户数据](protocol/get-user-data.md)
    - [x] [获取用户公钥](protocol/get-user-PubKey.md)
    - [x] [创建聊天](protocol/create-chat.md)
    - [ ] [用户邀请](protocol/invite-user.md)
    - [ ] 聊天信息的发送和接收
- [数据结构](struct)
    - [ ] [通讯包结构](struct/communicate-package.md)
    - [ ] [解密后的用户数据](struct/user-data-decrypted.md)
    - [ ] [解密后的聊天邀请包结构](struct/chat-invite-decrypted.md)

注意：请在看其他文档之前浏览一遍技术概览，不然很可能会对细节疑惑