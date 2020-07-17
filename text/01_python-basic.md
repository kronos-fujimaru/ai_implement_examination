# そうだ、AI実装師になろう！

## 1. Python入門

それでは、まずPythonの基本文法について触れていきましょう。

<br>

### 1-1. Hello World

print関数で文字列や数値、変数の値を表示できます。

```python
print("Hello, World!!")
```

実行結果は次のように表示されます。

```
Hello, World!!
```

<br>

### 1-2. 変数とデータ型

Pythonで取り扱うデータ型を確認しましょう。

```python
name = "Paul"
age = 33
height = 171.3
license = True
money = None

print(type(name))
print(type(age))
print(type(height))
print(type(license))
print(type(money))
```

実行結果は次のように表示されます。

```
<class 'str'>
<class 'int'>
<class 'float'>
<class 'bool'>
<class 'NoneType'>
```

> Pythonは動的型付けに分類されるため、代入する値によってデータ型が決まります。

<br>

### 1-3. 分岐処理

分岐処理にはif文を使用します。インデントによってスコープを表現します。また、論理積には `and`キーワード、論理和には `or`キーワードが使用できます。

```python
age = 20
student = True

if student:
    print(1200)
elif age >= 65:
    print(1500)
else:
    print(1800)
```

実行結果は次のように表示されます。

```
1200
```

Pythonには、Javaなどのswitch文に相当する構文がありません。1つの値で複数の条件を判定したい場合は、`in`キーワードが使用できます。

```python
if age in {20, 30, 40, 50, 60}:
    print("OK")
else:
    print("NG")
```

<br>

### 1-4. 反復処理

反復処理にはfor文を使用します。指定回数繰り返すには range関数を使い、以下の形式で引数を指定します。

- range()

```python
for i in range(3):
    print(i)

print()

for i in range(1, 3):
    print(i)

print()

for i in range(3, 1, -1):
    print(i)
```

実行結果は次のように表示されます。

```
0
1
2

1
2

3
2
```

<br>

### 1-5. リスト

Pythonでリスト（配列）を生成するには、`[]`キーワードを使用します。生成後のリストに値を追加するには、`append`キーワードを使用します。

```python
fruits = ["apple", "banana", "cherry"]
fruits.append("grape")

for fruit in fruits:
    print(fruit)
```

実行結果は次のように表示されます。

```
apple
banana
cherry
grape
```

<br>

### 1-6. ディクショナリ

Pythonでディクショナリを生成するには、`{}`キーワードを使用します。ディクショナリとは、キーと値をマッピングしたオブジェクトです。

```python
fruits = {"apple":100, "banana":200, "cherry":300}

print(fruits["apple"])

for key in fruits:
    print(key)

for value in fruits.values():
    print(value)

for key, item in fruits.items():
    print(key, item)
```

実行結果は次のように表示されます。

```
100
apple
banana
cherry
100
200
300
apple 100
banana 200
cherry 300
```

> ディクショナリのkeysメソッドでキーが、valuesメソッドで値が、itemsメソッドでキーと値が取得できます。

<br>

### 1-7. 関数

Pythonでは、`def`キーワードを使用して関数を定義します。

```python
def calc(price, count):
    return price * count

print(calc(100, 5))
print(calc(200, 5))
print(calc(300, 5))
```

実行結果は次のように表示されます。

```
500
1000
1500
```

<br>

### 1-8. クラス

クラスを定義するには `class`キーワードを使用します。

```python
class Dog:
    def __init__(self, name, age):
        self.name = name
        self.age = age

    def introduce(self):
        print("Name:{}, Age:{}".format(self.name, self.age))

john = Dog('John', 5)
paul = Dog('Paul', 2)

john.introduce()
paul.introduce()
```

クラスの中でインスタンス⾃⾝を参照するには `self`キーワードを使います。クラスに定義したメソッドやコンストラクタの第1引数には self を指定する必要があります。また、クラスにコンストラクタを定義する場合は `__init__`メソッドを実装します。

実行結果は次のように表示されます。

```
Name:John, Age:5
Name:Paul, Age:2
```
