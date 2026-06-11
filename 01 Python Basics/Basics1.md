# Python Basics

ਹੁਣ ਆਪਾਂ Python programming language ਦੀਆਂ basics ਪੜ੍ਹਾਂਗੇ। ਇੱਥੇ ਆਪਾਂ ਇਹ topics cover ਕਰਾਂਗੇ:

- Variables ਅਤੇ Data Types
- Operators
- Control Flow (if statements, loops)

---

## Variables

Python ਵਿੱਚ, variable ਇੱਕ container ਹੁੰਦਾ ਹੈ ਜਿਸ ਵਿੱਚ ਆਪਾਂ data values store ਕਰਦੇ ਹਾਂ। ਤੁਸੀਂ equals sign (`=`) ਵਰਤ ਕੇ ਕਿਸੇ variable ਨੂੰ value assign ਕਰ ਸਕਦੇ ਹੋ। ਮਿਸਾਲ ਲਈ:

```python
x = 5
y = "Sat Sri Akal!"
```

### ਇਹ ਚਾਹੀਦਾ ਕਿਉਂ ਹੈ?

ਕਿਉਂਕਿ computer ਕੋਲ memory ਹੁੰਦੀ ਹੈ ਅਤੇ ਆਪਾਂ ਨੂੰ ਉਸ memory ਵਿੱਚ data store ਕਰਨਾ ਪੈਂਦਾ ਹੈ। Memory ਇੱਕ limited resource ਹੈ ਤੇ ਆਪਾਂ ਨੂੰ ਇਸਨੂੰ ਸਹੀ ਢੰਗ ਨਾਲ access ਅਤੇ overwrite ਕਰਨਾ ਪੈਂਦਾ ਹੈ।

Variables ਆਪਾਂ ਨੂੰ ਇਹ ਕਰਨ ਦਿੰਦੇ ਹਨ। ਅੰਦਰੋਂ-ਅੰਦਰੀ, variable ਇੱਕ memory location ਨਾਲ map ਹੁੰਦਾ ਹੈ ਜਿੱਥੇ data store ਹੁੰਦਾ ਹੈ। ਆਪਾਂ variables ਵਰਤ ਕੇ numbers, strings, lists, ਅਤੇ ਹੋਰ ਕਈ ਕਿਸਮ ਦਾ data store ਕਰ ਸਕਦੇ ਹਾਂ।

ਸੌਖੇ ਸ਼ਬਦਾਂ ਵਿੱਚ ਸਮਝੋ - ਜਿਵੇਂ ਘਰ ਵਿੱਚ ਡੱਬੇ ਹੁੰਦੇ ਨੇ ਜਿਨ੍ਹਾਂ ਉੱਤੇ ਲਿਖਿਆ ਹੁੰਦਾ - "ਆਟਾ", "ਖੰਡ", "ਚਾਹਪੱਤੀ"। ਡੱਬੇ ਦਾ ਨਾਮ ਉਹੀ ਰਹਿੰਦਾ, ਪਰ ਅੰਦਰਲੀ ਚੀਜ਼ ਬਦਲ ਸਕਦੀ ਹੈ। Variable ਵੀ ਇਸੇ ਤਰ੍ਹਾਂ ਕੰਮ ਕਰਦਾ ਹੈ।

---

## Data Types

Python ਵਿੱਚ ਕਈ built-in data types ਹਨ ਜੋ ਆਪਾਂ ਵੱਖ-ਵੱਖ ਕਿਸਮ ਦਾ data store ਕਰਨ ਲਈ ਵਰਤ ਸਕਦੇ ਹਾਂ। Python ਦੇ ਕੁਝ ਆਮ data types:

- **int**: integers (ਪੂਰੇ numbers) store ਕਰਨ ਲਈ
- **float**: floating-point numbers (decimal numbers) store ਕਰਨ ਲਈ
- **str**: strings (text) store ਕਰਨ ਲਈ
- **bool**: boolean values (True ਜਾਂ False) store ਕਰਨ ਲਈ
- **list**: items ਦਾ collection store ਕਰਨ ਲਈ (ordered ਤੇ mutable) — list ਜਿਵੇਂ ਰਾਸ਼ਨ ਦੀ ਲਿਸਟ ਹੁੰਦੀ ਆ
- **tuple**: items ਦਾ collection store ਕਰਨ ਲਈ (ordered ਪਰ immutable — ਯਾਨੀ ਇੱਕ ਵਾਰ ਬਣਾਉਣ ਤੋਂ ਬਾਅਦ ਬਦਲੀ ਨਹੀਂ ਜਾ ਸਕਦੀ)
- **dict**: key-value pairs store ਕਰਨ ਲਈ (unordered ਤੇ mutable)
- **set**: unique items ਦਾ collection store ਕਰਨ ਲਈ (unordered ਤੇ mutable — ਇੱਕੋ value ਦੋ ਵਾਰ ਨਹੀਂ ਆ ਸਕਦੀ)

