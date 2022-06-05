---
output: html_document
editor_options: 
  chunk_output_type: console
---




# 경우의 수 {#prob-case}

고대 로마 수학자 보이티우스 (Boethius, 477 - 524)와 인도 수학자 바스카라 (Bhaskara, 1114-1185)는 확률이 알려기기 이전부터
현재 경우의 수라고 불리는 개념을 탐색했다고 알려져 있다.

# 여러가지 순열

- 원순열
- 중복순열

## 원순열 {#circula-permutation}

원수열은 서로 다른 것을 원형으로 배열할 때 경우의 수가 얼마나 될지 따지는 것이다.

### A &rarr; B &rarr; C &rarr; D &rarr; A


```{=html}
<div id="htmlwidget-19563f9f0ac16b3a595e" style="width:672px;height:480px;" class="DiagrammeR html-widget"></div>
<script type="application/json" data-for="htmlwidget-19563f9f0ac16b3a595e">{"x":{"diagram":"\n  graph LR\n    A-->B\n    B-->C\n    C-->D\n    D-->A\n"},"evals":[],"jsHooks":[]}</script>
```

### B &rarr; A &rarr; D &rarr; C &rarr; B


```{=html}
<div id="htmlwidget-d406df56954abd7a35e0" style="width:672px;height:480px;" class="DiagrammeR html-widget"></div>
<script type="application/json" data-for="htmlwidget-d406df56954abd7a35e0">{"x":{"diagram":"\n  graph LR\n    B-->A\n    A-->D\n    D-->C\n    C-->B\n"},"evals":[],"jsHooks":[]}</script>
```

이와 같이 4가지 경우가 있을 때 이를 조합하면 몇가지 경우의 수가 생기게 될까?

1. 4가지 문자 중 하나를 선택한다. 
1. 앞서 4개중 하나를 뺐기 때문에 3가지중 하나를 선택한다.
1. 앞서 3개중 하나를 뺐기 때문에 2가지중 하나를 선택한다.
1. 마지막 남은 한가지를 선택한다.


따라서, $4 \times 3 \times 2 \times 1 = 24$

하지만 원으로 배열하면 같은 것이 4가지 있기 때문에 원형으로 배열하는 경우의 수는 
다음과 같다.

$$ \frac{4!}{4} = \frac{4 \times 3 \times 2 \times 1}{4} = 3 \times 2 \times 1 = 6$$

이것을 일반화하면 다음과 같다.

$$\frac{n!}{n} = (n-1)!$$

## 중복순열 {#permutations}

자전거 도난방지를 위해서 체인형태로 된 자물쇠 비빌번호는 통상 4자리로 구성된다. 
4자리로 구성된 자전거 비밀번호 총 조합의 수는 몇개나 될까?

각 자리는 0~9까지 총 10개 숫자로 구성된다. 따라서 각각을 달리 설정하여 나오는 총 
비밀번호 경우의 수는 다음과 같이 구할 수 있다.

$10 \times 10 \times 10 \times 10 = 10^4$

상기 방식을 일반화할 수 있다.

1. 10자리가 아니라 $n$ 자리로 확장하는 경우
    - $n \times n \times n \times n = n^4$
1. 자물쇠 비밀번호 자리수를 4개에서 $r$개까지 확장하는 경우
    - $\underbrace{10 \times 10 \times 10 \times 10 \times \cdots \times 10}_\text{r번} = 10^r$
1. $n$ 자리 $r$번 확장하는 경우
    - $\underbrace{n \times n \times n \times n \times \cdots \times n}_\text{r번} = n^r$

서로다른 $n$개에서 $r$개를 선택하는 중복순열의 수는 수식을 이용하여 표현하면 다음과 같다.

$${}_n \Pi _r = \underbrace{n \times n \times n \times n \times \cdots \times n}_\text{r번} = n^r$$

A,B,C,D 네가지 영문자를 조합하는 경우수를 컴퓨터를 이용하여 나열하면 다음과 같다.


```
      [,1] [,2] [,3] [,4]
 [1,] "A"  "B"  "C"  "D" 
 [2,] "A"  "B"  "D"  "C" 
 [3,] "A"  "C"  "B"  "D" 
 [4,] "A"  "C"  "D"  "B" 
 [5,] "A"  "D"  "B"  "C" 
 [6,] "A"  "D"  "C"  "B" 
 [7,] "B"  "A"  "C"  "D" 
 [8,] "B"  "A"  "D"  "C" 
 [9,] "B"  "C"  "A"  "D" 
[10,] "B"  "C"  "D"  "A" 
[11,] "B"  "D"  "A"  "C" 
[12,] "B"  "D"  "C"  "A" 
[13,] "C"  "A"  "B"  "D" 
[14,] "C"  "A"  "D"  "B" 
[15,] "C"  "B"  "A"  "D" 
[16,] "C"  "B"  "D"  "A" 
[17,] "C"  "D"  "A"  "B" 
[18,] "C"  "D"  "B"  "A" 
[19,] "D"  "A"  "B"  "C" 
[20,] "D"  "A"  "C"  "B" 
[21,] "D"  "B"  "A"  "C" 
[22,] "D"  "B"  "C"  "A" 
[23,] "D"  "C"  "A"  "B" 
[24,] "D"  "C"  "B"  "A" 
```

### 같은 것이 있는 순열


## 중복조합






