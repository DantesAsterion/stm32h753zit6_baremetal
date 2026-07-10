# STM32H753ZIT6 Absolute Bare-Metal DO-178C Project

## Project Goals
- Bare-metal drivers for STM32H753ZIT6 (Cortex-M7) from absolute zero.
- Strict adherence to DO-178C (Requirements, Traceability, Verification).
- 100% MISRA C:2012 compliant.
- End goal: Deterministic DTCM Memory Pool handling MDMA and DSP algorithms.

## Toolchain & Environment
- **OS:** Linux Mint
- **Editor & Multiplexer:** Neovim + Tmux
- **Build System:** Custom Makefile written from scratch
- **Compiler:** `arm-none-eabi-gcc`
- **Debugger:** `gdb-multiarch` + `OpenOCD`
- **Book Generation:** `pdflatex` (O'Reilly style textbook)

## Coding Standards & Style
- **Language:** Strictly C99 and ARMv7E-M Assembly.
- **ZERO EXTERNAL DEPENDENCIES:** The inclusion of ANY standard library (e.g., `#include <stdint.h>`) is strictly forbidden. All basic types, macros, and utilities must be defined manually.
- **Naming Conventions:**
  - Macros/Registers: `UPPER_CASE_SNAKE`
  - Variables/Functions: `lower_case_snake`
  - Types: `PascalCase_t`
- **Specific Rules:** ALWAYS use `NO` instead of `num` for GPIO numbering suffixes or variables (e.g., `pin_NO`, not `pin_num`).
- **Memory Safety:** No dynamic memory allocation. Static allocation and custom deterministic memory pools only.
- **Documentation:** All code must be heavily documented with DO-178C LLR traceability tags.
