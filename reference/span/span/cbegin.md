# cbegin
* span[meta header]
* std[meta namespace]
* span[meta class]
* function[meta id-type]
* cpp23[meta cpp]

```cpp
constexpr const_iterator cbegin() const noexcept;
```
* const_iterator[link /reference/iterator/const_iterator.md.nolink]

## 概要
先頭要素を指す読み取り専用イテレータを取得する。


## 戻り値

```cpp
return begin();
```
* begin[link ./begin.md]


## 例外
投げない

## 例
```cpp example
#include <iostream>
#include <span>
#include <vector>

int main() {
  std::vector<int> v = {1, 2, 3, 4, 5};
  std::span<int, 5> sp{v};

  auto cit = sp.cbegin();

  std::cout << *cit << '\n';

  // これはできない
  // *cit = 0;
}
```
* cbegin()[color ff0000]

### 出力
```
1
```

## バージョン
### 言語
- C++23

### 処理系
- [Clang](/implementation.md#clang): ??
- [GCC](/implementation.md#gcc): 13.1
- [Visual C++](/implementation.md#visual_cpp): 2022 Update 6

## 参照
- [P2278R4 `cbegin` should always return a constant iterator](https://www.open-std.org/jtc1/sc22/wg21/docs/papers/2022/p2278r4.html)
