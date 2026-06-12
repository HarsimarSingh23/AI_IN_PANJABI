# Python Fundamentals - Functions, Classes, Modules, Packages

ਹੁਣ ਆਪਾਂ ਉਹਨਾਂ fundamentals ਨੂੰ ਸਮਝਾਂਗੇ ਜੋ ਕਿਸੇ ਵੀ software ਦੀ ਨੀਂਹ ਹਨ:

- Functions
- Classes
- Modules
- Packages

---

## Functions

Functions ਉਹ ਮੁੜ-ਮੁੜ ਵਰਤਣ ਯੋਗ blocks of code ਹੁੰਦੇ ਹਨ ਜੋ ਕੋਈ ਖਾਸ ਕੰਮ ਕਰਦੇ ਹਨ। ਇਹਨਾਂ ਦੀ ਮਦਦ ਨਾਲ ਅਸੀਂ ਔਖੇ problems ਨੂੰ ਛੋਟੇ-ਛੋਟੇ ਹਿੱਸਿਆਂ ਵਿੱਚ ਵੰਡ ਸਕਦੇ ਹਾਂ। Functions input parameters ਲੈ ਸਕਦੇ ਨੇ ਅਤੇ output values ਵਾਪਸ ਕਰ ਸਕਦੇ ਨੇ।

Functions ਨੂੰ ਇੰਝ ਸਮਝੋ ਜਿਵੇਂ car ਦੇ ਵਿੱਚ engine ਹੁੰਦਾ ਹੈ, ਜਿਸ ਦਾ ਕੰਮ car ਨੂੰ ਚਲਾਉਣਾ ਹੁੰਦਾ ਹੈ। ਅਤੇ ਇਹੀ engine ਹੋਰ car ਦੇ ਵਿੱਚ ਵੀ ਵਰਤਿਆ ਜਾ ਸਕਦਾ ਹੈ — ਜਿਵੇਂ VW ਦਾ engine Audi ਦੇ ਵਿੱਚ ਵੀ ਵਰਤਿਆ ਜਾਂਦਾ ਹੈ। Functions ਦੀ ਮਦਦ ਨਾਲ ਅਸੀਂ ਆਪਣੇ code ਨੂੰ modular ਬਣਾ ਸਕਦੇ ਹਾਂ, ਜਿਸ ਨਾਲ code ਦੀ readability ਅਤੇ maintainability ਵਧ ਜਾਂਦੀ ਹੈ।

### ਇੱਕ practical example

ਮੰਨ ਲਓ ਆਪਾਂ ਤਿੰਨ ਖੇਤਾਂ ਦਾ ਖੇਤਰਫਲ (area) ਕੱਢ ਰਹੇ ਹਾਂ। ਹਰ ਖੇਤ ਗੋਲ ਹੈ, ਤੇ ਗੋਲ ਚੀਜ਼ ਦਾ ਖੇਤਰਫਲ ਕੱਢਣ ਦਾ ਫਾਰਮੂਲਾ ਹੁੰਦਾ ਹੈ:

**ਖੇਤਰਫਲ = ਪਾਈ × ਅਰਧਵਿਆਸ²**

- **ਅਰਧਵਿਆਸ (radius)** — ਖੇਤ ਦੇ ਵਿਚਕਾਰੋਂ ਲੈ ਕੇ ਕਿਨਾਰੇ ਤੱਕ ਦੀ ਦੂਰੀ।
- **ਪਾਈ (pi)** — ਇੱਕ ਪੱਕਾ number ਹੁੰਦਾ ਹੈ, 3.14, ਜੋ ਹਰ ਗੋਲ ਚੀਜ਼ ਲਈ ਇੱਕੋ ਜਿਹਾ ਰਹਿੰਦਾ ਹੈ।
- **`** 2`** — ਇਸ ਦਾ ਮਤਲਬ ਹੈ "ਵਰਗ" (square), ਯਾਨੀ ਅਰਧਵਿਆਸ ਨੂੰ ਆਪਣੇ ਆਪ ਨਾਲ ਗੁਣਾ ਕਰਨਾ।
- **`print()`** — ਜਵਾਬ ਨੂੰ screen ਉੱਤੇ ਦਿਖਾਉਂਦਾ ਹੈ।

