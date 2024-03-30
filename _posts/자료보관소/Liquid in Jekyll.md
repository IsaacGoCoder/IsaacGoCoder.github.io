

link: https://jekyllrb.com/docs/liquid/
link2: https://shopify.github.io/liquid/basics/introduction/


## 개요
Liquid는 정적사이트를 위한 템플릿 언어이며, Jekyll은 Liquid를 사용한 템플릿을 이용해서 각 페이지들을 렌더링 함

## Liquid 기본
### 화면에 표시 될 내용
`{{` `}}`를 사용

### 화면에 표시되지 않는 내용
`{%` `%}`를 사용해서 조건문, 반복문 등의 문법을 사용할 수 있음

### 논리연산자
#### 종류
- `==`, `!=`, `>`, `>=`, `<=`, `<`, `or`, `and`, `contains`
	- `contains` : 서브스트링 존재 여부
		- 예) `{% if my_string contains "abc" %}`
	- not은 없으며, 별개의 `{% unless %}`구문을 사용

#### 다중 논리연산
- `and`나 `or`를 사용할 수 있지만, 괄호`(` `)`를 통한 중첩은 불가능하고, 맨 마지막 부터 순서대로 `bool`연산함
	- 예) `{% if true and false and true or false %}`
		- true and false and <font color="#ff0000">true or false</font>
		- true and <font color="#ff0000">false and true</font>
		- <font color="#ff0000">true and false</font>
		- false

### 자료형
#### 초기화
- `assign`이나 `capture`로 변수를 초기화 할 수 있음
####  문자열
- 작은따옴표(`'`)나 큰따옴표(`"`)로 감싸서 표현
- 예)
	- `{% assign my_string = "Jekyll" %}`
	- `{% assign my_string = 'Liquid' %}`

#### 숫자
- 정수와 실수의 구분이 없음
- 예)
	- `{% assign my_num = 9 %}`
	- `{% assign my_num = 9.22 %}`


### 불
- `true`, `false`
- 실제 값이 `true`가 아니어도, 그 값이 `nil`이 아닌이상 모두 `true`로 취급하며, `nil`은 `false`로 취급함
	- 예) `user`에 값이 있을 경우 `if`문 내부문장을 렌더링 함
	```Liquid
	{% if user %}
	  Hello {{ user.name }}!
	{% endif %}
	```

#### 배열
- `Liquid`내부에서 초기화 불가
	- 대신 `split`필터로 문자열을 쪼개서 배열로 생성할 수는 있음
		- 예) 과일명 배열 생성
		```liquid
		{% assign fruit_array = "apple,banana,cherry" | split "," %}
		```
		- 예) 빈 배열 생성
		```liquid
		{% assign empty_array = "" | split "" %}
		```


## Jekyll [전역변수](https://jekyllrb.com/docs/variables/)
- `_config.yml`파일에 선언한 변수를 `site.변수명`으로 사용할 수 있음
	- 예) `_config.yml`파일에 `my_test : "my test!!"`를 추가 후 `{{my_test}}`와 같이 사용 가능


