# 4 Semesters in CS in 5 hours with Brian Holt on [Lynda](https://www.lynda.com/JavaScript-tutorials/Four-Semesters-Computer-Science-5-Hours/604270-2.html)

> "Code is more for the person that has to maintain it than it is for the computer" - Kyle Simpson

## Big O

Big O is the way we analyze how efficient algorithms it ignores the little parts and concentrate on the big parts. "Broad strokes." The key is to look for nested loops which represent the exponent.

*Ex:* A loop **inside** of a loop inside of a loop would be O(n³).

O(log n) = As you add more terms to whatever you're doing it is going to take less time. Diminishing time = logarithmic time.

---

## Recursion

Recursion is when you define something in terms of itself. You define a function that calls itself. Each level of a recursive call has the ability to maintain it's own state. Calling a function is **not** free. It carries a cost, especially when dealing with memory. A *stack overflow* is when you recurse too far down and your computer runs out of the ability to track new calls with memory. Always favor Readability > performance. Once it becomes a problem/bottleneck, it should be refactored to be more iterative. Don't be clever in your code unless you have to be, always consider that someone else will be maintaining what you write.