### Function ਤੋਂ ਬਿਨਾਂ - ਇੱਕੋ ਹਿਸਾਬ ਵਾਰ-ਵਾਰ

```python
# ਪਹਿਲਾ ਖੇਤ
radius1 = 5
pi = 3.14
area1 = pi * (radius1 ** 2)
print(area1)

# ਦੂਜਾ ਖੇਤ
radius2 = 7
pi = 3.14
area2 = pi * (radius2 ** 2)
print(area2)

# ਤੀਜਾ ਖੇਤ
radius3 = 10
pi = 3.14
area3 = pi * (radius3 ** 2)
print(area3)
```

### Function ਨਾਲ - ਸੌਖਾ ਅਤੇ ਸਾਫ਼

```python
# ਖੇਤਰਫਲ ਕੱਢਣ ਵਾਲੀ ਮਸ਼ੀਨ (function) ਬਣਾਈ
def calculate_area(radius):
    pi = 3.14
    area = pi * (radius ** 2)
    return area

# ਹੁਣ ਸਿਰਫ਼ radius ਦਿਓ, ਖੇਤਰਫਲ ਲਓ
print(calculate_area(5))   # ਪਹਿਲਾ ਖੇਤ
print(calculate_area(7))   # ਦੂਜਾ ਖੇਤ
print(calculate_area(10))  # ਤੀਜਾ ਖੇਤ
```

### ਵਿਆਖਿਆ (Explanation)

- **`def calculate_area(radius):`** — ਇੱਥੇ ਅਸੀਂ ਇੱਕ ਮਸ਼ੀਨ (function) ਬਣਾਈ ਜਿਸ ਦਾ ਨਾਂ ਹੈ `calculate_area`।
- **`def`** ਦਾ ਮਤਲਬ ਹੈ "ਮਸ਼ੀਨ ਬਣਾਓ"।
- **`(radius)`** — ਇਹ ਉਹ ਚੀਜ਼ ਹੈ ਜੋ ਅਸੀਂ ਮਸ਼ੀਨ ਵਿੱਚ ਪਾਉਂਦੇ ਹਾਂ (ਜਿਵੇਂ ਟੋਕੇ ਵਿੱਚ ਹਰਾ ਚਾਰਾ)।
- **`return area`** — ਇਹ ਉਹ ਜਵਾਬ ਹੈ ਜੋ ਮਸ਼ੀਨ ਵਾਪਸ ਦਿੰਦੀ ਹੈ (ਕੱਟਿਆ ਹੋਇਆ ਚਾਰਾ ਬਾਹਰ)।
- **`calculate_area(5)`** — ਮਸ਼ੀਨ ਨੂੰ ਚਲਾਉਣਾ, 5 ਦੇ ਕੇ। ਹਰ ਵਾਰ ਵੱਖਰਾ number ਦਿਓ, ਹਰ ਵਾਰ ਸਹੀ ਜਵਾਬ ਮਿਲੂ।

### ਮੁੱਖ ਫ਼ਾਇਦਾ

- ਪਹਿਲਾਂ ਹਰ ਖੇਤ ਲਈ `pi * (radius ** 2)` ਵਾਲਾ ਹਿਸਾਬ ਵਾਰ-ਵਾਰ ਲਿਖਣਾ ਪੈਂਦਾ ਸੀ।
- ਹੁਣ ਉਹ ਹਿਸਾਬ ਸਿਰਫ਼ ਇੱਕ ਵਾਰ ਮਸ਼ੀਨ ਅੰਦਰ ਲਿਖਿਆ, ਤੇ 100 ਖੇਤ ਹੋਣ ਜਾਂ 1000 — ਬੱਸ number ਬਦਲ ਕੇ ਮਸ਼ੀਨ ਚਲਾ ਦਿਓ।
- ਜੇ ਕਦੇ ਫਾਰਮੂਲਾ ਬਦਲਣਾ ਹੋਵੇ, ਤਾਂ ਸਿਰਫ਼ ਇੱਕੋ ਥਾਂ ਠੀਕ ਕਰੋ — ਸਾਰੀਆਂ ਥਾਵਾਂ ਆਪੇ ਠੀਕ ਹੋ ਜਾਣਗੀਆਂ।

