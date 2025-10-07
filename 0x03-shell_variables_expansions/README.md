# Shell, init files, variables and expansions

This project contains Bash scripts that perform various tasks involving environment variables, shell initialization files, arithmetic operations, and string manipulations.

All scripts follow these rules:

- Allowed editors: `vi`, `vim`, `emacs`
- All scripts are tested on **Ubuntu 20.04 LTS**
- All scripts are **exactly two lines long**
- All files must end with a **new line**
- The first line of all files must be:  
  `#!/bin/bash`
- No use of `&&`, `||`, `;`, `bc`, `sed`, or `awk`
- All files must be **executable**

---

## **Task Descriptions**

### **0-alias**
Creates an alias named `ls` with the value `rm *`.

```bash
alias ls='rm *'
```

---

### **1-hello_you**
Prints “hello user”, where `user` is the current Linux user.

```bash
echo "hello $USER"
```

---

### **2-path**
Adds `/action` to the `PATH`. `/action` should be the last directory the shell looks into when searching for a program.

```bash
export PATH=$PATH:/action
```

---

### **3-paths**
Counts the number of directories in the `PATH`.

```bash
echo $PATH | tr ':' '\n' | wc -l
```

---

### **4-global_variables**
Lists all environment variables.

```bash
printenv
```

---

### **5-local_variables**
Lists all **local variables**, **environment variables**, and **functions**.

```bash
set
```

---

### **6-create_local_variable**
Creates a new local variable.

```bash
BEST="School"
```

---

### **7-create_global_variable**
Creates a new global variable.

```bash
export BEST="School"
```

---

### **8-true_knowledge**
Prints the result of adding **128** to the value stored in the environment variable `TRUEKNOWLEDGE`, followed by a new line.

```bash
echo $((TRUEKNOWLEDGE + 128))
```

---

### **9-divide_and_rule**
Prints the result of dividing the value of `POWER` by `DIVIDE`, followed by a new line.

```bash
echo $((POWER / DIVIDE))
```

---

### **10-love_exponent_breath**
Displays the result of `BREATH` raised to the power of `LOVE`.

```bash
echo $((BREATH ** LOVE))
```

---

### **11-binary_to_decimal**
Converts a number from base 2 to base 10.  
The number in base 2 is stored in the environment variable `BINARY`.

```bash
echo $((2#$BINARY))
```

---

### **12-combinations**
Prints all possible combinations of two lowercase letters, except `oo`.

- One combination per line
- Alphabetically ordered, starting with `aa`
- File content must be ≤ 64 characters

```bash
echo {a..z}{a..z} | tr ' ' '\n' | grep -v '^oo$'
```

---

### **13-print_float**
Prints a number with **two decimal places**, followed by a new line.  
The number is stored in the environment variable `NUM`.

```bash
printf "%.2f\n" "$NUM"
```

---

## 🧠 **Usage**

To run any script:

```bash
chmod +x script_name
./script_name
```

---

## ✅ **Example Tests**

```bash
export TRUEKNOWLEDGE=1209
./8-true_knowledge
# Output: 1337

export POWER=42784
export DIVIDE=32
./9-divide_and_rule
# Output: 1337

export BREATH=4
export LOVE=3
./10-love_exponent_breath
# Output: 64

export BINARY=10100111001
./11-binary_to_decimal
# Output: 1337

export NUM=3.14159265359
./13-print_float
# Output: 3.14
```

---

## ✨ **Author**
**DevPhil**  

