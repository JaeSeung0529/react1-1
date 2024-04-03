# 정재승 202230233  
<br>

## 2024-04-03 React 5주차 강의 내용
<br>

## chapter 5.컴포넌트와 Props
<br>

### 5.1 컴포넌트에 대해 알아보기 
<br>

* #### 리엑트는 컴포넌트 기반의 구조
* #### 컴포넌트 구조는 작은 컴포넌트가 모여 큰 컴포넌트를 구성, 이런 컴포넌트들이 모여 전체 페이지를 구성한다는 것을 의미
* #### 입력은 Props가 담당하고 출력은 리엑트 엘리먼트의 형태로 출력
* #### 엘리먼트를 필요한 만큼 만들어 사용한다는 면에서는 객체 지향과 개념이 비슷함
<br>

### 5.2 Props에 대해 알아보기
<br>

1. ### Props의 개념 
* #### props는 prop(property: 속성, 특성)의 준말
* #### 이 props가 바로 컴포넌트의 속성이다.
* #### 컴포넌트에 어떤 속성, props를 넣느냐에 따라 속성이 다른 엘리먼트가 출력된다.
* #### props는 컴포넌트에 전달 할 다양한 정보를 담고 있는 자바스크립트 객체이다.
![Alt text](image-1.png)
<br>

2. ### Props의 특징
* #### 읽기 전용. 변경할 수 없다.
* #### 속성이 다른 엘리먼트를 생성하려면 새로운 props를 컴포넌트에 전달하면 된다.
<br>

### Pure 함수 vs. Impure 함수
* #### Pure함수는 인수로 받은 정보가 함수 내부에서도 변하지 않는 함수
* #### Impure함수는 인수로 받은 정보가 함수 내부에서 변하는 함수
![Alt text](image-2.png)
<br>

3. ### Props 사용법
* #### JSX에서는 key-value쌍으로 props를 구성
![Alt text](image-3.png)
<br>

#### 위의 코드는
> 1. #### App 컴포넌트에서 props를 인자로 받아,
> 2. #### 내부의 Profile 컴포넌트로 전달해서 name, introduction, viewCount에 각각 속성을 할다하는,
> 3. #### 이때 전달되는 Props는 다음과 같은 자바스크립트 객체이다.
![Alt text](image-4.png)
<br>

### 5.3 컴포넌트 만들기
<br>

### 5.4 컴포넌트 합성
<br>

### 5.5 컴포넌트 추출
<br>

### 5.6 댓글 컴포넌트 만들기
<br>

## 2024-03-27 React 4주차 강의 내용
<br>

## chapter 3. JSX 소개
<br>

### 3.1 JSX(JavaScript XML)란?
----
* #### javascript에 XML을 추가한 확장 문법.
<br>

### 3.2 JSX의 역할
----
<br>

* #### JSX느 내부적으로 XML/HTML 코드를 자바스크립트로 변환.
* #### REACTrk createElement함수를 사용하여 자동으로 자바스크립트로 변환.
* #### 만일 JS작업할 경우 직접 createElement함수를 사용해야 합니다.
* #### JSX는 가독성을 높여 주는 역할
<br>

### 3.3 JSX의 장점
----
<br>

### 3.4 JSX 사용법
----
<br>

* #### 모든 자바스크립트 문법을 지원
* #### 자바스크립트 문법에 XML과 HTML을 섞어서 사용
* #### 만일 HTML이나 xml에 자바스크립트 코드를 사용하고 싶으면 {}괄호를 사용합니다.
<br>
    
    const element = <h1>안녕,[name]</h1>

<br>

### 3.5 JSX 실습
----
<br>
Book.jsx 

    import React from "react";

    export default function Book(props){
        return(
            <div>
                <h1>{`이 책의 이름은 ${props.name}입니다.`}</h1>
                <h2>{`이 책은 총 ${props.numOfPage}페이지로 미뤄져 있습니다.`}</h2>
            </div>
        );
    }
<br>
Library.jsx 

    import React from "react";
    import Book  from "./Book";

    export default function Library(props){
        return(
            <div>
            <Book name="처음 만난 파이썬" numOfPage={300}/>
            <Book name="처음 만난 AWS" numOfPage={400}/>
            <Book name="처음 만난 리액트" numOfPage={500}/>
            </div>
        )
    }
<br>

![index.js수정](Library.jsx입력후_index.js.수정.png)
<br>

### jsx 사용하지 않았을 때 Book 컴포넌트
![Book](Book원래_컴포넌트(jsx사용안함).png)

#### "import Library from `./chapter03/Library`;" 입력후
#### 기존에 있던 App 을 Library 로 수정
<br>

![Libray.jsx](Library_결과.png)
<br>

## Chapter 04.엘리먼트

<br>

### 4.1 엘리먼트에 대해 알아보기
----

### 1.엘리먼트의 정의
* #### 엘리먼트는 리액트 앱을 구성하는 요소를 의미
* #### 공식페이지에는 "엘리먼트는 리액트 앱의 가장 작은 빌딩 블록들"이라고 설명하고 있다.
* #### 웹사이트의 경우는 DOM 엘리먼트이며 HTML요소를 의미