---

## Classes

Class ਇੱਕ ਫਾਰਮ (ਜਾਂ ਸਾਂਚਾ) ਵਰਗੀ ਹੁੰਦੀ ਹੈ। Class ਆਪਾਂ ਉਦੋਂ ਵਰਤਦੇ ਆਂ ਜਦੋਂ ਸਾਨੂੰ ਇੱਕੋ ਕਿਸਮ ਦੀਆਂ ਚੀਜ਼ਾਂ ਚਾਹੀਦੀਆਂ ਨੇ, ਪਰ ਹਰ ਚੀਜ਼ ਦੀਆਂ properties ਵੱਖ-ਵੱਖ ਹੁੰਦੀਆਂ ਨੇ।

ਜਿਵੇਂ ਪਟਵਾਰੀ ਕੋਲ "ਖੇਤ ਰਜਿਸਟਰੀ ਫਾਰਮ" ਹੁੰਦਾ ਹੈ ਜਿਸ ਵਿੱਚ ਖ਼ਾਲੀ ਥਾਂਵਾਂ ਹੁੰਦੀਆਂ ਨੇ: ਮਾਲਕ ਦਾ ਨਾਂ, ਅਰਧਵਿਆਸ, ਫ਼ਸਲ। ਹਰ ਨਵੇਂ ਖੇਤ ਲਈ ਇੱਕ ਨਵਾਂ ਫਾਰਮ ਭਰ ਲਈਦਾ ਹੈ। ਉਹ ਭਰਿਆ ਹੋਇਆ ਫਾਰਮ = **object**।

ਅਤੇ ਇਹ ਫਾਰਮ ਆਪਣਾ ਖੇਤਰਫਲ ਆਪ ਕੱਢਣਾ ਵੀ ਜਾਣਦਾ ਹੈ। ਇਸ ਨੂੰ ਪਤਾ ਹੈ ਕਿ ਫਾਰਮ ਵਿੱਚ ਕੀ-ਕੀ ਪਾਇਆ ਹੋਇਆ ਹੈ ਅਤੇ ਉਸ ਦੇ ਹਿਸਾਬ ਨਾਲ ਹੋਰ ਕੀ-ਕੀ ਜਾਣਕਾਰੀ ਅਸੀਂ ਕੱਢ ਸਕਦੇ ਹਾਂ।

### Class ਤੋਂ ਬਿਨਾਂ - ਖਿੱਲਰੇ-ਪੁੱਲਰੇ variables

```python
# ਪਹਿਲੇ ਖੇਤ ਦੀ ਜਾਣਕਾਰੀ
owner1 = "Jagtar"
radius1 = 5
crop1 = "Wheat"

# ਦੂਜੇ ਖੇਤ ਦੀ ਜਾਣਕਾਰੀ
owner2 = "Balwinder"
radius2 = 7
crop2 = "Rice"

def calculate_area(radius):
    return 3.14 * (radius ** 2)

print(owner1, crop1, calculate_area(radius1))
print(owner2, crop2, calculate_area(radius2))
```

**ਦਿੱਕਤ:** `owner1`, `radius1`, `crop1` — ਇਹ ਤਿੰਨੇ ਇੱਕੋ ਖੇਤ ਦੇ ਨੇ, ਪਰ ਆਪਸ ਵਿੱਚ ਕਿਤੇ ਜੁੜੇ ਹੋਏ ਨਹੀਂ — ਸਿਰਫ਼ ਨਾਂ ਦੇ ਅਖ਼ੀਰ ਵਾਲੇ "1" ਨਾਲ। 50 ਖੇਤ ਹੋਣ ਤਾਂ 150 variables ਖਿੱਲਰ ਜਾਣਗੇ ਤੇ ਰਲ਼ਗੱਡ ਹੋਣ ਦਾ ਡਰ ਰਹਿੰਦਾ ਹੈ।

