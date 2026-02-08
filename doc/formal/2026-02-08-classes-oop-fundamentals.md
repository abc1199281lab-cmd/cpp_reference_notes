# 2026-02-08-classes-oop-fundamentals

## 1. Class & Struct (類別與結構)
在 C++ 中，`class` 與 `struct` 的唯一區別是預設的存取權限：
- **`struct`**: 預設為 `public`。
- **`class`**: 預設為 `private`。

## 2. Access Specifiers (存取限定符)
- **`public`**: 任何地方皆可存取。
- **`protected`**: 僅類別本身與衍生類別可存取。
- **`private`**: 僅類別內部可存取。

## 3. Special Member Functions (特殊成員函式)
編譯器在需要時會自動生成的函式：
- **Default Constructor**: 預設構造函式。
- **Destructor**: 析構函式。
- **Copy Constructor / Assignment**: 拷貝構造與賦值。
- **Move Constructor / Assignment (C++11)**: 移動構造與賦值。

## 4. Inheritance & Polymorphism (繼承與多載)
- **Inheritance**: 支援單一與多重繼承。
- **Virtual Functions**: 使用 `virtual` 關鍵字實現動態綁定。
- **Override & Final (C++11)**: 顯式標記覆寫與禁止繼承/覆寫。
- **Abstract Classes**: 包含純虛擬函式 (`= 0`) 的類別。

---
*Source: ref/cppreference-doc/en/cpp/language/classes*