### Example

```python
x = 10                                    # int
y = 3.14                                  # float
name = "Harman"                           # str
is_student = True                         # bool
my_list = ["gheo", "makhan", "elaichi"]   # list
my_tuple = ("singh", "kaur", "khalsa ji") # tuple
my_dict = {"name": "khalsa ji", "age": 25} # dict
my_set = {1, 2, 3, 4, 5}                  # set
```

Dictionary ਵਿੱਚ key-value pair ਹੁੰਦੀ ਆ, ਜਿਵੇਂ ਇੱਥੇ `"name"` key ਹੈ ਅਤੇ `"khalsa ji"` value ਹੈ। ਸੌਖੇ ਸ਼ਬਦਾਂ ਵਿੱਚ — ਜਿਵੇਂ ਫ਼ੋਨ ਦੀ ਡਾਇਰੀ ਵਿੱਚ ਨਾਮ ਦੇ ਸਾਹਮਣੇ number ਲਿਖਿਆ ਹੁੰਦਾ। ਨਾਮ key ਹੈ, number value ਹੈ।

### Data Access ਕਰਨ ਦਾ Example

```python
print(x)              # Output: 10
print(name)           # Output: Harman
print(my_list[0])     # Output: gheo
print(my_tuple[1])    # Output: kaur
print(my_dict["name"]) # Output: khalsa ji
print(my_set)         # Output: {1, 2, 3, 4, 5}
```

ਯਾਦ ਰੱਖਣ ਵਾਲੀ ਗੱਲ — list ਅਤੇ tuple ਵਿੱਚ counting **0** ਤੋਂ ਸ਼ੁਰੂ ਹੁੰਦੀ ਹੈ, 1 ਤੋਂ ਨਹੀਂ। ਇਸੇ ਕਰਕੇ `my_list[0]` ਨਾਲ ਪਹਿਲੀ item "gheo" ਮਿਲਦੀ ਹੈ।

---

## Operators

Operators ਉਹ special symbols ਹੁੰਦੇ ਹਨ ਜੋ operands (variables ਅਤੇ values) ਉੱਤੇ ਕੋਈ ਖਾਸ operation perform ਕਰਦੇ ਹਨ। Python ਵਿੱਚ ਕਈ ਕਿਸਮ ਦੇ operators ਹਨ:

- **Arithmetic Operators**: `+`, `-`, `*`, `/`, `%`, `**`, `//` — ਜੋੜ, ਘਟਾਓ, ਗੁਣਾ, ਭਾਗ ਵਰਗੇ math operations ਲਈ
- **Comparison Operators**: `==`, `!=`, `>`, `<`, `>=`, `<=` — ਦੋ values ਨੂੰ compare ਕਰਨ ਲਈ
- **Logical Operators**: `and`, `or`, `not` — multiple conditions ਨੂੰ ਜੋੜਨ ਲਈ
- **Assignment Operators**: `=`, `+=`, `-=`, `*=`, `/=`, `%=`, `**=`, `//=` — variable ਨੂੰ value assign ਕਰਨ ਲਈ
- **Bitwise Operators**: `&`, `|`, `^`, `~`, `<<`, `>>` — bits ਉੱਤੇ ਸਿੱਧਾ ਕੰਮ ਕਰਨ ਲਈ
- **Membership Operators**: `in`, `not in` — ਇਹ check ਕਰਨ ਲਈ ਕਿ ਕੋਈ value collection ਦੇ ਅੰਦਰ ਹੈ ਜਾਂ ਨਹੀਂ
- **Identity Operators**: `is`, `is not` — ਇਹ check ਕਰਨ ਲਈ ਕਿ ਦੋ variables ਇੱਕੋ memory location ਨੂੰ point ਕਰਦੇ ਨੇ ਜਾਂ ਨਹੀਂ

### Example

```python
a = 10
b = 3

print(a + b)     # 13  (arithmetic)
print(a > b)     # True (comparison)
print(a > 5 and b < 5)  # True (logical)

fruits = ["seb", "kela", "anaar"]
print("seb" in fruits)  # True (membership)
```

---

## Control Flow

Control flow statements ਆਪਾਂ ਨੂੰ ਆਪਣੇ program ਦੇ flow ਨੂੰ certain conditions ਦੇ ਆਧਾਰ ਉੱਤੇ control ਕਰਨ ਦਿੰਦੇ ਹਨ।

ਕਈ ਵਾਰ ਆਪਾਂ ਕੋਈ code ਸਿਰਫ਼ ਤਾਂ execute ਕਰਨਾ ਚਾਹੁੰਦੇ ਹਾਂ ਜੇ ਕੋਈ condition ਪੂਰੀ ਹੋਵੇ।