### Class ਨਾਲ - ਸਾਫ਼-ਸੁਥਰਾ structure

```python
class Field:
    def __init__(self, owner, radius, crop):
        self.owner = owner
        self.radius = radius
        self.crop = crop

    def calculate_area(self):
        pi = 3.14
        return pi * (self.radius ** 2)

# ਖੇਤ ਬਣਾਏ (objects) — ਫਾਰਮ ਭਰੇ
field1 = Field("Jagtar", 5, "Wheat")
field2 = Field("Balwinder", 7, "Rice")

print(field1.owner, field1.crop, field1.calculate_area())
print(field2.owner, field2.crop, field2.calculate_area())
```

### ਵਿਆਖਿਆ (Explanation)

- **`class Field:`** — ਇਹ ਫਾਰਮ/ਸਾਂਚੇ ਦਾ design ਬਣਾਉਂਦਾ ਹੈ। ਇੱਕ ਵਾਰ ਬਣਾਓ, ਜਿੰਨੇ ਮਰਜ਼ੀ ਖੇਤ ਬਣਾਓ।
- **`__init__`** — ਇਹ ਉਹ ਹਿੱਸਾ ਹੈ ਜੋ ਨਵਾਂ ਖੇਤ ਬਣਾਉਣ ਵੇਲੇ ਫਾਰਮ ਦੀਆਂ ਖ਼ਾਲੀ ਥਾਂਵਾਂ ਭਰਦਾ ਹੈ (owner, radius, crop)।
- **`self`** — ਇਸ ਦਾ ਮਤਲਬ ਹੈ "ਇਹੀ ਖੇਤ, ਆਪਣਾ ਆਪ"। `self.owner` ਯਾਨੀ ਇਸ ਖ਼ਾਸ ਖੇਤ ਦਾ owner — ਦੂਜੇ ਖੇਤ ਨਾਲ ਨਹੀਂ ਰਲ਼ਦਾ।
- **`field1 = Field("Jagtar", 5, "Wheat")`** — ਇੱਕ ਨਵਾਂ ਖੇਤ object ਬਣਾਇਆ, ਯਾਨੀ ਫਾਰਮ ਭਰਿਆ।
- **`field1.calculate_area()`** — ਖੇਤ ਨੂੰ ਕਿਹਾ "ਆਪਣਾ ਖੇਤਰਫਲ ਆਪ ਦੱਸ"। ਉਸਨੂੰ radius ਦੁਬਾਰਾ ਦੱਸਣ ਦੀ ਲੋੜ ਨਹੀਂ — ਉਹ ਆਪਣੇ ਅੰਦਰ ਪਹਿਲਾਂ ਹੀ ਰੱਖਦਾ ਹੈ।

### Class ਦੇ ਵਿੱਚ ਹੋਰ functions ਵੀ ਪਾ ਸਕਦੇ ਆਂ

```python
class Field:
    def __init__(self, owner, radius, crop):
        self.owner = owner
        self.radius = radius
        self.crop = crop

    def calculate_area(self):
        pi = 3.14
        return pi * (self.radius ** 2)

    def print_info(self):
        print(f"Owner: {self.owner}, Crop: {self.crop}, Area: {self.calculate_area()}")

# ਖੇਤ ਬਣਾਏ (objects) — ਫਾਰਮ ਭਰੇ
field1 = Field("Jagtar", 5, "Wheat")
field2 = Field("Balwinder", 7, "Rice")

field1.print_info()
field2.print_info()
```

ਹੁਣ ਅਸੀਂ ਇਸ ਦੇ ਵਿੱਚ ਇੱਕ function ਜੋੜਿਆ — `print_info` — ਜੋ ਸਾਨੂੰ ਦੱਸਦਾ ਹੈ ਕਿ ਇਸ ਖੇਤ ਦੇ owner ਦਾ ਨਾਮ ਕੀ ਹੈ, ਉਸ ਦੇ ਵਿੱਚ ਕੀ crop ਹੈ ਅਤੇ ਉਸ ਦਾ ਖੇਤਰਫਲ ਕੀ ਹੈ। ਅਸੀਂ ਇਸ function ਨੂੰ call ਕਰਕੇ ਆਪਣੇ ਖੇਤ ਦੀ ਸਾਰੀ ਜਾਣਕਾਰੀ ਇੱਕ ਹੀ ਵਾਰ print ਕਰਵਾ ਸਕਦੇ ਹਾਂ।

