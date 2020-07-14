---
title: 마크다운(Markdown) 문법 연습하기
date: 2020-07-14 14:07:22
category: MARKDOWN
draft: false
---

## 들어가기
블로그를 옮긴 후의 첫 포스팅이다. 이제 진짜 마크다운에 익숙해져야 한다! 😉  
마크다운 문법을 검색하다가 아주 좋은 학습 자료가 있길래 실습을 하기로 했다. 

> 이 포스팅은 [TheoryDB님의 블로그](https://theorydb.github.io/envops/2019/05/22/envops-blog-how-to-use-md/)글을 참고하여 만들어졌습니다.

- 목차
	- [들어가기](#들어가기) 
    - [문법실습](#문법-실습) 
    - [마무리](#마무리) 

## 문법 실습
+ __[1단계] `헤더(Header)` : 제목, 문단별 제목을 쓰고 싶을 때__
```markdown
# 제목 1단계
## 제목 2단계
### 제목 3단계
#### 제목 4단계
##### 제목 5단계
###### 제목 6단계
```

# 제목 1단계
## 제목 2단계
### 제목 3단계
#### 제목 4단계
##### 제목 5단계
###### 제목 6단계
---

+ __[2단계] `수평선` : 내용을 명시적으로 구분하고 싶을 때__
```markdown
---
```

---
---

+ __[3단계] `엔터키(개행)` : 라인을 바꾸고 싶을 때__
```markdown
띄어쓰기 2번을 입력하면 줄이 바뀐다.
```
  
---

+ __[4단계] `목록` : 요소를 나열할 때__
```markdown
1. 하나
2. 둘
3. 셋

+ 텔레토비
    - 뚜비
        * 나나
            + 뽀
```

1. 하나
2. 둘
3. 셋

+ 텔레토비
    - 뚜비
        * 나나
            + 뽀

---

+ __[5단계] `강조` : 단어를 눈에 띄게__
```markdown
__볼드__
_이탤릭체_
~~취소선~~
<u>밑줄</u>
__볼드로 진하게 만들다가 *이탤릭으로 기울이고* 다시 볼드로__
```

__볼드__  
_이탤릭체_  
~~취소선~~  
<u>밑줄</u>  
__볼드로 진하게 만들다가 *이탤릭으로 기울이고* 다시 볼드로__

---

+ __[6단계] `인용구` : 인용 또는 분위기 전환__
```markdown
> 안녕하세요
>> 감사해요
>>> 잘있어요
```

> 안녕하세요
>> 감사해요
>>> 잘있어요

---

+ __[7단계] `링크` : 다른 페이지로 이동할 때__
```markdown
유형1('설명어'를 클릭하면 URL로 이동) : [내 블로그](https://kamyu.netlify.app "안녕")
유형2(URL로 이동) : <https://kamyu.netlify.app>
유형3(동일 파일 내 문단 이동) : [문단으로 이동](#들어가기)
```

유형1('설명어'를 클릭하면 URL로 이동) : [내 블로그](https://kamyu.netlify.app "안녕")  
유형2(URL로 이동) : <https://kamyu.netlify.app>  
유형3(동일 파일 내 문단 이동) : [문단으로 이동](#들어가기)

> 유형 3 사용하는 방법 : 
> 1. 제목(header)에서 특수문자 제거  
> 2. 스페이스를 -로 변경  
> 3. 대문자를 소문자로 변경  
> 4. 맨 앞에 # 추가  
> 예시) "@Markdown 문법 연습" -> "#markdown-문법-연습"

---

+ __[8단계] `이미지` : 이미지 삽입__
```markdown
유형1(이미지 삽입) :
![이미지](../images/image.png "사진입니다")  

유형2(HTML 태그) :
<img src="../images/image.png" width="300" height="200">  

유형3(이미지 링크) :
[![이미지](../images/image.png)](https://kamyu.netlify.app)
```

유형1(이미지 삽입) :
![이미지](../images/image.png "사진입니다")  

유형2(HTML 태그) :
<img src="../images/image.png" width="300" height="150">  

유형3(이미지 링크) :
[![이미지](../images/image.png)](https://kamyu.netlify.app)

---

+ __[9단계] `표` : 표 그리기__
```markdown
| |Score|Grade|
|:---|---:|:---:|
|Jane|90|A|
|Austin|50|B|
```
||Score|Grade|
|:---|---:|:---:|
|Jane|90|A|
|Austin|50|B|

> 내용 정렬하는 방법 :
> 콜론(:) 기호를 구분선(---) 왼쪽, 오른쪽, 양쪽에 배치

---

+ __[10단계]  `수식` : 수학에 사용__
```markdown
$$f(x)= if x < x_{min} : (x/x_{min})^a$$  
$$otherwise : 0$$  
$$P(w)=U(x/2)(7/5)/Z$$  
$$p_{\theta}(x) = \int p_{\theta}(2z)p_{\theta}(y\mid k)dz$$  
$$x = argmax_k((x_t-x_u+x_v)^T*x_m)/(||x_b-x_k+x_l||)$$  
```

$$f(x)= if x < x_{min} : (x/x_{min})^a$$  
$$otherwise : 0$$  
$$P(w)=U(x/2)(7/5)/Z$$  
$$p_{\theta}(x) = \int p_{\theta}(2z)p_{\theta}(y\mid k)dz$$  
$$x = argmax_k((x_t-x_u+x_v)^T*x_m)/(||x_b-x_k+x_l||)$$  

> * 수식 표현에 제한이 있는 경우, `MathJax` JS를 사용한다.
>   ``` html
>   <script type="text/javascript" 
>   src="https://cdn.mathjax.org/mathjax/latest/MathJax.js?> config=TeX-AMS_HTML">
>   </script>
>   ```
> * 표현형식은 [Latex](https://en.wikibooks.org/wiki/LaTeX/Mathematics) 표기법과 동일하다.

---

+ __[11단계] `코드 블록` : 소스코드나 블록처리에 사용__
~~~
```python
py_vector = one_hot_encoding("파이",word2index)
py_vector.dot(torch_vector)
>>> 0.0
```
~~~

```python
py_vector = one_hot_encoding("파이",word2index)
py_vector.dot(torch_vector)
>>> 0.0
```  

> * `뒤에 python이라고 쓰면 python 스타일에 맞게 구문이 강조된다.  
> * 예시) bash, cpp, markdown, html, http, r, json, ruby, xml, sql ...

---

+ __[12단계] `UML 다이어그램` : 순서도, 흐름도를 표현__

> * [Flow charts](http://flowchart.js.org/)
> * [Sequence diagrams](https://bramp.github.io/js-sequence-diagrams/)


---

## 마무리
이 밖에도 특수문자를 표현하려면 \\ 기호를 붙이는 것 등의 팁이 있었다.  
제대로 마크다운 공부를 한 것은 처음이다.  
여러 차례 글을 작성하다 보면 작성 속도가 빨라질 수 있을 것 같다. 👍