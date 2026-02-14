---
title: "Rendering Test Post"
date: 2026-02-14
draft: false
tags: ["test", "markdown", "latex"]
categories: ["Test"]
math: true
---

This is a test post designed to evaluate Hugo site's Markdown rendering and LaTeX mathematical formula support.

## 1. Heading Test

# Heading 1
## Heading 2
### Heading 3
#### Heading 4
##### Heading 5
###### Heading 6

## 2. Text Formatting Test

This is **bold text**, this is *italic text*, this is ***bold italic text***.

This is ~~strikethrough text~~, this is `inline code`.

> This is a blockquote
> It can span multiple lines
>> Even nested blockquotes are possible

## 3. List Test

### Unordered List
- Item one
- Item two
  - Subitem 2.1
  - Subitem 2.2
    - Sub-subitem 2.2.1
- Item three

### Ordered List
1. First item
2. Second item
   1. Subitem 2.1
   2. Subitem 2.2
3. Third item

### Task List
- [x] Completed task
- [ ] Incomplete task
- [ ] Another to-do item

## 4. Links and Images Test

This is a [link example](https://example.com).

This is a link with title: [Hugo Official Site](https://gohugo.io "Hugo Static Site Generator")

This is an image (if it exists):
![Alternative text](https://via.placeholder.com/600x300 "Image title")

## 5. Table Test

| Header 1 | Header 2 | Header 3 |
|----------|----------|----------|
| Content A | Content B | Content C |
| Data 1 | Data 2 | Data 3 |
| Test X | Test Y | Test Z |

Alignment test:

| Left Aligned | Center Aligned | Right Aligned |
|:-------------|:--------------:|--------------:|
| Left         | Center         | Right         |
| AAA          | BBB            | CCC           |

## 6. Code Block Test

### Python Code
```python
def fibonacci(n):
    """Calculate Fibonacci sequence"""
    if n <= 1:
        return n
    return fibonacci(n-1) + fibonacci(n-2)

## Test function
for i in range(10):
    print(f"F({i}) = {fibonacci(i)}")
```

### JavaScript Code
```javascript
const greet = (name) => {
    console.log(`Hello, ${name}!`);
};

greet("World");
```

### Bash Code
```bash
#!/bin/bash
echo "Hello from bash script"
for i in {1..5}; do
    echo "Count: $i"
done
```

## 7. LaTeX Mathematical Formula Test

### Inline Formulas

This is an inline formula example: $E = mc^2$, and $a^2 + b^2 = c^2$.

Circle area formula: $A = \pi r^2$, where $r$ is the radius.

### Block Formulas

Quadratic equation solution:

$$x = \frac{-b \pm \sqrt{b^2 - 4ac}}{2a}$$

Euler's formula (one of the most beautiful equations in mathematics):

$$e^{i\pi} + 1 = 0$$

Matrix example:

$$
\begin{bmatrix}
a & b & c \\
d & e & f \\
g & h & i
\end{bmatrix}
$$

Integration example:

$$\int_{0}^{\infty} e^{-x^2} dx = \frac{\sqrt{\pi}}{2}$$

Summation formula:

$$\sum_{i=1}^{n} i = \frac{n(n+1)}{2}$$

### Complex Formulas

Fourier Transform:

$$F(\omega) = \int_{-\infty}^{\infty} f(t) e^{-i\omega t} dt$$

Schrödinger Equation:

$$i\hbar\frac{\partial}{\partial t}\Psi(\mathbf{r},t) = \hat{H}\Psi(\mathbf{r},t)$$

Maxwell's Equations:

$$
\begin{align}
\nabla \cdot \mathbf{E} &= \frac{\rho}{\epsilon_0} \\
\nabla \cdot \mathbf{B} &= 0 \\
\nabla \times \mathbf{E} &= -\frac{\partial \mathbf{B}}{\partial t} \\
\nabla \times \mathbf{B} &= \mu_0\mathbf{J} + \mu_0\epsilon_0\frac{\partial \mathbf{E}}{\partial t}
\end{align}
$$

## 8. Horizontal Rule Test

---

***

___

## 9. Special Characters Test

HTML entities: &copy; &reg; &trade; &nbsp; &lt; &gt; &amp;

Emoji: 😀 🎉 🚀 ⭐ 💡

## 10. Footnote Test

Here's a footnote reference[^1], and another one[^2].

[^1]: This is the content of the first footnote.
[^2]: This is the second footnote, which can include **formatted text** and `code`.
