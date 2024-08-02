# 👋 가계부 웹 과제

# 사용 기술
- mySQL
- express
- webpack
- javascript


# router

`/` : 홈

`/report` : 달 분석


# API

### 수입

### request (/, post) body

```jsx
{
    "date":"2024-01-12",
     "bank":"카카오뱅크",
    "category":"식비",
    "money":123123,
    "content":"content",
    "memo":"memo",
    "ie":"I"
}
```

### 지출

### request (/, post) body

```jsx
{
    "date":"2024-01-12",
     "bank":"카카오뱅크",
    "category":"식비",
    "money":123123,
    "content":"content",
    "memo":"memo",
    "ie":"E"
}
```

### response

```jsx
{
	message : "success"
}
```

```jsx
{
	message : "카테고리가 해당 분류가 아닙니다"
}
```

### 달 별  수입 지출 조회

### request (domain?date=2024-04 & ie=e , get)

- date

### response

```jsx
{
    "message": "Success",
    "data": [
        {
            "id": 10,
            "date": "2024-01-01",
            "bank": "1223",
            "category": "12313",
            "money": "12312321",
            "content": "312321312",
            "memo": "312321",
            "ie": "I"
        }
    ]
}
```

```jsx
{
	message : "에러"
}
```

### 월별 총 비용 계산 보고서

report

### request (domain/report?date=?, get)

```jsx
{
    "message": "Success",
    "data": {
        "date": "2024-01",
        "total": {
            "total_income": "31174182",
            "total_expense": "640347",
            "total_profit": "30533835"
        },
        "items": [
            {
                "category": "3123",
                "total_expense": "123213"
            },
            {
                "category": "3213",
                "total_expense": "24642"
            },
            {
                "category": "식비",
                "total_expense": "492492"
            }
        ]
    }
}
```
