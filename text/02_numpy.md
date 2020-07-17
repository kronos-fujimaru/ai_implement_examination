# そうだ、AI実装師になろう！

## 2. NumPyライブラリ

### 2-1. NumPyライブラリとは

NumPyライブラリは、Pythonで数値計算を効率的に行うためのライブラリです。ndarrayという多次元配列を使って、数値データを高速に、かつ柔
軟に処理できることが特徴です。

例えば、配列の各要素の値を足し算したい場合、Pythonのリスト同士を足しても計算はされず、要素が増えるだけです。

```python
num1 = [1, 2, 3]
num2 = [4, 5, 6]

num3 = num1 + num2

print(num3)
```

**実行結果**

```
[1, 2, 3, 4, 5, 6]
```

<br>

そこで、NumPy配列を使用すると、NumPy配列同士を足すことで、要素ごとの値を計算することができます。

```python
import numpy as np

np_num1 = np.array([1, 2, 3])
np_num2 = np.array([4, 5, 6])

np_num3 = np_num1 + np_num2

print(np_num3)
```

**実行結果**

```
[5 7 9]
```

<br>

その他にもスライスなどの機能もあり、データ分析や機械学習をする上で必要な計算が容易にできるようになります。

NumPyを使用する場合は以下のようにimportする必要があります。

```python
import numpy as np
```

<br>

### 2-2.
