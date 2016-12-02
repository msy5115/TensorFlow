# スライシング

計算結果を再現させる場合に利用する。

Sample

```python
# coding:utf-8
import numpy as np

# 0から10までの配列
x = np.arange(10)
# => [ 0,  1,  2,  3,  4,  5,  6,  7,  8,  9]

# 全部の値を取得する
print x[:]
# 全部の値を逆順で取得する
print x[::-1]
# 4番目以降の値を取得する
print x[4:]
# 7番目までの値を取得する
print x[:7]
# 4番目から7番目までの値を取得する
print x[4:7]
# 1番目から8番目までの値を1つ飛ばしで取得する
print x[1:8:2]
# 8番目から1番目までの値を逆順で取得する
print x[8:1:-1]

# 行列(多次元配列)に関しても同様
# 0から16までの4x4行列
# => [[ 0,  1,  2,  3],
#     [ 4,  5,  6,  7],
#     [ 8,  9, 10, 11],
#     [12, 13, 14, 15]]
y = np.arange(16).reshape((4,4))

# 2行3列の要素
print y[2,3]
# 以下も同様
print y[2][3]
# 2行目
print y[2]
# 3列目
print y[:,3]
```

出力結果

```shell
[0 1 2 3 4 5 6 7 8 9]
[9 8 7 6 5 4 3 2 1 0]
[4 5 6 7 8 9]
[0 1 2 3 4 5 6]
[4 5 6]
[1 3 5 7]
[8 7 6 5 4 3 2]
11
11
[ 8  9 10 11]
[ 3  7 11 15]
```