---

## Modules

ਹੁਣ ਜਦੋਂ ਅਸੀਂ program ਲਿਖਦੇ ਆਂ ਤਾਂ ਅਸੀਂ ਜਾਂ ਤਾਂ ਪੂਰਾ code ਇੱਕੋ file ਵਿੱਚ ਲਿਖ ਸਕਦੇ ਆਂ, ਜਾਂ code ਨੂੰ ਵੱਖ-ਵੱਖ files ਵਿੱਚ ਲਿਖ ਕੇ ਉਸ ਨੂੰ ਇਕੱਠੇ ਕਰ ਸਕਦੇ ਆਂ।

Module ਕੁਝ ਨਹੀਂ ਹੁੰਦਾ — ਬੱਸ ਇੱਕੋ ਤਰ੍ਹਾਂ ਦੇ ਕੰਮ ਕਰਨ ਵਾਲੇ functions ਨੂੰ ਇੱਕ ਜਗ੍ਹਾ ਇਕੱਠਾ ਕਰ ਲੈਂਦੇ ਆਂ ਅਤੇ ਉਸ ਨੂੰ ਆਪਣੇ code ਦੇ ਵਿੱਚ ਵਰਤਦੇ ਆਂ।

### Module ਨਾਲ — ਕੰਮ ਨੂੰ ਦੋ files ਵਿੱਚ ਵੰਡਿਆ

**File 1 — `field_calc.py`** (ਇਹ ਸਾਂਝੀ ਮਸ਼ੀਨ / module):

```python
class Field:
    def __init__(self, owner, radius, crop):
        self.owner = owner
        self.radius = radius
        self.crop = crop

    def calculate_area(self):
        return 3.14 * (self.radius ** 2)
```

**File 2 — `main.py`** (ਇੱਥੇ ਮਸ਼ੀਨ ਨੂੰ ਬੁਲਾਇਆ):

```python
import field_calc          # ਮਸ਼ੀਨ ਬੁਲਾਈ

field1 = field_calc.Field("Jagtar", 5, "Wheat")
field2 = field_calc.Field("Balwinder", 7, "Rice")

print(field1.owner, field1.crop, field1.calculate_area())
print(field2.owner, field2.crop, field2.calculate_area())
```

### ਵਿਆਖਿਆ (Explanation)

- **`import field_calc`** — Python ਨੂੰ ਕਿਹਾ ਕਿ `field_calc.py` ਨਾਮ ਦੀ file ਵਿੱਚੋਂ ਸਾਰਾ code ਮੇਰੇ program ਵਿੱਚ ਲੈ ਆ।
- **`field_calc.Field(...)`** — module ਦੇ ਅੰਦਰੋਂ `Field` class ਨੂੰ ਵਰਤਿਆ। ਨਾਮ ਤੋਂ ਪਹਿਲਾਂ `field_calc.` ਲਾਉਣਾ ਪੈਂਦਾ ਹੈ ਤਾਂ ਜੋ Python ਨੂੰ ਪਤਾ ਲੱਗੇ ਕਿ ਇਹ ਉਸੇ module ਵਿੱਚੋਂ ਹੈ।
- ਫ਼ਾਇਦਾ: main.py ਛੋਟਾ ਤੇ ਸਾਫ਼ ਰਹਿੰਦਾ ਹੈ। ਖੇਤ ਦਾ ਸਾਰਾ ਹਿਸਾਬ ਅਲੱਗ file ਵਿੱਚ ਹੈ — ਜੇ ਕੱਲ੍ਹ ਨੂੰ ਫਾਰਮੂਲਾ ਬਦਲਣਾ ਹੋਵੇ ਤਾਂ ਸਿਰਫ਼ ਇੱਕ ਥਾਂ ਠੀਕ ਕਰਨਾ ਪਵੇਗਾ।

