# Mission 5 — Numbers and data

## 1. Task / objective
Convert decimal, binary and hexadecimal values, verify results with Python, build a working Python number converter, and explain text encoding.

## 2. Work completed

### Task 5.1 — Convert numbers by hand

| Question | Your working and answer |
|---|---|
| Convert decimal 13 to binary. | Successive division by 2:<br>13 ÷ 2 = 6 rem 1<br>6 ÷ 2 = 3 rem 0<br>3 ÷ 2 = 1 rem 1<br>1 ÷ 2 = 0 rem 1<br>Reading remainders from bottom to top: **`1101₂`** |
| Convert decimal 25 to binary. | Successive division by 2:<br>25 ÷ 2 = 12 rem 1<br>12 ÷ 2 = 6 rem 0<br>6 ÷ 2 = 3 rem 0<br>3 ÷ 2 = 1 rem 1<br>1 ÷ 2 = 0 rem 1<br>Reading remainders from bottom to top: **`11001₂`** |
| Convert binary 1010 to decimal. | Positional notation (powers of 2):<br>(1 × 2³) + (0 × 2²) + (1 × 2¹) + (0 × 2⁰)<br>= 8 + 0 + 2 + 0 = **`10₁₀`** |
| Convert binary 1101 to decimal. | Positional notation (powers of 2):<br>(1 × 2³) + (1 × 2²) + (0 × 2¹) + (1 × 2⁰)<br>= 8 + 4 + 0 + 1 = **`13₁₀`** |
| Convert hexadecimal A to decimal. | Single hex digit value:<br>In base 16, A represents **`10₁₀`** |
| Convert hexadecimal 1F to decimal. | Positional notation (powers of 16):<br>(1 × 16¹) + (15 × 16⁰)<br>= 16 + 15 = **`31₁₀`** |
| Convert binary 1111 to hexadecimal. | 4-bit nibble conversion:<br>(1 × 2³) + (1 × 2²) + (1 × 2¹) + (1 × 2⁰) = 8 + 4 + 2 + 1 = 15₁₀<br>In base 16, 15 is represented as **`F₁₆`** |

---

### Task 5.2 — Verify using Python
Tested in Python 3 interactive shell:

| Test Expression | Python Result | Matches Manual Calculation? |
|---|---|---|
| `bin(13)` | `'0b1101'` | Yes (`1101`) |
| `bin(25)` | `'0b11001'` | Yes (`11001`) |
| `int('1010', 2)` | `10` | Yes (`10`) |
| `int('1101', 2)` | `13` | Yes (`13`) |
| `int('A', 16)` | `10` | Yes (`10`) |
| `int('1F', 16)` | `31` | Yes (`31`) |
| `hex(0b1111)` | `'0xf'` | Yes (`F`) |

---

### Task 5.3 — Build a small number converter
Created and tested `number_converter.py`:

| Test number | Binary output | Hexadecimal output |
|---|---|---|
| 13 | `0b1101` | `0xd` |
| 25 | `0b11001` | `0x19` |
| 42 | `0b101010` | `0x2a` |

#### How the conversion functions work:
- `bin(x)`: Converts an integer `x` into a binary string prefixed with `0b`.
- `hex(x)`: Converts an integer `x` into a lowercase hexadecimal string prefixed with `0x`.
- `int(s, base)`: Parses a string representation `s` in the specified numeric base and returns the corresponding decimal integer.

---

### Task 5.4 — How is text stored?
- **ASCII decimal codes:**
  - Uppercase letter **'A'**: `65` (binary `01000001`)
  - Lowercase letter **'a'**: `97` (binary `01100001`)
- **Why computers need an encoding standard to store text:**
  Computers operate purely with binary electrical states (bits: 0 and 1). An encoding standard assigns a standardized numerical code point to each letter, punctuation mark, and symbol, ensuring that text written on one machine displays accurately on another without misinterpretation.
- **Example character outside basic ASCII:**
  The emoji **'🚀'** (Unicode code point `U+1F680`, encoded in UTF-8 as 4 bytes: `0xF0 0x9F 0x9A 0x80`) or accented characters like **'é'** (`U+00E9`).

## 3. Commands / tools used
- `python3` interactive REPL for verifying base conversions.
- `python3 number_converter.py` for executing the conversion CLI program.
- Python built-ins: `input()`, `int()`, `bin()`, `hex()`, and string formatting.

## 4. My understanding
I learned that all digital information is stored as bits and bytes. Binary (base 2) directly reflects hardware transistor states, hexadecimal (base 16) provides a compact, human-readable shorthand for binary bytes, and character encoding schemes (ASCII, UTF-8) translate text into numeric codes.

## 5. Difficulties faced
Distinguishing between the 7-bit ASCII range (0–127) and multi-byte UTF-8 representations for international characters and emojis.

## 6. How I resolved them
Researched UTF-8 variable-length encoding, understanding that standard ASCII characters are preserved in the first 128 code points using a single byte, while extended characters use 2 to 4 bytes.

## 7. Evidence / files
- `mission-05-numbers-data/number_converter.py`
- Manual calculation steps, REPL verification, and text encoding notes in `mission-05-numbers-data/README.md`.

## 8. Commit details
- **Commit message:** `Build number converter and practise data representation`
- **Pushed to GitHub:** Yes
