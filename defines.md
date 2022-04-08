# 细节定义
## 各种盐
saltPassword为长度为32的随机byte
saltUsername为字符串"PIMS-USER-NAME-SALT"

## 唯一用户id
用户名+[saltUsername](defines.md#各种盐)进行SHA3-256(统称UsernameHash)成为唯一用户id

## 密码Hash和用户数据ChaCha20密钥
用户密码+[saltPassword](defines.md#各种盐)进行SHA3-256(后称PasswordHash)作为ChaCha20的密钥