---

## Packages

Package modules ਤੋਂ ਇੱਕ ਕਦਮ ਅੱਗੇ ਹੈ।

ਜੇ module ਇੱਕ ਮਸ਼ੀਨ ਸੀ, ਤਾਂ package ਇੱਕ ਪੂਰਾ store/ਅਲਮਾਰੀ (ਗੋਦਾਮ) ਹੈ ਜਿਸ ਵਿੱਚ ਕਈ ਮਸ਼ੀਨਾਂ ਸਜਾ ਕੇ ਰੱਖੀਆਂ ਹੁੰਦੀਆਂ ਨੇ। ਜਿਵੇਂ ਖੇਤੀ ਦੇ store ਵਿੱਚ ਇੱਕ ਪਾਸੇ ਏਰੀਆ ਨਾਪਣ ਵਾਲੀ ਮਸ਼ੀਨ, ਦੂਜੇ ਪਾਸੇ ਬੀਜ ਤੋਲਣ ਵਾਲੀ — ਸਭ ਇੱਕੋ ਥਾਂ, ਸਾਫ਼ ਵੰਡੀਆਂ ਹੋਈਆਂ।

**Package = ਕਈ modules ਦਾ ਇੱਕ ਇਕੱਠ।**

### Package ਦਾ ਢਾਂਚਾ (structure)

`farming` ਇੱਕ folder ਹੈ ਜਿਸ ਦੇ ਅੰਦਰ 3 files ਨੇ। ਹਰ company ਇੱਕ package ਬਣਾ ਕੇ ਉਸ ਨੂੰ use ਕਰਦੀ ਹੈ।

```
farming/                  ← package (ਇੱਕ folder)
├── __init__.py           ← ਇਹ ਦੱਸਦੀ ਹੈ "ਇਹ folder package ਹੈ"
├── field_calc.py         ← module 1 (ਏਰੀਆ ਵਾਲੀ ਮਸ਼ੀਨ)
└── crop_calc.py          ← module 2 (ਬੀਜ ਵਾਲੀ ਮਸ਼ੀਨ)

main.py                   ← ਇੱਥੋਂ package ਨੂੰ ਵਰਤਿਆ
```

### `main.py` ਵਿੱਚ package ਵਰਤਣਾ

```python
from farming import field_calc, crop_calc   # store ਵਿੱਚੋਂ ਦੋ ਮਸ਼ੀਨਾਂ ਚੁੱਕੀਆਂ

field1 = field_calc.Field("Jagtar", 5, "Wheat")
area = field1.calculate_area()
seeds = crop_calc.seeds_required(area)

print(field1.owner, "ਦੇ ਖੇਤ ਦਾ ਏਰੀਆ:", area)
print(field1.owner, "ਨੂੰ", seeds, "ਕਿਲੋ ਬੀਜ ਚਾਹੀਦਾ")
```

### ਵਿਆਖਿਆ (Explanation)

- **package** = ਇੱਕ folder ਜਿਸ ਵਿੱਚ ਕਈ modules (`.py` files) ਇਕੱਠੀਆਂ ਰੱਖੀਆਂ ਹੁੰਦੀਆਂ ਨੇ।
- **`__init__.py`** = ਇਹ ਖ਼ਾਸ file folder ਉੱਤੇ ਲੱਗੀ ਨਾਮ-ਪਲੇਟ ਵਰਗੀ ਹੈ — ਇਹ Python ਨੂੰ ਦੱਸਦੀ ਹੈ ਕਿ "ਇਹ ਸਿਰਫ਼ ਆਮ folder ਨਹੀਂ, ਇਹ ਅਸਲੀ package ਹੈ"। ਇਹ ਖ਼ਾਲੀ ਵੀ ਹੋ ਸਕਦੀ ਹੈ।
- **`from farming import field_calc`** = "farming store ਵਿੱਚੋਂ field_calc ਮਸ਼ੀਨ ਕੱਢੋ"।
- ਇੱਕ ਵੱਡੇ project ਦਾ ਸਾਰਾ code ਵਿਸ਼ੇ ਮੁਤਾਬਕ ਵੱਖ-ਵੱਖ modules ਵਿੱਚ ਵੰਡ ਕੇ, ਇੱਕ package ਹੇਠ ਸਜਾ ਲਈਦਾ ਹੈ।

