# 경사 하강법(Gradient discent)
선형회귀를 통해 구한 그래프를 $y = ax + b$라고 할 때, 오차는 기울기 $a$값에 따라 그 규모가 결정된다.\
이러한 관계는 이차함수 형태( $y = 오차$ , $x = 기울기(a)$ )로 나타난다.\
경사 하강법이란 해당 이차함수에서 미분값이 0이 되는 지점, 즉 오차 값의 극소를 구하여, 최적의 기울기값( $m$ )을 구하는 과정이다.\
경사 하강법은 기울기 $a$ 뿐 아니라 $y$절편 $b$를 구하는 데에도 사용된다.

## 학습률(learning rate)
경사 하강법에서는 최적의 값을 찾기 위해 특정 값을 기준으로 대입값을 증감시키는데, 이 때 이동하는 거리를 __학습률(leraning rate)__ 이라고 한다.\
딥러닝에서의 최적화는 학습률의 값을 적절히 바꿔가며 최적의 학습률을 찾아가는 과정이라고 할 수 있다.

## 미분
- MSE는 다음과 같다.

$$평균제곱오차(MSE) = \frac{1}{n} \sum_{i}^n (y_i - \hat{y}_i)^2 $$

- $\hat{y}_i$는 $x_i$를 대입했을 때의 값이므로, $y_i = ax_i + b$를 대입한다.

$$\frac{1}{n} \sum_{i}^n (y_i - (ax_i + b))^2 $$

- $a$와 $b$에 대해 알아야 하므로, 편미분을 이용하면 다음과 같다.

$$a로 편미분한 결과 = \frac{2}{n} \sum(ax_i + b - y_i)x_i$$

$$b로 편미분한 결과 = \frac{2}{n} \sum(ax_i + b - y_i)$$

## 코드로 구현해보자
https://github.com/catuscio/DeepLearning-Basic/blob/main/colab%20workout/gradient_descent.ipynb

-----

# 다중 선형 회귀
기존의 선형 회귀에서 새로운 데이터 축이 추가된 것이다.
$$y = a_1 x_1 + a_2 x_2 + b$$

## 코드로 구현해보자
https://github.com/catuscio/DeepLearning-Basic/blob/main/colab%20workout/multi_linear_regression.ipynb

-----
### 궁금한 점
colab 노트로 이동이 불가능하다. 아무래도 github api에서 토큰을 발급 받던지 git 명령어로 따로 마운트를 해야되는 것 같은데 잘 모르겠다,,
