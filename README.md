# qkmao-docs
v1 使用方法可以在 <https://qkmao.cc/dev> 查看  
## 一般使用方法
```haskell
POST https://qkmao.cc/api/v2
```
```json
{
  "link": "https://random.link",
  "slug": "good-stuff-not-drugs"
}
```
RESPONSE:
```json
(200)

{
  "message": "successful",
  "link": "https://qkmao.cc/good-stuff-not-drugs"
}
```
## 隨機短網址
```haskell
POST https://qkmao.cc/api/v2?random
```
```json
{
  "link": "https://long-link.here"
  // no need to use slug because ?random
}
```
