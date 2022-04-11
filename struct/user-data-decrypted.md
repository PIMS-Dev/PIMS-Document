# 用户数据结构
用户数据将使用json储存

根对象
| 字段名     | 内容        | 备注       |
| ---------- | ----------- | ---------- |
| UserName   | 明文用户名  |            |
| PrivateKey | ECDSA的私钥 | base64形式 |
| ChatList   | 聊天的数组  |            |

ChatList数组的内容
| 第0项    | ...      |
| -------- | -------- |
| 聊天对象 | 聊天对象 |

聊天对象结构
| 字段名   | 内容       | 备注       |
| -------- | ---------- | ---------- |
| ChatName | 聊天的名称 |            |
| ChatID   | 聊天的ID   | UUID       |
| ChatKey  | ChatKey    | base64形式 |
| ChatNonce| ChatNonce  | base64形式 |