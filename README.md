# qkmao – API Docs
以下為 Qkmao 的 API 文檔。

## 一般
一般使用方法。

```http
POST https://qkmao.cc/api/v2
```
```json
{
  "link": "https://random.link",
  "slug": "good-stuff-not-drugs"
}
```

**回應 <kbd>✅ 200</kbd>：**
```json

{
  "message": "successful",
  "link": "https://qkmao.cc/good-stuff-not-drugs"
}
```

<br />

## 隨機短網址
提供一個連結，並自動產生隨機網址。
```haskell
POST https://qkmao.cc/api/v2
```
```json
{
  "link": "https://long-link.here",
  "random": true
}
```

**回應 <kbd>✅ 200</kbd>：**
```json

{
  "message": "successful",
  "link": "https://qkmao.cc/xxx"
}
```

<br />

## 獲取原網址
提供 "slug" 即可獲取原完整網址。由於此使用的是 `GET` 方式，因此使用 `slug` "URL Parameter"。以下為獲取 `hello` (slug) 的網址。
```http
GET https://qkmao.cc/api/v2/get?slug=hello
```

**回應 <kbd>✅ 200</kbd>：**
```json

{
  "message": "successful",
  "link": "https://maoyue.lol"
}
```
