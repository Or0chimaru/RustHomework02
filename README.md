# RustHomework02
---
## 所有权 Ownership

- Rust 中的任意值**有且仅有一个**所有者
- 所有者通过变量名表示
- 值会在其所有者离开作用域时被释放
- 所有者作用域范围
	- 如果变量是在函数内部声明，那么它的作用域从声明处开始，直到函数的大括号块结束。
	- 如果变量是在代码块（由大括号括起来的一段代码）内部声明，那么它的作用域从声明处开始，直到该代码块的大括号块结束。

## 不可变引用和可变引用

- 区分引用和所有者的作用域：引用的作用域始之于其定义，终之于其最后一次使用，如从未使用，则作用域仅在其所被定义的一行，因此引用的作用域不会长于所有者的作用域，因此 Rust 中的引用必定是有效的。
- 一个资源的某个可变引用和某个不可变引用作用域不能交叠
- 一个资源多个不可变引用作用域可以交叠
- 一个资源多个可变引用作用域不能交叠
