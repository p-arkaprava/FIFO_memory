# 📦 FIFO Memory in Verilog

This project implements a **FIFO (First-In-First-Out) memory** in Verilog, designed for efficient data buffering in digital systems. The FIFO includes core memory logic, read/write pointer control, and advanced status signal handling.

---

## 🧠 Project Specifications

- 🔢 16-stage FIFO memory
- 📏 8-bit data width
- 🔄 Synchronous design using clock and reset
- ✅ Includes overflow, underflow, full, empty, and threshold status indicators

---

## 📂 Files Included

| File Name                     | Description                                      |
|------------------------------|--------------------------------------------------|
| `fifo_mem.v`                 | Top-level FIFO module integrating all submodules |
| `memory_array.v`            | Memory storage array for FIFO                    |
| `write_pointer.v`           | Write pointer logic                              |
| `read_pointer.v`            | Read pointer logic                               |
| `status_signal.v`           | Status flags for overflow, underflow, etc.       |
| `tb_fifo_32.v`              | Testbench with clock, reset, and test operations |
| `README.md`                 | This documentation                               |

---

## 📊 Status Signals

| Signal         | Description                                                                 |
|----------------|-----------------------------------------------------------------------------|
| `fifo_full`    | High when FIFO is full                                                      |
| `fifo_empty`   | High when FIFO is empty                                                     |
| `fifo_overflow`| High when write occurs while FIFO is full                                  |
| `fifo_underflow`| High when read occurs while FIFO is empty                                 |
| `fifo_threshold`| High when FIFO usage exceeds a defined threshold                          |

---

## 🧪 Testbench Summary

- Generates clock and reset
- Performs 17 write operations followed by 17 reads
- Checks for correctness of data using internal memory mirroring
- Displays simulation progress and validation status (PASS/FAIL)

### Example Log Output

```text
TIME = 300, wr = 1, rd = 0, data_in = 01
TIME = 340, wr = 0, rd = 0, data_in = 01
=== PASS ===== PASS ==== PASS ==== PASS ===
```

---

## ⚙️ Tools Used

- 💻 **Language**: Verilog HDL
- 🧪 **Simulation**: Xilinx Vivado Simulator
- 🧰 **Design Style**: Structural and RTL
- 📐 **Modules**:
  - `fifo_mem`: Top-level wrapper
  - `write_pointer`: Write address generation
  - `read_pointer`: Read address generation
  - `memory_array`: 16x8-bit storage
  - `status_signal`: Flag logic for state reporting


## 📚 Learning Objectives

This project demonstrates:
- Modular Verilog design
- FIFO queue implementation
- Use of status flags in digital memory design
- Testbench-driven verification

---

## 👨‍💻 Author

**Arkaprava Paul**  


---

## 📝 License

This project is for academic and educational use. Please credit the author if reusing parts of the design.
