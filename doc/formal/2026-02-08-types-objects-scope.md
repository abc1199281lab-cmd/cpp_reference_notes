# 2026-02-08-types-objects-scope

## 1. Types (型別)
C++ 的型別系統分為以下幾類：
- **Fundamental Types**: `int`, `char`, `float`, `double`, `bool`, `void` 等。
- **Compound Types**: 指標 (`*`), 引用 (`&`, `&&`), 陣列 (`[]`), 函式等。
- **User-defined Types**: `class`, `struct`, `union`, `enum`。
- **CV-qualifiers**: `const`, `volatile`。

## 2. Objects (物件)
在 C++ 中，物件是「一段具有屬性的記憶體區域」：
- **Lifetime**: 物件從構造完成到析構開始的區間。
- **Storage Duration**:
    - `static`: 程式執行期間。
    - `thread`: 執行緒執行期間。
    - `automatic`: 進入區塊到離開區塊（棧物件）。
    - `dynamic`: 透過 `new`/`malloc` 手動管理（堆物件）。
- **Alignment**: 物件在記憶體中的對齊要求。

## 3. Scope (作用域)
作用域決定了名稱（Name）的能見度：
- **Block Scope**: 函式內或 `{}` 內。
- **Function Scope**: 僅限於 `label`。
- **Namespace Scope**: 全域或 `namespace` 內。
- **Class Scope**: 類別定義內。
- **Enumeration Scope**: 列舉定義內。
- **Template Parameter Scope**: 模板參數。

## 4. Name Lookup (名稱查找)
當程式碼引用一個名稱時，編譯器會由內而外查找對應的聲明（Declaration），並考慮 ADL (Argument-Dependent Lookup) 等機制。

---
*Source: C++ Standard / ref/cppreference-doc*
