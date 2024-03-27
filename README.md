# 정재승 202230233  
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

