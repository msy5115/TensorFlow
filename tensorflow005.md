# 標準正規分布のTensorを作る

正規分布により乱数を生成する。

`tf.random_normal(shape, mean=0.0, stddev=1.0, dtype=tf.float32, seed=None, name=None)`

* `shape` Tensorのサイズ
* `mean` 平均
* `stddev` 標準偏差
* `dtype` 値の型

デフォルトでは`mean=0.0, stddev=1.0`となっており、標準正規分布になっている。

```python
# coding:utf-8
import tensorflow as tf

# 標準正規分布による乱数を値に持つ3x3行列
x = tf.random_normal(shape=(3,3))

with tf.Session() as sess:
    y = sess.run(x)
    print y
```

計算結果

```shell
[[ 1.09942019  0.08562929  0.03443986]
 [-0.73919928 -0.21810924  0.91688985]
 [ 0.50970089  0.08562437  0.54271621]]
```

# 参考

* [TensorFlow API](https://www.tensorflow.org/versions/master/api_docs/python/constant_op.html#random_normal)