ਉਦਾਹਰਨ ਲਈ - ਜੇ ਮੈਨੂੰ ਭੁੱਖ ਲੱਗੀ ਹੈ, ਤਾਂ ਮੈਂ ਖਾਣਾ ਖਾਵਾਂਗਾ।

ਇਹ Python ਵਿੱਚ ਇੰਝ ਲਿਖਿਆ ਜਾਂਦਾ ਹੈ:

```python
is_hungry = True
if is_hungry:
    print("I will eat food")
```

ਇੱਥੇ `is_hungry` ਦੀ value `True` ਹੈ, ਇਸ ਕਰਕੇ if statement ਦੇ ਅੰਦਰ ਵਾਲਾ code execute ਹੁੰਦਾ ਹੈ। ਜੇ `is_hungry` ਦੀ value `False` ਹੁੰਦੀ, ਤਾਂ if statement ਦੇ ਅੰਦਰ ਵਾਲਾ code execute ਨਹੀਂ ਹੁੰਦਾ। `is_hungry` ਦੀ value ਕਿਤੇ ਹੋਰ set ਹੋ ਰਹੀ ਆ ਇਸ code ਦੇ ਪਹੁੰਚਣ ਤੋਂ ਪਹਿਲਾਂ।

### If Statements

If statement ਆਪਾਂ ਨੂੰ ਇੱਕ block of code execute ਕਰਨ ਦਿੰਦਾ ਹੈ ਜੇ ਕੋਈ condition true ਹੋਵੇ।

```python
x = 10
if x > 5:
    print("x is greater than 5")
```

ਆਪਾਂ `if` ਨਾਲ `else` ਅਤੇ `elif` ਵੀ ਵਰਤ ਸਕਦੇ ਹਾਂ:

```python
marks = 75

if marks >= 90:
    print("Distinction")
elif marks >= 60:
    print("First class")
else:
    print("Try harder next time")
```

### Loops

Loops ਆਪਾਂ ਨੂੰ ਇੱਕੋ block of code ਨੂੰ ਕਈ ਵਾਰ execute ਕਰਨ ਦਿੰਦੇ ਹਨ। ਇਹ ਉਦੋਂ ਕੰਮ ਆਉਂਦੇ ਨੇ ਜਦੋਂ ਇੱਕੋ ਕੰਮ ਵਾਰ-ਵਾਰ ਕਰਨਾ ਹੋਵੇ — ਜਿਵੇਂ ਕਿਸੇ list ਦੀ ਹਰ item ਨੂੰ ਵੇਖਣਾ।

#### For Loop

For loop ਆਪਾਂ ਨੂੰ ਕਿਸੇ sequence (ਜਿਵੇਂ list ਜਾਂ string) ਉੱਤੇ iterate ਕਰਨ ਦਿੰਦਾ ਹੈ।

```python
my_list = [1, 2, 3, 4, 5]
for item in my_list:
    print(item)
```

#### While Loop

While loop ਆਪਾਂ ਨੂੰ ਉਦੋਂ ਤੱਕ code execute ਕਰਨ ਦਿੰਦਾ ਹੈ ਜਦੋਂ ਤੱਕ ਕੋਈ condition true ਹੈ।

```python
x = 0
while x < 5:
    print(x)
    x += 1
```

ਉੱਪਰਲੇ example ਵਿੱਚ, while loop ਉਦੋਂ ਤੱਕ execute ਹੁੰਦਾ ਰਹੇਗਾ ਜਦੋਂ ਤੱਕ `x` 5 ਤੋਂ ਘੱਟ ਹੈ। Loop ਦੇ ਅੰਦਰ ਆਪਾਂ `x` ਦੀ value print ਕਰਦੇ ਹਾਂ ਅਤੇ ਫਿਰ ਉਸ ਵਿੱਚ 1 ਜੋੜਦੇ ਹਾਂ। ਜਦੋਂ `x` 5 ਉੱਤੇ ਪਹੁੰਚਦਾ ਹੈ, ਤਾਂ condition false ਹੋ ਜਾਂਦੀ ਹੈ ਅਤੇ loop ਰੁੱਕ ਜਾਂਦਾ ਹੈ।

ਖਿਆਲ ਰੱਖੋ — while loop ਵਿੱਚ condition ਨੂੰ ਕਿਤੇ ਨਾ ਕਿਤੇ false ਹੋਣਾ ਚਾਹੀਦਾ, ਨਹੀਂ ਤਾਂ loop ਕਦੇ ਨਹੀਂ ਰੁਕੇਗਾ (ਇਸਨੂੰ infinite loop ਕਹਿੰਦੇ ਨੇ, ਅਤੇ ਇਹ program ਨੂੰ hang ਕਰ ਸਕਦਾ ਹੈ)।