# 2026-02-08-cpp-standards-overview

## C++ 標準演進簡介
C++ 自 1998 年標準化以來，經歷了多次重大更新。現代 C++（Modern C++）通常指 C++11 及其之後的版本。

### 主要版本特性
- **C++11 (The Big Leap)**:
    - Auto 型別推導
    - Lambda 表達式
    - 右值引用與移動語義 (Move Semantics)
    - 智慧指標 (`std::unique_ptr`, `std::shared_ptr`)
- **C++14**:
    - 泛型 Lambda
    - `constexpr` 限制放寬
- **C++17**:
    - `std::optional`, `std::variant`, `std::any`
    - 結構化綁定 (Structured Bindings)
    - `if constexpr`
- **C++20 (The Revolution)**:
    - Concepts (約束與概念)
    - Ranges (範圍庫)
    - Modules (模組化)
    - Coroutines (協程)
- **C++23**:
    - `std::expected`
    - `std::print` (類 Python/Rust 的格式化輸出)

## 學習與文件導覽
所有的深入分析將基於 `ref/cppreference-doc` 中的 HTML 文件，涵蓋 `std` 命名空間下的核心函式庫。

---
*Source: ref/cppreference-doc*
