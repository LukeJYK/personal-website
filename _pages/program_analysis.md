---
layout: page
permalink: /notes/program_analysis
title: Program Analysis
description: 
nav: false
---

<aside>
📌 Nanjing University Program Analysis

📌 Teachers: Yue Li, Tian Tan


</aside>

# 1. Introduction

Static analysis: analyze P before running P.

- information leak
- pointer(dereference, memory location)
- cast operations(eg. Java int cast to double) safe or not safe
- *assert* statement fail or not fail
- dead code problem
- …

> **Rice Theorem**: no approach determine whether P Satisfied non-trivial properties(give YES or NO answer) 无法准确告知以上情况存不存在
> 

> **Rice Theorem**: any non-trivial property of the behavior of programs in re language is undecidable 递归可枚举语言（图灵机可识别的语言）是undecidable. non-trivial properties=interesting properties=related to run-time behavior

**Perfect static analysis (sound and complete) not exist!** 

Most compromising completeness: **sound** but not **fully-precise**.

example:

```jsx
B b = new B();
a.fld = b;
C c = new C();
a.fld = c;
B b' = (B) a.fld;
```

not safe cast if run the sound static analysis.

> Static Analysis: ensure (or get close to) soundness, while making good trade-offs between analysis precision and analysis speed. (Abstraction and Over-approximation)
> 

static analysis 主要关心程序的abstract domain(sign): +, -, 0, unknown, undefined

**How to get abstract values?** Transfer function


<!-- 1. Course Introduction		                 [note][slides]
2. Intermediate Representation               [note][slides]
3. Data Flow Analysis - Applications I	     [note][slides]	
4. Data Flow Analysis - Applications II	     [note][slides]
5. Data Flow Analysis - Foundations I	     [note][slides]		
6. Data Flow Analysis - Foundations II	     [note][slides]
7. Interprocedural Analysis	                 [note][slides]
8. Pointer Analysis                          [note][slides]	  	
9. Pointer Analysis - Foundations I	         [note][slides]	
10. Pointer Analysis - Foundations II	     [note][slides]
11. Pointer Analysis - Context Sensitivity I [note][slides]		
12. Pointer Analysis - Context Sensitivity II[note][slides]	
13. Static Analysis for Security             [note][slides]	
14. Datalog-Based Program Analysis		     [note][slides]	
15. CFL-Reachability and IFDS		         [note][slides]
16. Soundness and Soundiness                 [note][slides] -->
