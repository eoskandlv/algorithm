# 📖 <span style="color:#2c2c2c;">문자열 내 p와 y의 개수</span>

프로그래머스 문자열 Level 1😆

## ✍ <span style="color:#fff;background-color:#F15F5F"> 문제설명 </span>

대문자와 소문자가 섞여있는 문자열 s가 주어집니다. s에 'p'의 개수와 'y'의 개수를 비교해 같으면 True, 다르면 False를 return 하는 solution를 완성하세요. 'p', 'y' 모두 하나도 없는 경우는 항상 True를 리턴합니다. 단, 개수를 비교할 때 대문자와 소문자는 구별하지 않습니다.

예를 들어 s가 "pPoooyY"면 true를 return하고 "Pyy"라면 false를 return합니다.

<br>

## 👉 <span style="color:#fff;background-color:#F15F5F"> 제한사항 </span>

- 문자열 s의 길이 : 50 이하의 자연수
- 문자열 s는 알파벳으로만 이루어져 있습니다.

<br>

## 🧐 <span style="color:#F15F5F;">입출력 예</span>

| s         | return |
| :-------- | ------ |
| "pPoooyY" | true   |
| "Pyy"     | false  |

<br>

## 👉 <span style="color:#fff;background-color:#F15F5F"> 나의 이해 </span>

1. 문자열 'p','y' 찾기

2. 문자열 p의 길이와 y의 길이 비교

<br>

## ❗처음코드❗(실패)

```
function solution(s){
   let answer = false;
    let pstr = s.indexOf('p')
    console.log(pstr)
    let ystr = s.indexOf('y')
    console.log(ystr)


    if(pstr.length == ystr.length){
    answer = true
    }
     return answer

}
```

#### 실패 원인

- 문자열 소문자, 대문자 변환을 안하고 indexOf 메소드를 사용해 문자를 찾으려했고 indexOf의 '배열에서 지정된 요소를 찾을 수 있는 첫 번째 인덱스를 반환한다'는 정의가 내 로직에서는 불필요한 메소드였다는걸 알았다.

## ❗2번째 코드❗(성공)

```
function solution(s){
   let answer = false;
    let pstr = s.toLowerCase().split('p')
    console.log(pstr)
    let ystr = s.toLowerCase().split('y')
    console.log(ystr)


    if(pstr.length == ystr.length){
    answer = true
    }
     return answer

}
```

- toLowerCase/toUpperCase라는 소문자 -> 대문자 / 대문자 -> 소문자 치환 메소드를 처음 알게 되었다.
- indexOf가 아닌 String 객체를 지정한 구분자를 이용하여 여러 개의 문자열을 나누는 정의를 가진 Split 메소드를 사용했다.
