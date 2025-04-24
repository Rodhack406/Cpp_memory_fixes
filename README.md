# C++ Memory Management Fixes

This repo showcases great understanding of memory management and pointer handling in C++. In this project, I am taking on the role of a systems-level engineer tasked with identifying, debugging, and fixing common, yet critical memory issues in C++. This isn’t theory. It’s a real, hands-on experience..

I this lab simulation contains broken code to simulate real-world problems developers face in C++ environments: 
### memory leaks
### segmentation faults
### dangling pointers
### uninitialized memory and 
### out-of-bounds errors.

The purpose of this lab is to demonstrate that I not only understand how pointers and memory management work in C++, but I also know how to debug and fix issues with precision — using tools like ### Valgrind ### , ### logical deduction ### , and ### good engineering practice ###.

---

## What This Lab Covers

- Heap allocation and deallocation (`new` / `delete`)
- Dangling pointers and stack-frame pitfalls
- Uninitialized pointer usage
- Double deletion bugs
- Out-of-bounds memory access
- Memory debugging using Valgrind
- Writing and documenting clean fixes
- Preventive memory safety strategies

---

## Structure

### Source Code
All C++ programs are located in the `src/` folder.

| File | Bug Type |
|------|----------|
| `memory_leak.cpp` | A User class allocates memory in the constructor but forgets to release it in the destructor. |
| `double_delete.cpp` | A Resource object manually deletes a pointer, then deletes it again in the destructor, classic double delete. |
| `dangling_pointer.cpp` | A function returns a pointer to a local stack array, and the main function tries to use it — resulting in a dangling pointer. |
| `uninitialized_pointer.cpp` | A class dereferences a pointer that was never initialized, leading to undefined behavior. |
| `out_of_bounds.cpp` | Dynamically allocated array is written one index past its bounds — easy to miss but very dangerous. |

Each bug has a corresponding fixed version in `src/fixed_versions/`.

---

## What You'll Find in This Repo

| File | Description |
|------|-------------|
| [`Pointer_Bugs_and_Fixes.md`](./report/Pointer_Bugs_and_Fixes.md) | A log of each issue, how it was found, what caused it, and how I fixed it |
| [`Debugging_Process.md`](./report/Debugging_Process.md) | My personal debugging workflow, including Valgrind output, command-line steps, and thought process |
| [`Reflection.md`](./report/Reflection.md) | What I learned, what surprised me, and how I grew as an engineer through this lab |
| [`Concepts_Summary.md`](./report/Concepts_Summary.md) | My understanding of core memory concepts, written clearly and in my own words |

---

## Why This Lab Matters

A lot of developers say they “know pointers” — I wanted to *show* it.

This lab is my proof. I’ve made mistakes on purpose, fixed them manually, and explained everything clearly. If you want to know whether I understand C++ memory management, just look through this repo.

— **Moses Kaluba**
