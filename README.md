# programmers - 프로그래머스 문제풀이 


## 1️⃣  양꼬치
### 💡 문제 설명
`머쓱이네 양꼬치 가게는 10인분을 먹으면 음료수 하나를 서비스로 줍니다. 양꼬치는 1인분에 12,000원, 음료수는 2,000원입니다. 정수 n과 k가 매개변수로 주어졌을 때, 양꼬치 n인분과 음료수 k개를 먹었다면 총얼마를 지불해야 하는지 return 하도록 solution 함수를 완성해보세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120830
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
```js
   function solution(n, k) {
    return n*12000 + k*2000 - parseInt(n/10)*2000
}
```

## 2️⃣   짝수 홀수 개수구하기



## 3️⃣   배열의 평균값 구하기
### 💡 문제 설명
`정수 배열 numbers가 매개변수로 주어집니다. numbers의 원소의 평균값을 return하도록 solution 함수를 완성해주세요.`

문제 링크 https://school.programmers.co.kr/learn/courses/30/lessons/120817
```js
    function solution(numbers) {
    return numbers.reduce(((acc, cur) => acc + cur), 0) / numbers.length
}
```
-> reduce 초기값 주의하기
