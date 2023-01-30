---
marp: true
theme: default
class: invert
---
<style>
    h1, h2, code {
        font-family: "IBM Plex Mono";
    }
</style>


# Smart Pointers in C++

---

## Pointers

When you create a pointer, you are requesting that much memory from the OS.
Later, you have to remember to give the memory back by calling `free()`.

Having to remember this each time can cause mistakes, which lead to memory leaks.

C++ has somewhat of a solution...

---

## RAII

In C++, objects have a special *destructor* function that is **automatically** called when the object goes out of scope.

> A *scope* is a block of code that is surrounded with curly brackets. When an object goes out of scope, you can't access it anymore in the code.

C++ automatically allocates memory when an object is created, and we can automatically free it at the end of the scope using the destructor.

This semi-automatic memory management pattern is called *resource acquisition is initialization*, usually shortened to *RAII*.

---

## RAII for objects
