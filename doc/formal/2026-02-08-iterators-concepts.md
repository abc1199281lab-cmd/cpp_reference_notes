# 2026-02-08-iterators-concepts

## 1. Iterators (迭代器) 簡介
迭代器是連接容器與演算法的橋樑。它提供了一種統一的方法來訪問容器中的元素，而無需暴露容器的內部表示。

## 2. 迭代器分類 (Iterator Categories)
根據支援的操作，迭代器分為以下幾類：
- **Input Iterator**: 僅支援單向讀取。
- **Output Iterator**: 僅支援單向寫入。
- **Forward Iterator**: 支援多次讀取與寫入，僅限單向。
- **Bidirectional Iterator**: 支援雙向移動（如 `std::list`）。
- **Random Access Iterator**: 支援 $O(1)$ 隨機跳轉（如 `std::vector`, `std::array`）。
- **Contiguous Iterator (C++17)**: 保證元素在記憶體中連續存放。

## 3. 關鍵操作
- `*it`: 解引用。
- `++it` / `--it`: 移動。
- `it + n`: 隨機跳轉（僅限隨機訪問迭代器）。

## 4. 特殊迭代器
- **Insert Iterators**: 如 `std::back_inserter`，用於自動擴展容器。
- **Stream Iterators**: 如 `std::istream_iterator`，將串流視為容器。

---
*Source: ref/cppreference-doc/en/cpp/iterator/*
