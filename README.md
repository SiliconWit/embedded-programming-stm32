---
title: "Embedded Programming STM32 - Collaboration Guide"
description: "Contributing guide for Embedded Programming STM32 course content"
tableOfContents: true
sidebar:
  order: 999
---

# Embedded Programming STM32

![Build](https://img.shields.io/badge/build-passing-brightgreen)
![License](https://img.shields.io/badge/license-MIT-blue)
![Contributors Welcome](https://img.shields.io/badge/contributors-welcome-orange)

**Read this course at:** [https://siliconwit.com/education/embedded-programming-stm32/](https://siliconwit.com/education/embedded-programming-stm32/)

A course on STM32 ARM Cortex-M development covering HAL and register-level programming. Topics include clock configuration, DMA, communication peripherals, FreeRTOS integration, and production firmware practices.

## Lessons

| # | Title |
|---|-------|
| 1 | STM32 Toolchain and ARM Architecture |
| 2 | GPIO and Clock Tree |
| 3 | Timers PWM and Input Capture |
| 4 | UART with DMA and Interrupts |
| 5 | SPI and I2C HAL vs Registers |
| 6 | ADC with DMA and Analog Watchdog |
| 7 | Debugging with SWD and GDB |
| 8 | FreeRTOS on STM32 |
| 9 | Low-Power and Production Firmware |

## File Structure

```
embedded-programming-stm32/
├── lesson-0.mdx        # Course introduction
├── lesson-1.mdx        # STM32 Toolchain and ARM Architecture
├── lesson-2.mdx        # GPIO and Clock Tree
├── lesson-3.mdx        # Timers PWM and Input Capture
├── lesson-4.mdx        # UART with DMA and Interrupts
├── lesson-5.mdx        # SPI and I2C HAL vs Registers
├── lesson-6.mdx        # ADC with DMA and Analog Watchdog
├── lesson-7.mdx        # Debugging with SWD and GDB
├── lesson-8.mdx        # FreeRTOS on STM32
├── lesson-9.mdx        # Low-Power and Production Firmware
└── README.md
```

## How to Contribute

All commands below work on Linux, macOS, and Windows (using Git Bash, PowerShell, or Command Prompt with Git installed).

### For Team Members (with push access)

**First time setup (clone the repo once):**

```bash
git clone https://github.com/SiliconWit/embedded-programming-stm32.git
cd embedded-programming-stm32
```

**Every time you start working:**

```bash
git pull origin main
```

Always pull before making changes. This avoids conflicts with other contributors.

**After making your changes:**

```bash
git add .
git commit -m "Brief description of what you changed"
git push origin main
```

**If you get a push error** (someone pushed before you):

```bash
git pull origin main
```

Git will merge the changes automatically in most cases. If there is a conflict, Git will mark the conflicting lines in the file. Open the file, choose which version to keep, then:

```bash
git add .
git commit -m "Resolve merge conflict"
git push origin main
```

**Tips to avoid conflicts:**

- Always `git pull origin main` before you start working
- Push your changes as soon as you are done, do not hold onto uncommitted work for long
- Coordinate with other contributors so two people are not editing the same file at the same time

### For External Contributors (without push access)

1. Fork the repository: [SiliconWit/embedded-programming-stm32](https://github.com/SiliconWit/embedded-programming-stm32)
2. Clone your fork:
   ```bash
   git clone https://github.com/YOUR-USERNAME/embedded-programming-stm32.git
   cd embedded-programming-stm32
   ```
3. Make your changes and commit:
   ```bash
   git add .
   git commit -m "Brief description of what you changed"
   git push origin main
   ```
4. Open a Pull Request against `main` on the original repository
5. Describe what you changed and why in the PR description

## Content Standards

- All lesson files use `.mdx` format
- Do not use `<BionicText>` in this course
- Code blocks should include a title attribute:
  ````mdx
  ```c title="uart_dma.c"
  HAL_UART_Transmit_DMA(&huart2, buffer, len);
  ```
  ````
- Use Starlight components (`<Tabs>`, `<TabItem>`, `<Steps>`, `<Card>`) where appropriate
- Keep paragraphs concise and focused on practical application
- Include working code examples that readers can compile and flash

## Local Development

Clone the main site repository and initialize submodules:

```bash
git clone --recurse-submodules <main-repo-url>
cd siliconwit-com
npm install
npm run dev
```

To test a production build:

```bash
npm run build
```

## License

This course content is released under the [MIT License](LICENSE).
