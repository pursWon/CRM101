#  filter() 함수

filter()은 배열에 사용하며, 주어진 함수의 조건을 만족하는 모든 요소를 모아 새로운 배열로 반환합니다.
출처: https://codesign.tistory.com/165 [CODESIGN:티스토리]

</br>

### filter()함수 기본 문법

```javascript
arr.filter(callback(element[, index[, array]])[, thisArg])
```

- element : 요소 값
- index : 요소의 인덱스
- array : 사용되는 배열 객체

</br>

### 예시1

아래 코드에 array라는 배열에서 10 미만인 값을 출력해보려고 한다.    
이를 위해 우선 결과값들을 담아둘 result 변수를 만들고,  filter()에 필터 조건을 넣어 주었다.    

</br>

```javascript

let array = [1,12,3,'string'];

let result = array.filter((value) => value < 10)

console.log(result);

// 결과: [1,3]
```

</br>

### 예시2 

</br>

특정 값 삭제. 주어진 arr 배열에서 b를 삭제해보았다.

```javascript

let arr = ['a', 'b', 'b', 'c'];

// 원소 'b' 삭제
let filtered = arr.filter((element) => element !== 'b');

console.log(filtered); // ['a', 'c']
```

</br>






