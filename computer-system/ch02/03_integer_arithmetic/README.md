# 정수 산술

## 부호 없는 정수(Unsigned)의 덧셈

두 부호 없는 정수 $x$, $y$를 고려해보자

$x$, $y$는 다음을 따른다.

$$ 0 \le x, y \le 2^w - 1 $$

만약 x, y를 덧셈하게 되면 범위는 다음과 같이 바뀐다.

$$ 0 \le x, y \le 2^{w+1} - 2 $$

즉, 이 합을 표현하기 위해서는 $w + 1$ 개의 비트가 필요한 것이다. 또한 이 값을 유지하고 다른 값을 더하려면 $w + 2$ 개의 비트가 필요할 수 있다.

### 오버플로우

unsinged int $x$, $y$가 존재할 때, $x + y$ 가 $x$보다 크거나 같다면, 오버플로우가 일어난다.

## 이진 보수(Signed)의 덧셈

두 이진 보수 $x$, $y$는 다음을 따른다.

$$ -2^{w - 1} \le x, \space y \le 2^{w - 1} - 1 $$

즉, $x + y$의 범위는 다음과 같다.

$$ -2^w \le x + y \le 2^{w} -2 $$

![이진 보수 간의 덧셈에 대한 관계](./static//img1.PNG)

### 오버플로우