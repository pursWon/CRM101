#  Map() 함수 


배열의 요소를 순회하려면 for문과 같은 반복문이 필요한데, map() 함수를 쓰면 for문을 쓰지 않고도 배열 전체를 순회하면서 각 요소에 대해 함수를 호출한다. 각 요소는 순서대로 함수를 타고, 함수에 정의된 새로운 형태의 배열로 반환되는 것이다.
js에 약한데 실무에서 굉장히 유용하게 쓰게 되어 기록으로 남긴다. 

</br>

### map()함수 기본 문법

```javascript
array.map(callBackFunction(currValue, index, array), newValue);
```

- currValue: 원본 배열의 데이터 
- index : 현재처리중인 인덱스 
- array : 기존 배열 
- newValue: callBackFunction에서 사용될 값 

</br>

### 예시1

```javascript

let array = ["월", "화", "수"];
let map = array.map(item => item + "요일");
//기존요소 + 요일 추가
console.log(map);

```

</br>

### 예시2 

```javascript

let array = ["월", "화", "수"];
let map = array.map(customFunc);//사용자 함수 넣기 

function customFunc(item){
 return item + "요일";
}
console.log(map);


//같은 결과
["월요일", "화요일", "수요일"]

//OR 

let array = ["월", "화", "수"];
let map = array.map(function(item){return item + "요일"}); //바로 함수넣기 

console.log(map);


//같은 결과
["월요일", "화요일", "수요일"]
```

</br>

### 예시3

```javascript

let originDataList = 
    [{"param1":"아무개1", "param2":"01012341234"}
    ,{"param1":"아무개2", "param2":"01012341234"}
    ,{"param1":"아무개3", "param2":"01012341234"}];

let customDataList = originDataList.map(item => {name:item.param1, phone_num:item.param2}); 
//name key에 param1의 value, 
//phone_num key에 param2 value 셋팅. 

console.log(customDataList);

//결과 
 [{"name":"아무개1", "phone_num":"01012341234"}
 ,{"name":"아무개2", "phone_num":"01012341234"}
 ,{"name":"아무개3", "phone_num":"01012341234"}]
```