---

## ਕਿਸੇ ਹੋਰ ਦਾ ਬਣਾਇਆ Package ਵਰਤਣਾ - `pip install`

ਜਦੋਂ package ਕਿਸੇ ਹੋਰ ਨੇ ਬਣਾਇਆ ਹੋਵੇ, ਤਾਂ ਉਹ ਘਰ ਲਿਆਉਣ ਲਈ `pip install` ਵਰਤੀਦਾ ਹੈ। ਜਿਵੇਂ ਇੱਕ famous package ਹੈ **numpy** ਜੋ ਕਾਫ਼ੀ data analysis ਵਿੱਚ use ਕੀਤਾ ਜਾਂਦਾ ਹੈ।

ਕਿਵੇਂ install ਕਰੀਏ (ਇਹ Python ਦੇ ਅੰਦਰ ਨਹੀਂ, ਸਗੋਂ terminal/command line ਵਿੱਚ ਲਿਖੀਦਾ ਹੈ):

```bash
pip install numpy
```

Install ਹੁੰਦੇ ਵੇਲੇ pip ਇਹ ਦਿਖਾਉਂਦਾ ਹੈ:

```
Downloading numpy-2.4.4 ...
Successfully installed numpy-2.4.4     ← ਮਸ਼ੀਨ ਘਰ ਆ ਗਈ ✅
```

ਜੇ ਮਸ਼ੀਨ ਪਹਿਲਾਂ ਤੋਂ ਮੌਜੂਦ ਹੋਵੇ, ਤਾਂ pip ਕਹਿੰਦਾ ਹੈ:

```
Requirement already satisfied      ← ਪਹਿਲਾਂ ਤੋਂ ਪਈ ਹੈ, ਦੁਬਾਰਾ ਲਿਆਉਣ ਦੀ ਲੋੜ ਨਹੀਂ
```

### Install ਕਰਨ ਤੋਂ ਬਾਅਦ ਵਰਤੋਂ

ਹੁਣ ਆਪਣੇ ਬਣਾਏ package ਵਾਂਗ ਹੀ import ਕਰੋ:

```python
import numpy

radius = 5
area = numpy.pi * (radius ** 2)   # ਆਪਣੀ 3.14 ਦੀ ਥਾਂ numpy ਦੀ ਪੂਰੀ pi
print(area)
```

### ਵਿਆਖਿਆ (Explanation)

- **PyPI** = online ਮੰਡੀ (pypi.org) ਜਿੱਥੇ ਲੱਖਾਂ ਮੁਫ਼ਤ packages ਪਏ ਨੇ।
- **`pip install <ਨਾਂ>`** = ਉਸ ਮੰਡੀ ਵਿੱਚੋਂ package download ਕਰਕੇ ਆਪਣੇ computer ਉੱਤੇ ਲਾਉਣਾ। ਇਹ ਸਿਰਫ਼ ਇੱਕ ਵਾਰ ਕਰਨਾ ਪੈਂਦਾ ਹੈ।
- ਇੱਕ ਵਾਰ install ਹੋ ਜਾਵੇ, ਫੇਰ ਜਿੰਨੇ ਮਰਜ਼ੀ programs ਵਿੱਚ ਬੱਸ import ਕਰੋ — ਦੁਬਾਰਾ install ਨਹੀਂ ਕਰਨਾ ਪੈਂਦਾ।

### ਕੁਝ ਆਮ ਵਰਤੇ ਜਾਣ ਵਾਲੇ packages

- **numpy** — ਹਿਸਾਬ-ਕਿਤਾਬ
- **pandas** — data/tables
- **requests** — internet ਤੋਂ data ਲੈਣਾ
- **matplotlib** — graphs