# .github

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
        },
        {
            "id": 14,
            "date": "2024-01-01",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 15,
            "date": "2024-01-09",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 16,
            "date": "2024-01-09",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 17,
            "date": "2024-01-09",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 18,
            "date": "2024-01-09",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 19,
            "date": "2024-01-09",
            "bank": "213",
            "category": "1231",
            "money": "3123123",
            "content": "12312",
            "memo": "123123",
            "ie": "I"
        },
        {
            "id": 58,
            "date": "2024-01-12",
            "bank": "카카오뱅크",
            "category": "식비",
            "money": "123123",
            "content": "content",
            "memo": "memo",
            "ie": "I"
        },
        {
            "id": 21,
            "date": "2024-01-16",
            "bank": "12",
            "category": "3123",
            "money": "123213",
            "content": "42141",
            "memo": "4124",
            "ie": "E"
        }
    ]
}
```

```jsx
{
	message : "에러"
}
```

### 월별 총 비용 계산

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
