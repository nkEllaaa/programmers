# programmers - 프로그래머스 문제풀이 


## 1️⃣  양꼬치
### 💡 문제 설명
`머쓱이네 양꼬치 가게는 10인분을 먹으면 음료수 하나를 서비스로 줍니다. 양꼬치는 1인분에 12,000원, 음료수는 2,000원입니다. 정수 n과 k가 매개변수로 주어졌을 때, 양꼬치 n인분과 음료수 k개를 먹었다면 총얼마를 지불해야 하는지 return 하도록 solution 함수를 완성해보세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120830
<br>
<br>
<strong>- 내가 푼 답</strong>
```js
    function solution(n, k) {
  	let answer = 0;
    if (n >= 10) {
       k -= Math.floor(n/10);
    }
    answer = n*12000+k*2000
    return answer;
}
```
<strong>- 참고할만한 답</strong>
```js
   function solution(n, k) {
    return n*12000 + k*2000 - parseInt(n/10)*2000
}
```
- [x] 함수보다는 메소드를 좀 더 활용하는 방법으로 풀어보기
<br>
<br>

## 2️⃣   배열의 평균값 구하기
### 💡 문제 설명
`정수 배열 numbers가 매개변수로 주어집니다. numbers의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120817
<br>
<br>
<strong>- 내가 푼 답</strong>
```js
    function solution(numbers) {
    return numbers.reduce(((acc, cur) => acc + cur), 0) / numbers.length
}
```
- [x] reduce 초기값 주의하기

<br>
<br>

## 3️⃣    피자 나눠 먹기
### 💡 문제 설명
`머쓱이네 피자가게는 피자를 일곱 조각으로 잘라 줍니다. 피자를 나눠먹을 사람의 수 n이 주어질 때, 모든 사람이 피자를 한 조각 이상 먹기 위해 필요한 피자의 수를 return 하는 solution 함수를 완성해보세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120814
<br>
<br>
<strong>- 내가 푼 답</strong>
```js
function solution(n){
    let pizza = 0;
    if(n%7 === 0){
        pizza = parseInt(n/7);
    }
    else {
        pizza = parseInt(n/7) + 1
        
    }
    return pizza;
}
```
<strong>- 참고할만한 답</strong>
```js
function solution(n) {
    return n % 7 === 0 ? n / 7 : parseInt(n / 7) + 1;
}
```
- [x] 생각보다 삼항연산자가 쓰이는 알고리즘이 많다.
<br>
<br>

## 4️⃣   중복된 숫자 갯수
### 💡 문제 설명
`정수가 담긴 배열 array와 정수 n이 매개변수로 주어질 때, array에 n이 몇 개 있는 지를 return 하도록 solution 함수를 완성해보세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120583
<br>
<br>
<strong>- 내가 푼 답</strong>
```js
function solution(array, n) {
    let count = 0;
    for (let i = 0; i < array.length; i++) {
        if(array[i] === n)
            count++;
    }
    return count;
}
```
```js
function solution(array, n) {
  let count = 0;
  array.forEach((item) => {
    if (item === n) {
      count++;
    }
  });
  return count;
}
```
<strong>- 참고할만한 답</strong>
```js
function solution(array, n) {
      return array.filter(num => num === n).length;
      }
```
- [x] 같은문제를 다양하게 풀어보자
<br>
<br>

## 5️⃣ 짝수 홀수 개수
### 💡 문제 설명
`정수가 담긴 리스트 num_list가 주어질 때, num_list의 원소 중 짝수와 홀수의 개수를 담은 배열을 return 하도록 solution 함수를 완성해보세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120824
<br>
<br>
<strong>- 내가 푼 답</strong>
```js
function solution(num_list) {
    let even = num_list.filter(num => num % 2 === 0).length
    let odd = num_list.filter(num => num % 2 !== 0).length
    
    return [even, odd];
}
// filter() 메서드는 주어진 함수의 테스트를 통과하는 모든 요소를 모아 새로운 배열로 반환한다.
```
```js
function solution(num_list) {
    let answer = [0,0];

    for(let i of num_list) { //for of 문에서 i는 value를 의미한다.
        if(i % 2 === 1) answer[1] += 1;
        else answer[0] += 1;
    }

    return answer
}
```
<strong>- 참고할만한 답</strong>
```js
function solution(num_list) {
    var answer = [0,0];

    for(let a of num_list){
        answer[a%2] += 1 //나머지로 인덱스를 구분할 수 있다는 새로운 접근을 알게되었다.
    }

    return answer;
}
```
- [x] 다른사람의 답을 열심히 공부하자
<br>
<br>


## 6️⃣
