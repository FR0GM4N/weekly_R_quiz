Q) 데이터 분석을 위한 전처리를 해주세요!   

고객의 web log가 다음과 같이 기록되어 있습니다  

```{r, message=FALSE, warning=FALSE, include=FALSE}
id <- rep(LETTERS[1:5], c(7,3,7,7,5))

page <- c(
  'main','event','bestseller','purchase','main','search','purchase',
  'main','search','purchase',
  'mypage','cart','purchase','main','free_book','purchase','mypage',
  'main','recommendation','purchase','mypage','wishlist','event','search',
  'event','purchase','mypage','cart','purchase')
  
raw.data <- 
  data.frame(id, page, stringsAsFactors=FALSE)
```

1. 구매가 이루어졌음을 뜻하는 purchase를 기준으로 끊어 chain.id를 부여한 뒤   
2. 다음과 같은 chain column 형태로 묶어주세요~ (id: character, chain.id: numeric, page: List[character])  

![target!](purchase_chain_result.PNG)
