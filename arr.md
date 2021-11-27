## 配列について

```cpp
int x[5] = {0, 1, 2, 3, 4};
int y = x[2];  // 2

int x[5];

x[0] = 0;
x[1] = 1;
x[2] = 2;
x[3] = 3;
// 指定しない場合、x[4] == 0
```

配列は暗黙的にポインタに変換される。
```cpp
#include <iostream>

int x[] = {2, 4, 6, 8, 10};
int* p = x;
std::cout << *p << std::endl;        // 2
std::cout << *(p + 1) << std::endl;  // 4
std::cout << *(p + 2) << std::endl;  // 6
std::cout << *(p + 3) << std::endl;  // 8
std::cout << *(p + 4) << std::endl;  // 10

// int y[] = x;　は出来ない。
```

