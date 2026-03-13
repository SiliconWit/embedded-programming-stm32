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

1. Fork the repository: [SiliconWit/embedded-programming-stm32](https://github.com/SiliconWit/embedded-programming-stm32)
2. Create a feature branch: `git checkout -b feature/your-topic`
3. Make your changes and commit with a clear message
4. Push to your fork and open a Pull Request against `main`
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
