# 음식점 추천 서버

💡 금요일마다 친구들과 밥 먹을때 음식점 고르기 귀찮아서 만들기로함

## API Reference

### `GET` /search?keyword=<키워드 들...>

**request**  

|Name|Type|Description|
|----|----|-----------|
|keyword|array|키워드 리스트 (required)|


**response**
```json
{
  "places": [
    {
      "name" : "String",
      "image" : "String"
    }
  ]
}
```

### `POST` /place

**body**

```json
{
  "city": "String",
  "gu": "String",
  "dong": "String",
  "name": "String"
}
```

**request**

|Name|Type|Description|
|----|----|-----------|
|city|String| 시 이름 ex) 대구.. (required) |
|gu|String|구 이름 ex) 달서구.. (required)|
|dong|String|동 이름 ex) 월성동.. (required)|
|name|String|가게 이름 (required)|

**response**
```json
{
  "message" : "ok"
}
```

### `POST` /evaluation

**body**

```json
{
  "status": "Integer"
}
```

**request**

|Name|Type|Description|
|----|----|-----------|
|status|Integer| 좋았다면 1, 별로였다면 0 (required) |

**response**
```json
{
  "message" : "ok"
}
```