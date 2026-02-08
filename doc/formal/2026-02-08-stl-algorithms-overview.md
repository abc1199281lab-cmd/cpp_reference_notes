# 2026-02-08-stl-algorithms-overview

## 1. 演算法庫簡介 (`<algorithm>`)
C++ STL 提供了大量預定義的演算法，用於操作容器中的元素。這些演算法通常接受迭代器（Iterators）作為範圍。

## 2. 核心演算法分類

### 非修改型 (Non-modifying)
- **`std::find`**: 尋找特定值的元素。
- **`std::count`**: 計算特定值的出現次數。
- **`std::all_of`, `std::any_of`, `std::none_of`**: 檢查範圍是否符合條件。

### 修改型 (Modifying)
- **`std::copy` / `std::move`**: 複製或移動元素。
- **`std::transform`**: 對範圍內的每個元素應用函式並存儲結果。
- **`std::replace`**: 替換特定值的元素。

### 排序與相關操作 (Sorting)
- **`std::sort`**: 排序範圍（預設升冪）。
- **`std::stable_sort`**: 保持相等元素的相對順序。
- **`std::binary_search`**: 二分搜尋（需先排序）。

### 集合操作
- **`std::set_union`**, **`std::set_intersection`** 等。

## 3. Ranges (C++20)
C++20 引入了 `std::ranges`，使得演算法可以直接作用於容器，而不需要顯式傳遞 `begin()` 與 `end()`。
例如：`std::ranges::sort(my_vector);`

---
*Source: ref/cppreference-doc/en/cpp/algorithm/*
