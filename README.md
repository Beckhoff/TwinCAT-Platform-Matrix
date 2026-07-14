# TwinCAT 3 Runtime Platforms

This page lists the TwinCAT runtime target platforms that are currently supported (TwinCAT 3.1, 4026).
Use it to pick the correct platform for your device when configuring a TwinCAT C++ or PLC project.

| TwinCAT platform (C++) | Associated PLC platform | Operating system | Example devices | Processor | C++ compiler | Binary format |
|--|--|--|--|--|--|--|
| TwinCAT OS (ARMV7-A) | TwinCAT OS (ARMV7-A) | TC/RTOS, Linux | AMP8000, VCS2000, EL66xx | ARM Cortex-A9 | Clang | PE (TC/RTOS), ELF (Linux) |
| TwinCAT OS (ARMV7-M) | TwinCAT OS (ARMV7-M) | TC/RTOS | CX7000 | ARM Cortex-M7 | Clang | PE |
| TwinCAT OS (ARMV8-A) | TwinCAT OS (ARMV8-A) | Linux | CX8200, CX9240 | ARM Cortex-A53 | Clang | ELF |
| TwinCAT OS (x64) | TwinCAT OS (x64) | Windows, TC/BSD | Industrial PC | x86-64 | MSVC / Clang | PE |
| TwinCAT OS (x64-E) | TwinCAT OS (x64-E) | Linux | Industrial PC | x86-64 | Clang | ELF |
| TwinCAT OS (x86) | TwinCAT OS (x86) | Windows | Industrial PC | x86 | MSVC / Clang | PE |
| TwinCAT RT (x64) | TwinCAT RT (x64) | Windows (kernel) | Industrial PC | x86-64 | MSVC | PE |
| TwinCAT RT (x86) | TwinCAT RT (x86) | Windows (kernel) | Industrial PC | x86 | MSVC | PE |

## Notes

- **TwinCAT OS ("TCOS")** is the portable TwinCAT runtime that runs on Windows (user mode), Linux and
  TC/BSD. **TwinCAT RT** is the Windows kernel-mode runtime.
- **Binary format** refers to the format of the TwinCAT-loaded runtime modules:
  - **PE** on Windows, TC/RTOS and TC/BSD (TC/BSD loads the runtime as PE via a custom loader).
  - **ELF** on Linux only.
- **x64 vs x64-E:** `TwinCAT OS (x64)` is the PE variant (Windows and TC/BSD); `TwinCAT OS (x64-E)` is the
  ELF variant, used on Linux.
- **TC/BSD** is available for **x64 only**.

*Device lists are examples, not exhaustive. Availability can depend on the TwinCAT version and device firmware.*
