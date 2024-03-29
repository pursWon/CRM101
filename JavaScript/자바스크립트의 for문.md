# 자바 스크립트의 for문 
 
## for문

가장 일반적인 for문의 형태는 다음과 같다.
console.log(i)를 총 10번 반복하는 반복문이다.

```javascript

for(let i = 0; i<10; i++){
	console.log(i);
}

```
≈

for문 안의 구성이 각각 의미하는 바를 살펴보면,   
let i=0 : 변수 let i를 선언하고 0으로 할당 (반복문 초기값 설정).   
i<10 : for문을 얼마나 돌릴 것인지 조건을 적는 부분(조건이 참이면 실행).   
i++ : 루프가 한번 돌때마다 변수 증감식.   
여기에서는 i가 0부터 시작해서 10보다 작을 때까지 이므로 0~9. 총 10번 반복할 것이다.    
i의 값은 루프가 한 번 돌때마다 1씩 증가하여 console.log는 1, 2, 3, .... 9를 순서대로 출력하고 for문은 종료된다.    

for in문은 object 에 사용할 수 있는 반복분이다.   
배열에도 사용할 수 있지만 배열 반복에는 추천되지 않는다.

</br>

## for..in

for in문은 object 에 사용할 수 있는 반복분이다.
배열에도 사용할 수 있지만 배열 반복에는 추천되지 않는다.

</br>

```javascript

const obj = {
  name : '이름',
  age : '나이'
}

for(const key in obj){
  console.log(key); // key값 출력
  console.log(obj.name, obj.age); // value 값 출력

  console.log(`key 값 : ${key}`); // 1. key값 : 이름 // 2. key값 :age
  console.log(`value 값 : ${obj[key]}`); // 1. value 값 : 이름 // 2. value값 : 나이
}

````

기본 for문과 생김새는 비슷하다. 대신 in 키워드를 사용한다.    
obj.name과 같이 사용하려면 object내에 name이라는 key값을 가진 value가 존재해야한다.   
없는 key값을 사용하게 되면 undefined가 출력된다.    
객체의 모든 value값을 얻으려면 obj[key]로 객체를 순회하여 얻을 수 있다.   

## for...of

for of문은 반복 가능한 객체(Array, Map, Set, String, TypedArray, arguments 객체 등 포함)에 대해 사용할 수 있다.    

보통은 Array(배열)에 사용한다고 흔히 알려져 있다.   

</br>

```javascript

const array = ['1번', '2번', '3번'];

for(const element of array) {
  console.log(element); // 배열[0] ~ 끝까지 순차적 출력
  console.log(array); // 배열 전체 출력
}

```

</br>

배열에 들어있는 0번째~마지막 번째 요소까지 순차적으로 출력된다.
배열안에 있는 요소를 꺼내쓸 때 사용하면 좋다.

</br>

## forEach

배열에 사용되는 메서드이다. 인자에 콜백함수를 넣어 사용한다.

```javascript 

const array = ['1번', '2번', '3번'];

array.forEach((element)=>{
  console.log(element);
})

```

## while

</br>

조건이 참이면 실행되는 반복문이다. 이전에 살펴본 for문처럼 반복 실행을 해준다.

```javascript

while(condition) {
  // condition이 참이면 실행
}

````

while의 ()안의 조건이 true면 실행, false면 실행되지 않는다.
즉, while(condition)이 false이면 단 1회도 실행하지 않는다는 것이다.

</br>

## do...while

앞에서 살펴본 while과는 달리 do{}에 작성된 코드는 최소 1번 실행된다는 것이다.   
최소 1번 실행 후, while 조건이 false인 경우 더이상 실행되지 않는다.

</br>

```javascript

do {
	// 거짓이더라도
  //do에 작성된 코드는 무조건 1회는 실행
}while(condition)

```
적어도 1번은 실행하고 싶은 코드가 있을 때 사용된다.








