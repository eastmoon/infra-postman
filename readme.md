# Postman

Postman 是一套用於測試 API 運作狀況與回應的測試服務工具，最早是 Chrome 的服務，現為可獨立安裝的應用程式；Postman 可經使用者介面，設計並規劃 API 測試規則與腳本，在匯出腳本後，則可透過 Newman CLI 來測試並套用 Reporter 工具來匯出客自化的報告。

## 指令

本專案使用 docker-compose 啟用專案，並透過 .env 檔案做為參數匯入 YML 檔案。

+ 啟動虛擬環境
```
dockerw start
```

+ 關閉虛擬環境
```
dockerw down
```

## 設定

Newman 是 Postman 的 CLI 工具，其官方 Docker 基於 Node.js 建置，對此相關設定與操作參考如下：

### Reporter 安裝

Newman 本身為 Node.js 套件，其相關 Reporter 工具則需在 Dockerfile 中設定。

### HTML Reporter 設定

newman-reporter-html 是 Node.js 套件，依據官方文件說明，使用此套件後，可額外使用兩項參數

+ ```reporter-html-export```：報告匯出的路徑
+ ```reporter-html-template```：報告模板 ( hbs )，匯出報告會依據此模板輸出

## 參考

+ CURL
  - [How do I measure request and response times at once using cURL?](https://stackoverflow.com/questions/18215389)
+ Postman
  - [Documenting your API](https://learning.postman.com/docs/publishing-your-api/documenting-your-api/)
    + [Automate Your API Tests with Postman](https://www.postman.com/use-cases/api-testing-automation/)
    + [newman 一個讓 postman api testing 自動化的好幫手](https://medium.com/cubemail88/8e12a6956a25)
  - [postman/newman with Docker](https://hub.docker.com/r/postman/newman/)
    + [DannyDainton/postman-docker](https://github.com/DannyDainton/postman-docker)
    + [newman-reporter-html with NPM](https://www.npmjs.com/package/newman-reporter-html)
