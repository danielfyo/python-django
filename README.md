# python-django
E-commerce con Python+Django+Postgress SQL++Jenkings+Kafka+Rabbit MQ+TDD+DDD+Event Driven Architecture+EKL+APM+Sentry+Pronmetheus+Grafana

# 1. First stepes
## 1.1 Download the IDE
- To install Python, download the last versión from https://www.python.org/
- To Install a IDE [VS CODE](https://code.visualstudio.com/) / [PyCharm](https://www.jetbrains.com/pycharm/download)
# 2. Sintaxis
## 2.1. Data  types
In Python, we have several data types or structures that are fundamental in programming. These allow us to store and manipulate information.
### 2.1.1 Common Data Types
- **Lists**: `[]`
- **Tuples**: `()`
- **Dictionaries**: `{}`

### 2.1.2 Characteristics
- **Lists**:
  - Mutable
  - Ordered
  - Allow duplicates
- **Tuples**:
  - Immutable
  - Ordered
  - Allow duplicates
- **Dictionaries**:
  - Key-Value pairs
  - Keys are unique
  - Values can be repeated

### 2.1.3 Additional Types
- **Text**: `str`
  - Example: `"Python"`
- **Numbers**:
  - Integer (`int`)
    - Example: `250`
  - Float (`float`)
    - Example: `12.50`
- **Boolean**:
  - Examples: `True`, `False`

### 2.1.4 Sets
- Represented as `{}` (introduced in Python 3.7+ with certain considerations).

### 2.1.5 Notes
- Keys in dictionaries must be unique.
- Values in dictionaries can be repeated.

## 2.2 Best Practices for Naming Files, Variables, and Methods in Python

This guide provides the best practices for naming files, variables, and methods in Python, following the recommendations from **PEP 8**, Python’s official style guide.

---

### 2.2.1. Files (Modules)
- Use **lowercase with underscores**:
  - ✅ `my_script.py`
  - ✅ `process_data.py`
  - ❌ `MyScript.py`
  - ❌ `processData.py`
- Choose descriptive names that reflect the purpose of the file.
- Avoid generic names like `temp.py` or `script.py`.

---

### 2.2.2 Variables
- Use **`snake_case` (lowercase with underscores)**:
  - ✅ `total_sales`
  - ✅ `number_of_clients`
  - ❌ `totalSales`
  - ❌ `NumberOfClients`

- **Be descriptive but concise**:
  - ✅ `product_price`
  - ❌ `x` (unless in a clear context, like mathematical operations).
  - ❌ `the_product_price_is_high`.

- Avoid overwriting Python’s built-in names (e.g., `list`, `dict`, `str`):
  - ❌ `list = [1, 2, 3]`

---

### 2.2.3. Methods and Functions
- Use **`snake_case`**:
  - ✅ `calculate_total()`
  - ✅ `process_user_data()`
  - ❌ `calculateTotal()`
  - ❌ `ProcessData()`

- **Use clear names with verbs** to indicate actions:
  - ✅ `get_data()`
  - ✅ `save_file()`
  - ❌ `data()` (unclear).

- For private methods, prefix with an underscore (`_`):
  - ✅ `_private_method()`

---

### 2.2.4. Classes
- Use **`CamelCase`**:
  - ✅ `User`
  - ✅ `DataProcessor`
  - ❌ `user`
  - ❌ `data_processor`

---

### 2.2.5. Constants
- Use **`UPPERCASE_WITH_UNDERSCORES`**:
  - ✅ `MAX_CONNECTIONS = 10`
  - ✅ `PI = 3.14159`
  - ❌ `max_connections = 10`

---

### 2.2.6. Function Parameters and Arguments
- Follow the **`snake_case`** style:
  - ✅ `def calculate_total(unit_price, quantity):`
  - ❌ `def calculate_total(UnitPrice, Quantity):`

- Use meaningful and intuitive names for parameters.

---

### 2.2.7. Prefixes and Suffixes in Names
- Use prefixes like `is_`, `has_`, `can_` for boolean variables:
  - ✅ `is_active`
  - ✅ `has_error`
- Use suffixes to clarify context:
  - ✅ `user_id`
  - ✅ `file_path`

---

### 2.2.8. General Best Practices
- Avoid cryptic abbreviations:
  - ❌ `usrCnt` (use `user_count`).
- Be consistent:
  - If you use `total_sales`, don’t switch to `sales_total` elsewhere.
- Use short but descriptive names for temporary variables:
  - ✅ `x` in quick mathematical operations.
  - ✅ `i` for loop indices.
  - ❌ `dskj` (meaningless).

---

### 2.2.9. Complete Example

```python
# File name: calculate_total.py

class DataProcessor:
    MAX_CONNECTIONS = 5

    def __init__(self, user_id):
        self.user_id = user_id
        self.is_active = True

    def calculate_total(self, unit_price, quantity):
        total = unit_price * quantity
        return total

    def _private_method(self):
        pass

