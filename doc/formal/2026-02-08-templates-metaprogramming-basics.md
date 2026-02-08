# 2026-02-08-templates-metaprogramming-basics

## 1. Templates (模板)
模板是 C++ 實現泛型程式設計（Generic Programming）的核心工具，允許在不指定具體型別的情況下定義函式與類別。

### 函式模板 (Function Templates)
`template <typename T> T add(T a, T b) { return a + b; }`

### 類別模板 (Class Templates)
`template <typename T> class Box { T value; };`

## 2. Template Specialization (模板特化)
- **Full Specialization**: 為特定型別提供完整的定義。
- **Partial Specialization**: 僅為類別模板的部分參數或特定情況（如指標）提供定義。

## 3. Template Metaprogramming (TMP)
在編譯期執行計算的技術。
- **`std::conditional`**: 編譯期 `if-else`。
- **`std::enable_if` (C++11)**: 基於 SFINAE (Substitution Failure Is Not An Error) 的條件編譯。
- **Variadic Templates (C++11)**: 支援任意數量的模板參數。

## 4. Concepts & Constraints (C++20)
顯式定義模板參數必須滿足的條件，提高程式碼的可讀性與編譯錯誤的易懂度。
`template <std::integral T> void process(T t);`

---
*Source: ref/cppreference-doc/en/cpp/language/templates*
