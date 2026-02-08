# 2026-02-08-stl-containers-overview

## 1. Sequence Containers (序列容器)
按線性順序存儲元素：
- **`std::vector`**: 動態陣列。支援快速隨機存取，末尾插入/刪除效率高。
- **`std::deque`**: 雙端佇列。兩端插入/刪除均為 $O(1)$，支援隨機存取。
- **`std::list`**: 雙向鏈結串列。支援任意位置 $O(1)$ 插入/刪除，不支援隨機存取。
- **`std::forward_list`**: 單向鏈結串列。節省空間，僅支援單向迭代。
- **`std::array` (C++11)**: 固定長度陣列。靜態分配，無額外開銷。

## 2. Associative Containers (關聯容器)
基於紅黑樹（Red-Black Tree）實現，元素自動排序：
- **`std::set` / `std::multiset`**: 儲存唯一/非唯一鍵。
- **`std::map` / `std::multimap`**: 儲存鍵值對（Key-Value pairs）。

## 3. Unordered Associative Containers (無序關聯容器)
基於雜湊表（Hash Table）實現，平均 $O(1)$ 查找：
- **`std::unordered_set` / `std::unordered_map`** 等。

## 4. Container Adapters (容器配接器)
提供特定接口的包裝：
- **`std::stack`**: LIFO (後進先出)。
- **`std::queue`**: FIFO (先進先出)。
- **`std::priority_queue`**: 優先權佇列。

---
*Source: ref/cppreference-doc/en/cpp/container/*
