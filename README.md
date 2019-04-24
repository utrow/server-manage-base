# サーバを管理するための
(VPC群を管理するようなものではない)

## Packaged
- リバースプロキシ
- LetsEncryptツール
- netdata

## Installation
docker network create -d bridge public-proxy-nginx

## Settings

### リバースプロキシの設定（app側）
仮想ホスト名の設定
```
environment:
    VIRTUAL_HOST: example.com
    VIRTUAL_PORT: 8080　# 任意
```

### LetsEncryptの設定（app側）
仮想ホスト名の設定
```
environment:
    LETSENCRYPT_HOST: example.com
    LETSENCRYPT_EMAIL: ---
```

