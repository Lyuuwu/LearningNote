# Introduction

---

## Turning machine

### What is turing machine?

Turing machine is defined by its transition functions, a.k.a **programs**. It can simulate the logic of algorithm or computation that can be described in terms of **step-by-step process**.

The Turing machine is a theoretical framework that introduces the concept of a **program**, in addition to the basic components of a computing machine, such as input/output mechanisms, memory, and a processor.

### What is the function of *program* in Turing model?

The program in Turing model is a set of instructions that **tell the computer/machine what to do**.

### What would happen if there were *no program* in the Turing model?

Without a program, the machine would be unable to **interpret the input data**, making the output data **meaningless**. Additionally, it is unclear how many types or sets of operations a machine based on this model can perform. Therefore, adding the program to the model is necessary to **specify the operation** of the machine.

---

## Von Neumann model

### What is Von Neumann model?

A computer based on the Von Neumann model comprises four subsystems: ALU, control unit, memory, and input/output. The input subsystem receives input data, while the output subsystem sends results to the outside world. Both data and programs are stored in memory, with the ALU responsible for processing the data using the program. The control unit commands the other three subsystems.

### FOUR subsystems

- arithmetic logic unit (ALU): Handles the arithmetic and logical operations on data as directed by the program.
- memory: Store both data and program instructions. This includes input data, program instructions, and results of computations.
- control unit: Responsible for coordinating and directing the operations of the other subsystems based on instructions stored in memory.
- input/output: Facilitates communication between the computer and the external world, allowing input data to be received and results to be sent out.

![Von Neumann model](Von_Neumann_model.png)

### Feature

- The stored program concept:
  - The Von Neumann model stores programs in memory, marking a significant departure from the architecture of early computers.
- Sequential execution of instructions:
  - In the von Neumann model, a program consists of a set of instructions stored in memory. The control unit fetches, decodes, and executes these instructions sequentially, meaning they are executed one after another in the order they are stored in memory.
  Although certain instructions may alter the control flow by requesting the control nit to jump to different instructions, the overall execution remains sequential.

---

## Computer

### Three Computer Components

1. computer hardware
2. data
3. computer software

#### Computer Hardware

1. central processing unit(CPU)
2. main memory
3. input/output(I/O) subsystem

### Why *Program* is composed of instructions?

The answer lies in **Reusability** and **Modularization**.

Computers handle millions of tasks. If every program were treated as an independent entity without anything in common with other programs, programming would be challenging, daunting and overwhelming.

Handling a large task can be challenging. However, breaking it down into numerous smaller tasks makes it much easier to manage. Therefore, programs should be designed ot break down into smaller more manageable parts, interact with other programs, and share resources as needed.

This approach enables **reusability** and **modularization**.

### Why *Program* must be stored?

Because computer can **execute them**. When a program is stored in memory, it means that CPU can access and retrieve the instructions that make up the program when needed.

### Computer Software

#### Algorithm

**Algorithm is a strategy to solve a specific problem.**

Programmers can effectively combine multiple instructions to solve specific tasks. They must design a step-by-step approach to problem-solving and carefully select the appropriate instructions. This systematic approach to problem-solving is known as an **algorithm**.

#### Language

Since **machine language** is too difficult, abstruse and abstract for humans to understand, computer scientists have developed **computer languages**. Computer languages, like natural language such as English, use symbols and words to command machines, making it easier for human to operate them, The key distinction between computer language and natural language is that the former is used to interact with computers, whereas the latter serves broader communication purposes among humans.

#### Software Engineering

Soft engineering involves designing and writing programs to solve tasks. However, nowadays, software engineering encompasses more than just these aspects.

#### Operating Systems(os)

Because some instructions are used frequently and written only once, this need for efficiency gave rise to the concept of operating systems. While in the past, operating systems were primarily for managing and facilitating access to a computer's components by a program, today, operating systems serve a much broader range of functions, including efficient resource management, providing a user interface, and supporting a variety of applications and services.

---

## Computer Generation (1950 - present)

- **First generation:** Computers were bulky and used vacuum tubes as electronic switches. They were only affordable for big organization.
- **Second generation:** Computers transitioned from using **vacuum tubes** to **transistors**, which reduced costs and size significantly. The invention of two-high-level programming languages, **FORTRAN** and **COBOL**, made programming much easier. These languages enabled individuals to solve programming problems without needing to delve into the electronic details of computer architecture.
- **Third generation:** The invention of **integrated circuit** (IC), which incorporates transistors, wiring, and other components on a small chip, further reduced the size and cost of computers. This innovation, along with advancements in transistor technology, led to the emergence of **minicomputers** in the market. Additionally, the availability of **canned programs**, which are software packages providing fixed solutions to specific problems, made computers more accessible to a wider audience.
- **Fourth generation:** The Altair 8800, one of the first personal computers, was introduced. Advancements in teh electronic industry enabled entire computer subsystems to fit onto a single circuit board. Computer networks also began to emerge, laying the foundation for modern networking technologies.
- **Fifth generation:** This generation witnessed the emergence of laptop, palmtop PC, improvements in secondary storage media(CD-ROM, DVD and so on), the use of multimedia, and the phenomenon of virtual reality.
