# 🔢 STM32 Mastermind LED Guessing Game

This project recreates the classic **Mastermind** game using the **STM32F103RB microcontroller**.  
You must guess a **4-digit hexadecimal code (0–F)** within **8 attempts** using **DIP switches** to input digits and a **push button** to confirm.

---

## 🎯 Game Concept

After each guess, feedback is shown using **4 LEDs**:

| LED State | Meaning |
|-----------|---------|
| 🟢 Solid ON  | Correct digit, correct position |
| ✴️ Blinking  | Correct digit, wrong position |
| ⚫ Off       | Digit not in the code |

Like **Wordle**, the game shows how many digits are correct or misplaced —  
**but it does not reveal their positions**.

---

## 🛠 Hardware Pin Mapping

### 🔌 LEDs (Outputs)
| LED | Pin |
|-----|-----|
| LED1 (MSB) | PA0 |
| LED2       | PA1 |
| LED3       | PA4 |
| LED4 (LSB) | PB0 |

### 🎚 DIP Switch Inputs
| Switch | Pin |
|--------|-----|
| SW0 (LSB) | PB4 |
| SW1       | PB6 |
| SW2       | PB8 |
| SW3 (MSB) | PB9 |

### 🔘 User Button
| Component | Pin |
|-----------|-----|
| User Button | PC13 |

---

## 🚀 How to Play

1️⃣ Set a **hex digit (0–F)** using the DIP switches  
2️⃣ Press the **User Button** to confirm the digit  
3️⃣ Repeat for all **4 digits**  
4️⃣ LEDs display **feedback** (Solid / Blinking / Off)  
5️⃣ Use feedback to make your next guess  
6️⃣ Win by correctly guessing all 4 digits  
7️⃣ Lose if all **8 attempts** are used without success  

---

## 🎥 Tutorial Video

👉 **[Click here to watch the tutorial video](https://example.com)**  
*(Replace with your actual link — YouTube, Drive, OneDrive, URCourses, etc.)*

---

## 🧠 Win & Lose Animations

| Condition | Outcome |
|-----------|---------|
| All 4 digits correct | 🎉 Win — All LEDs blink together |
| 8 wrong attempts     | 💀 Lose — LED chase animation |

---

## ✨ Features

✔ DIP switch input (0–15)  
✔ LED feedback display  
✔ Button input with debounce  
✔ Mastermind-style game logic  
✔ Win/Lose animations  
✔ Replayable without reset  

---

## 💡 Possible Extensions

- Use SysTick for random code generation  
- UART serial debug output  
- LCD or 7-segment display support  
- FreeRTOS state-based version  
- EEPROM-based score tracking  

---

## 👤 Author

**Amr Azouz**  
University of Regina — Faculty of Engineering & Applied Science

---
