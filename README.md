## 简介

​		使用自签名IP搭建tailscale私有 DERP 中继服务器。

## 使用方法

```
docker run --restart always \
  --name derper -p 3477:3477 -p 3478:3478/udp \
  -e DERP_CERT_MODE=manual \
  -e DERP_ADDR=:3477 \
  -d geniotic/ip_derper:latest
```

## 参考链接

> https://icloudnative.io/posts/custom-derp-servers/#%E4%BD%BF%E7%94%A8%E5%9F%9F%E5%90%8D
