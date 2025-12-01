Mastermind – STM32 Term Project

What is the Game:
Mastermind is a code-breaking logic game. In this STM32 version, the system randomly generates a secret 4-digit hexadecimal code using digits 0 to F. Your goal is to correctly guess the entire 4-digit code in 8 tries or less. After every guess, the system gives feedback using LEDs to help you narrow down the correct code.

How Feedback Works:

Solid ON LED: One digit is correct and in the correct position.

Blinking LED: One digit is correct but in the wrong position.

OFF LED: The digit is not in the code at all.

Solid LEDs always come first, followed by blinking LEDs, no matter the positions in your guess.

How to Play:

The system generates a new random 4-digit hexadecimal code at the start of every game.

You enter one digit at a time using the dip switches (0–F in binary).

After setting a digit on the dip switches, press the user button to confirm it.

Repeat this process four times to enter your full 4-digit guess. The LEDs will indicate which digit position you are currently entering:

Digit 1 → 1000

Digit 2 → 1100

Digit 3 → 1110

Digit 4 → 1111

After entering four digits, the LEDs display feedback:

Number of correct digits in the correct position → Solid LEDs.

Number of correct digits but in the wrong position → Blinking LEDs.

Incorrect digits → No LED.

Press the button to move to the next round and make another guess.

Continue guessing using the feedback until you either:

Guess the code correctly (Win)

Run out of attempts (Lose)

Winning:
If your guess matches the secret code exactly, all four LEDs blink together on and off four times. Then the LEDs display how many guesses it took (in 4-bit binary). Press the button to start a new game.

Losing:
If you do not guess the code within 8 attempts, the system shows a failure animation using the LEDs. Press the button to restart and play again.

Hardware Used:

STM32 Nucleo board

Dip switches

User push button

4 LEDs

This game helps develop logic thinking and teaches input handling, feedback processing, and embedded programming using GPIO control on the STM32 board.