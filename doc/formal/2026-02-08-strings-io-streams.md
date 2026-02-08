# 2026-02-08-strings-io-streams

## 1. Strings (字串)
C++ 提供了一套強大的字串處理工具，主要位於 `<string>` 與 `<string_view>`。

- **`std::string`**: 可變長度的字元序列，負責記憶體管理。
- **`std::string_view` (C++17)**: 非擁有性的字串參考，用於高效的唯讀字串處理（避免不必要的拷貝）。
- **`std::wstring`, `std::u16string`, `std::u32string`**: 支援不同的字元編碼。

## 2. Input/Output Streams (輸入輸出流)
C++ 的 I/O 系統是基於串流（Stream）類別階層建立的。

- **`std::iostream`**: 基礎 I/O，包含 `std::cin`, `std::cout`, `std::cerr`, `std::clog`。
- **`std::fstream`**: 檔案 I/O，支援讀取 (`std::ifstream`) 與寫入 (`std::ofstream`)。
- **`std::sstream`**: 字串 I/O，允許將字串視為串流進行格式化。

## 3. Formatted Output (C++20/23)
- **`std::format` (C++20)**: 提供類 Python 的格式化字串功能。
- **`std::print` (C++23)**: 結合了 `std::format` 與高效輸出的新標準。

---
*Source: ref/cppreference-doc/en/cpp/string/ & ref/cppreference-doc/en/cpp/io/*
