# 🔢 STM32 Mastermind LED Guessing Game

This project recreates the classic **Mastermind** game using the **STM32F103C8T6 (Blue Pill)** microcontroller.  
You must guess a **4-digit hexadecimal code (0–F)** within **8 attempts** using DIP switches to input digits and a push button to confirm.

---

## 🎯 Game Concept

After each guess, feedback is shown using **4 LEDs**:

| LED State | Meaning |
|-----------|---------|
| Solid ON  | Correct digit, correct position |
| Blinking  | Correct digit, wrong position |
| Off       | Digit not in the code |

Like **Wordle**, the game tells you how many digits are correct or misplaced — **but not their positions**.

---

## 🛠 Hardware Pin Mapping

### LEDs (Outputs)
| LED | Pin |
|-----|-----|
| LED1 (MSB) | PA0 |
| LED2 | PA1 |
| LED3 | PA4 |
| LED4 (LSB) | PB0 |

### DIP Switch Inputs
| Switch | Pin |
|--------|-----|
| SW0 (LSB) | PB4 |
| SW1 | PB6 |
| SW2 | PB8 |
| SW3 (MSB) | PB9 |

### User Button
| Component | Pin |
|-----------|-----|
| User Button | PC13 |

---

## 🚀 How to Play

1️⃣ Set a hex digit (0–F) using DIP switches  
2️⃣ Press the **User Button** to confirm  
3️⃣ Repeat for all 4 digits  
4️⃣ LEDs display feedback (Solid / Blinking / Off)  
5️⃣ Use feedback to make a new guess  
6️⃣ Win by correctly guessing all 4 digits  
7️⃣ Lose if all 8 attempts are used without success  

---

## 🧠 Win & Lose Animations

| Condition | Outcome |
|-----------|---------|
| All 4 digits correct | 🎉 Win — flashing animation |
| 8 incorrect attempts | 💀 Lose — LED chase animation |

---

## ✨ Features

✔ Bare-metal STM32 programming (no HAL)  
✔ DIP switch hex input (0–15)  
✔ LED feedback display  
✔ Button input with debounce  
✔ Win/Lose animations  
✔ Mastermind-style logic  

---

## 💡 Possible Extensions

- Generate random secret using SysTick  
- UART serial output for debugging  
- 7-segment or LCD output  
- FreeRTOS-based game states  
- Score tracking & EEPROM storage  

---

## 📄 License

MIT License — free to modify and share.

---

## 👤 Author

**Amr Azouz**  
University of Regina — Faculty of Engineering & Applied Science
