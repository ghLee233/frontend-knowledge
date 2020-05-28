# 对称加密和非对称加密和证书

1. 三次握手
2. 客户端发送:对称加密套件列表+加密套件列表+client-random
3. 服务端接受请求，返回非对称加密套件+加密套件+server-random+证书
4. 浏览器验证数字证书，生成随机数（pre-master），公钥加密pre-master，发送请求
5. 服务器私钥解密得到 pre-master
6. 客户端有 client-random + server-random + pre-master，生成 master-secret
7. 服务端有 client-random + server-random + pre-master，生成 master-secret
8. 客户端和服务端通过master-secret对称加密通信



# 总结

- 客户端和服务端需要三个随机数生成对称加密的秘钥，然后才开始加密通信
- client-random 和 server-random 各自生成通过请求传递
- pre-master通过加密算法产生，通过非对称加密的公钥加密后传递