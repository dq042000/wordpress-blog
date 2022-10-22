## 腳本安裝

### 第一次安裝使用以下指令

```bash
sh setup.sh
```

### 如果已經安裝過，且 DB 都已經有裝好了，單純要啟動容器及服務，使用以下指令

```bash
sh setup.sh -nodb
```

## 手動安裝
## 設定 hosts

  - 打開 Terminal
```
  sudo vi /etc/hosts
```

  - 增加

```
  127.0.0.1		wordpress.test
```

  - 按下 `Esc` 鍵後，儲存後離開
```
  按下 鍵盤 `Esc` 鍵
  :wq
```

## 切換開發環境分支

  - master
  - production : 正式環境
  - develop : 開發環境
```
  git checkout develop
```

## db 設定
```
mkdir DB
```

## docker 設定檔

```
cp docker-compose-sample.yml docker-compose.yml
cp env-sample .env
cp ./web/.env.example ./web/.env
```

## 啟動 docker

```
docker-compose up -d --build
```

## 開啟瀏覽器

    網站
    http://wordpress.test:9810

    phpMyAdmin
    http://wordpress.test:9811

