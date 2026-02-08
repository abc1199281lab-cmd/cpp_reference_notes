# 2026-02-08-functions-lambda-expressions

## 1. Functions (函式)
C++ 函式的核心組成：
- **Declaration & Definition**: 宣告與定義的分離。
- **Parameters**: 
    - Pass-by-value
    - Pass-by-reference (`&`)
    - Pass-by-pointer (`*`)
- **Return Type**: 支援 `auto` 推導（C++14）。
- **Overloading**: 同名但參數列表不同。
- **Inline Functions**: 建議編譯器展開程式碼以優化效能。

## 2. Lambda Expressions (Lambda 表達式)
C++11 引入的匿名函式，語法如下：
`[capture-list] (params) -> return-type { body }`

### Capture List (捕獲清單)：
- `[]`: 不捕獲任何變數。
- `[&]`: 以引用方式捕獲所有外部變數。
- `[=]`: 以數值（拷貝）方式捕獲所有外部變數。
- `[x, &y]`: 特定變數捕獲。
- `[this]`: 捕獲當前物件指標。

### 進階特性：
- **Generic Lambdas (C++14)**: 參數可使用 `auto`。
- **Capture with Initializers (C++14)**: 支援移動語義捕獲，例如 `[p = std::move(ptr)]`。
- **Constexpr Lambdas (C++17)**。

## 3. Function Objects (Functors)
重載了 `operator()` 的類別物件，Lambda 在編譯時會被轉換為類似 Functor 的結構。

---
*Source: ref/cppreference-doc/en/cpp/language/functions*
