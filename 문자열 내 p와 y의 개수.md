# ๐ <span style="color:#2c2c2c;">๋ฌธ์์ด ๋ด p์ y์ ๊ฐ์</span>

ํ๋ก๊ทธ๋๋จธ์ค ๋ฌธ์์ด Level 1๐

## โ <span style="color:#fff;background-color:#F15F5F"> ๋ฌธ์ ์ค๋ชย </span>

๋๋ฌธ์์ ์๋ฌธ์๊ฐ ์์ฌ์๋ ๋ฌธ์์ด s๊ฐ ์ฃผ์ด์ง๋๋ค. s์ 'p'์ ๊ฐ์์ 'y'์ ๊ฐ์๋ฅผ ๋น๊ตํด ๊ฐ์ผ๋ฉด True, ๋ค๋ฅด๋ฉด False๋ฅผ return ํ๋ solution๋ฅผ ์์ฑํ์ธ์. 'p', 'y' ๋ชจ๋ ํ๋๋ ์๋ ๊ฒฝ์ฐ๋ ํญ์ True๋ฅผ ๋ฆฌํดํฉ๋๋ค. ๋จ, ๊ฐ์๋ฅผ ๋น๊ตํ  ๋ ๋๋ฌธ์์ ์๋ฌธ์๋ ๊ตฌ๋ณํ์ง ์์ต๋๋ค.

์๋ฅผ ๋ค์ด s๊ฐ "pPoooyY"๋ฉด true๋ฅผ returnํ๊ณ  "Pyy"๋ผ๋ฉด false๋ฅผ returnํฉ๋๋ค.

<br>

## ๐ <span style="color:#fff;background-color:#F15F5F"> ์ ํ์ฌํญ </span>

- ๋ฌธ์์ด s์ ๊ธธ์ด : 50 ์ดํ์ ์์ฐ์
- ๋ฌธ์์ด s๋ ์ํ๋ฒณ์ผ๋ก๋ง ์ด๋ฃจ์ด์ ธ ์์ต๋๋ค.

<br>

## ๐ง <span style="color:#F15F5F;">์์ถ๋ ฅ ์</span>

| s         | return |
| :-------- | ------ |
| "pPoooyY" | true   |
| "Pyy"     | false  |

<br>

## ๐ <span style="color:#fff;background-color:#F15F5F">ย ๋์ ์ดํดย </span>

1. ๋ฌธ์์ด 'p','y' ์ฐพ๊ธฐ

2. ๋ฌธ์์ด p์ ๊ธธ์ด์ y์ ๊ธธ์ด ๋น๊ต

<br>

## โ์ฒ์์ฝ๋โ(์คํจ)

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

#### ์คํจ ์์ธ

- ๋ฌธ์์ด ์๋ฌธ์, ๋๋ฌธ์ ๋ณํ์ ์ํ๊ณ  indexOf ๋ฉ์๋๋ฅผ ์ฌ์ฉํด ๋ฌธ์๋ฅผ ์ฐพ์ผ๋ คํ๊ณ  indexOf์ '๋ฐฐ์ด์์ ์ง์ ๋ ์์๋ฅผ ์ฐพ์ ์ ์๋ ์ฒซ ๋ฒ์งธ ์ธ๋ฑ์ค๋ฅผ ๋ฐํํ๋ค'๋ ์ ์๊ฐ ๋ด ๋ก์ง์์๋ ๋ถํ์ํ ๋ฉ์๋์๋ค๋๊ฑธ ์์๋ค.

## โ2๋ฒ์งธ ์ฝ๋โ(์ฑ๊ณต)

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

- toLowerCase/toUpperCase๋ผ๋ ์๋ฌธ์ -> ๋๋ฌธ์ / ๋๋ฌธ์ -> ์๋ฌธ์ ์นํ ๋ฉ์๋๋ฅผ ์ฒ์ ์๊ฒ ๋์๋ค.
- indexOf๊ฐ ์๋ String ๊ฐ์ฒด๋ฅผ ์ง์ ํ ๊ตฌ๋ถ์๋ฅผ ์ด์ฉํ์ฌ ์ฌ๋ฌ ๊ฐ์ ๋ฌธ์์ด์ ๋๋๋ ์ ์๋ฅผ ๊ฐ์ง Split ๋ฉ์๋๋ฅผ ์ฌ์ฉํ๋ค.
