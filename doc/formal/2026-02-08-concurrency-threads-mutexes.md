# 2026-02-08-concurrency-threads-mutexes

## 1. C++ 並行程式設計概論
C++11 引入了標準執行緒庫，讓開發者能夠撰寫跨平台的並行程式。隨著標準演進（C++17/20），處理並發任務變得更加安全與簡潔。

## 2. 執行緒管理 (Threads)

### `std::thread` (C++11)
- 最基礎的執行緒類別。
- 需要手動呼叫 `join()`（等待結束）或 `detach()`（背景執行），否則解構時會導致程式崩潰。

### `std::jthread` (C++20)
- **自動 Join**：解構時會自動嘗試 join。
- **停止請求 (Stop Token)**：內建支援協同式停止請求，透過 `std::stop_token` 可以在不強制殺死執行緒的情況下優雅地結束任務。

## 3. 執行緒同步 (Synchronization)

### Mutex (互斥鎖)
- **`std::mutex`**: 基本鎖，確保同一時間只有一個執行緒存取資源。
- **`std::recursive_mutex`**: 允許同一執行緒多次加鎖。
- **`std::shared_mutex` (C++17)**: 實現「讀寫鎖」（Read-Write Lock），允許多個讀者或單個寫者。

### Lock Guards (RAII 鎖管理)
- **`std::lock_guard`**: 簡單的 RAII 鎖，不可手動解鎖。
- **`std::unique_lock`**: 靈活的鎖，支援手動解鎖、延遲加鎖。
- **`std::scoped_lock` (C++17)**: 支援同時鎖定多個 Mutex，有效防止死鎖（Deadlock）。

## 4. 非同步任務 (Asynchronous Tasks)
- **`std::async`**: 以非同步方式執行函式，回傳 `std::future`。
- **`std::future` / `std::promise`**: 用於在執行緒之間傳遞回傳值或異常。
- **`std::condition_variable`**: 用於執行緒間的等待與通知機制。

## 5. 原子操作 (Atomics)
- **`std::atomic<T>`**: 提供無鎖（Lock-free）的原子操作，適用於高性能的計數器或旗標，避免了 Mutex 的開銷。

---
*Source: ref/cppreference-doc/en/cpp/thread/*
