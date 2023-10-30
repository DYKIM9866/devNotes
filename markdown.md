마크다운 문법
=================
내가 사용하는 문법 위주로 문법으로 부족하다면 html문법 사용

## 1. 헤더
* 큰 제목
```
This is an H1
==============
```
* 작은제목
```
This is an H2
==============
```
* #으로 표현
```
# This is H1
## This is H2
### This is H3
#### This is H4
##### This is H5
###### This is H6
```
# This is H1
## This is H2
### This is H3
#### This is H4
##### This is H5
###### This is H6

## 2. 목록
* 순서있는 목록<br>
번호가 순서가 틀려도 순서대로 정렬됨
```
1. 첫번째
3. 두번째
2. 세번째
```
1. 첫번째
3. 두번째
2. 세번째

* 순서없는 목록<br>
혼합해서도 사용가능
```
* 하나
    * 둘
        * 셋
+ 하나
    + 둘
        + 셋
- 하나
    - 둘
        - 셋
* 하나
    - 둘
        + 셋        
```
* 하나
    * 둘
        * 셋
+ 하나
    + 둘
        + 셋
- 하나
    - 둘
        - 셋
* 하나
    - 둘
        + 셋

## 3. 코드
들여쓰기를 해서 할 수도 있는데 나는 명확한 구분이 되는게 좋아서 코드블럭을 사용
(```) 를 사용해서 쓴다. 또 기능이 있으면 뒤에 언어를 붙혀서도 사용 가능
```
    ```java
        class Car{
            public  Car(){

            }
        }
    ```
```

## 4. 수평선
```
* * *
***
*****
- - -
-------------------
```
* * *
***
*****
- - -
-------------------

## 5. 링크
```
[네이버](www.naver.com)
[구글](www.google.com)
```
[네이버](https://www.naver.com/)<br>
[구글](https://google.com)

## 6. 강조
```
*single asterisks*
_single underscores_
**double asterisks**
__double underscores__
~~cancelline~~
```
* *single asterisks*
* _single underscores_
* **double asterisks**
* __double underscores__
* ~~cancelline~~

## 7. 줄바꿈
```
이렇게 하거나 띄어쓰기 세번    
아니면 이렇게<br>하거나
```
이렇게 하거나 띄어쓰기 세번    
아니면 이렇게<br>하거나