### 리액트 엘리먼트와 DOM엘리먼트의 차이
* #### 리액트 엘리먼트는 Virtual DOM의 형태를 취함
* #### DOM 엘리먼트는 페이지의 모든 정보를 갖고 있어 무겁다.
* #### 리액트 엘리먼트는 변화한 부분만 갖고 있어 가볍다.
<br>

![DOM,VirtualDOM](DOMvsVirtualDOM.png)
<br>
<br>

<!-- ### 2.엘리먼트의 생김새 
* #### 리액트 엘리먼트는 자바스크립트 객체의 형태로 존재 -->
### 3.엘리먼트의 특징
* #### 불변성 - 한 번 생성된 엘리먼트의 children이나 속성(attributes)을 바꿀수 없습니다.

#### 내용이 바뀐다면?
* #### 컴포넌트를 통해 새로운 엘리먼트를 생성하면 된다.
* #### 그 다음 이전 엘리먼트와 교체를 하는 방법으로 내용을 바꾸는 것
* #### 이렇게 교체하는 작업을 하기위해 Virtual DOM을 사용한다.
<br>

### 4.2 엘리먼트 렌더링하기
----
<br>

#### Root DOM node 
#### id값이 root인 div태그로 단순하지만 리액트에 필수로 들어가는 중요한 코드다.
#### 이 div 태그 안에 리액트 엘리먼트가 렌더링 되며, 이것을 Root DOM node라고 한다.

    <div id="root"></div>

#### 엘리먼트를 렌더링 하기 위해서는 다음과 같은 코드가 필요하다.

    const element = <h1>안녕, 리엑트!<h1>;
    ReactDOM.render(element,document.getElementById('root'));

#### 이때 render() 함수를 사용하게 된다.
#### 이 함수의 첫 번째 파라메타 출력할 리액트 엘리먼트이고, 두번째 파라메터는 출력할 타겟을 나타낸다.
#### 즉 리엑트 렌더링의 과정은 Virtual DOM에서 실제 DOM으로 이동하는 과정이라고 할 수 있다.
<br>

### 4.3 렌더링된 엘리먼트 업데이트 하기
---
<br>

* #### 다음 코드는 tick() 함수를 정의하고 있다. 
* #### 이 함수는 현재 시간을 포함한 element를 생성해서 root div에 렌더링해 준다.
* #### 그런데 


## 2024-03-20 React 3주차 강의 내용  
<br>

## Chapter 1. 리액트 

### 1.1 리액트는 무엇인가?
----
<br>

#### -웹 및 앱 유저 인터페이스를 위한 라이브러리-  
#### -The Library for Web and Native User Interfaces.-
>##### (공식 사이트: react.dev)
<br>

* #### 복잡한 사이트를 쉽고 빠르게 만들고, 관리하기위해 만들어진 것.
* #### 다른 표현으로는 SPA를 쉽고 빠르게 만들 수 있도록 해주는 도구.  
<br>

### 1.2 리액트의 장점  
----
<br>

#### 1.빠른 업데이트와 랜더린 속도  
> * ##### Virtual DOM
> * ##### DOM(Document Object Model)이란 XML, HTML문서의 각 항목을 계층으로 표현하여 생성, 변형, 삭제할 수 있도록 돕는 인터페이스. (W3C의 표준)
> * ##### Virtual DOM은 DOM 조작이 비효율적인 이유로 속도가 느려 고안된 방법.  
> * ##### DOM - 동기식, Virtual DOM - 비동기식 -방법으로 랜더링 (동기식은 일부분이 바껴도 전체적으로 바꿈, 비동기식은 일부분만 바꿈.)
<br>

#### 2.컴포넌트 기반 구조  
> * ##### 리액트의 모든 페이지는 컴포넌트로 구성됨.
> * ##### 하나의 컴포넌트는 다른 여러개의 컴포넌트와의 조합으로 구성 가능.
> * ##### 리엑트로 개발 -> 레고 블록을 조립하는 듯한 방식으로 웹사이트 개발.
<br>

#### 3.재사용성  
> * ##### 반복적인 작업을 줄여 생산성을 높여줌.
> * ##### 유지보수
> * ##### 재사용이 가능할려면 의존성이 없어야함.  

<br>

#### 4.든든한 지원군
> * ##### 메타에서 오픈소스 프로젝트로 관리하고 있어 계속 발전하고 있음.
<br> 

#### 5.활발한 지식 공유 & 커뮤니티
<br>

#### 6.모바일 앱 개발가능
> * ##### 리액트 네이티브라는 모바일 환경 UI 프레임워크를 사용하면 크로스 플랫폼 모방일 앱을 개발 할 수 있음  
<br>

### 1.3 리액트의 단점
<br>

#### 1. 높은 상태 관리 복잡도
<br>  

## Chapter 2. 리액트 시작하기  
<br>

### 2.1 Create-react-app으로 만들기
<br>

![리액트만들기](리액트_create-react-app.png)
<br>

#### 위에 사진 치고 .gitignore에서 터미널 열고 npm start   
<br>


---------

## 3주차 총정리  
<br>

> * #### 리액트가 무엇인지, 장단점, 프로젝트 만들기  
<br>


## 2024-03-13 React 2주차 강의 내용
<br>

### GitHub 사용법     
<br>

## git config user.name  
## git config user.email  

