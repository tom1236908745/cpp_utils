## メモリ領域

c++のプログラムが使用する主な領域

### スタック
pros: メリットヒープと比べて高速に扱える。メモリの確保と解放はコンパイラ、OSが自動的に行う。

cons: 使用できるスタックに限りがあるので、大きなデータを扱うのには向いていない。


```cpp
void Function() {
    int x = 100; // ローカル変数xはスタックに確保される。
    int y = 200; // ローカル変数yはスタックに確保される。

} // 関数の終了とともに変数 x, y はスタックから取り除かれる。
  // スタックはLIFO（後入れ先出し）形式のため y, x の順で取り除かれる。

int main() {
    Function();

    return 0;
}
```
### ヒープ
pros: サイズをプログラム実行時に動的に変化させる事ができる。自由度が高い。
cons: メモリの確保と解放を行う必要がある。
other: std::vector は、保持する要素をヒープ上に確保することで、要素数を実行時に変更できるという仕組みを実現しています。 
