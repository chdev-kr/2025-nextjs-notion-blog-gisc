# 2025 Vanilla JavaScript Study Log

## 📚 프로젝트 소개

Vanilla JavaScript 학습 과정을 기록하고 실습하는 저장소입니다.

## 🎯 학습 목표

- JavaScript 기본 문법 마스터
- DOM 조작 및 이벤트 처리
- 비동기 프로그래밍 (Promise, async/await)
- ES6+ 문법 활용
- 실전 프로젝트 구현

## 📊 학습 진행사항

### 섹션 1: JavaScript 기초

- [x] 자바스크립트의 실행 환경 (2025-08-17)
- [x] 변수와 상수 (2025-08-17)
- [x] 자료형과 형 변환 (2025-08-17)
- [x] 연산자 (2025-08-17)
- [x] 조건문 (2025-08-17)
- [x] 함수 (2025-08-17)
- [ ] 스코프 (완료일: )
- [ ] 호이스팅 (완료일: )
- [ ] 함수 표현식과 화살표 함수 (완료일: )
- [ ] 객체 (완료일: )
- [ ] 배열 (완료일: )
- [ ] 생성자 함수 (완료일: )
- [ ] 반복문 (완료일: )
- [ ] 배열 메서드-1 (완료일: )
- [ ] 배열 메서드-2 (완료일: )
- [ ] 배열과 객체 구조 분해 할당 (완료일: )
- [ ] spread와 rest (완료일: )

### 섹션 2: 비동기와 API

- [ ] 비동기 처리 (완료일: )
- [ ] 프로미스 객체 (완료일: )
- [ ] async와 await (완료일: )
- [ ] API 호출 (완료일: )

### 섹션 3: DOM과 DOM API

- [ ] 웹과 DOM (완료일: )
- [ ] DOM API-1 (완료일: )
- [ ] DOM API-2 (완료일: )
- [ ] 여러가지 폼 조작 (완료일: )

### 섹션 4: this와 화살표 함수

- [ ] 자바스크립트의 this-1 (완료일: )
- [ ] 자바스크립트의 this-2 (완료일: )
- [ ] this와 화살표 함수 (완료일: )

### 섹션 5: 중간 프로젝트

- [ ] 동물 앨범 만들기 코드 (완료일: )
- [ ] 동물 앨범 만들기-1-1 (완료일: )
- [ ] 동물 앨범 만들기-1-2 (완료일: )

### 섹션 6: 컴포넌트와 모듈 시스템

- [ ] 컴포넌트란 (완료일: )
- [ ] 모듈 시스템이란 (완료일: )
- [ ] 동물 앨범 만들기-2-1 (완료일: )

### 섹션 7: 상태 관리와 SPA

- [ ] 상태 관리란 (완료일: )
- [ ] 동물 앨범 만들기-2-2 (완료일: )
- [ ] 동물 앨범 만들기-2-3 (완료일: )
- [ ] MPA와 SPA (완료일: )
- [ ] SPA와 라우팅 (완료일: )
- [ ] 동물 앨범 만들기-3 (완료일: )
- [ ] express 버전 안내 (완료일: )
- [ ] node.js와 express.js (완료일: )

### 섹션 8: 최종 프로젝트

- [ ] 최종 프로젝트 안내 (완료일: )
- [ ] Trip Wiki 코드 (완료일: )
- [ ] 여행지 정보 웹 사이트(Trip Wiki) (완료일: )
- [ ] 컴포넌트화 작업 (완료일: )
- [ ] CityList 개발 (완료일: )
- [ ] Header 개발 (완료일: )
- [ ] RegionList 개발 (완료일: )
- [ ] CityDetail 개발-1 (완료일: )
- [ ] CityDetail 개발-2 (완료일: )
- [ ] 강의를 마치면서 (완료일: )

## 📝 학습 내용 정리

### 🔧 기본 문법

#### 변수와 상수

```javascript
let num = 10; // 변수 (재할당 가능)
const PI = 3.14; // 상수 (재할당 불가)
var oldWay = "구식"; // var (사용 권장하지 않음)
```

#### 자료형과 형 변환

```javascript
// 기본 자료형
let string = "문자열";
let number = 42;
let boolean = true;
let nullValue = null;
let undefinedValue = undefined;

// 형 변환
let strToNum = parseInt("123"); // 문자열 → 숫자
let numToStr = String(123); // 숫자 → 문자열
```

#### 연산자

```javascript
// 증감 연산자
let num = 10;
console.log(num++); // 10 (후위 연산)
console.log(num); // 11
console.log(++num); // 12 (전위 연산)

// 비교 연산자
console.log(10 === "10"); // false (엄격한 비교)
console.log(10 == "10"); // true (느슨한 비교)

// 논리 연산자
console.log(true && false); // false (AND)
console.log(true || false); // true (OR)
console.log(!true); // false (NOT)

// null 병합 연산자
let value = undefined ?? "기본값"; // "기본값"

// 삼항 연산자
let result = 10 > 5 ? "크다" : "작다"; // "크다"
```

#### 조건문

```javascript
// if-else
if (num > 10) {
  console.log("10보다 크다");
} else if (num === 10) {
  console.log("10이다");
} else {
  console.log("10보다 작다");
}

// switch-case
switch (fruit) {
  case "apple":
    console.log("사과");
    break;
  case "banana":
    console.log("바나나");
    break;
  default:
    console.log("다른 과일");
}
```

#### 함수

```javascript
// 함수 선언식
function add(num1, num2) {
  return num1 + num2;
}

// 함수 표현식
const multiply = function (num1, num2) {
  return num1 * num2;
};

// 화살표 함수
const divide = (num1, num2) => num1 / num2;

// Early Return Pattern (가독성 좋은 코드)
function compare(num) {
  if (num === 0) return "0이다";
  if (num < 0) return "음수이다";
  if (num >= 10) return "10 이상이다";
  return "0보다 크고 10보다 작다";
}
```
