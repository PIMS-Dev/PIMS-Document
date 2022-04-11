# 解密后的聊天邀请包结构
聊天邀请包将使用json传输

根对象
| 字段名     | 内容               | 备注       |
| ---------- | ------------------ | ---------- |
| ChatID     | 唯一的聊天ID       | base64形式 |
| ChatKey    | 聊天的ChaCha20密钥 | base64形式 |
| ChatPriKey | 聊天的ECDSA私钥    | base64形式 |