![](../../workflows/gds/badge.svg) ![](../../workflows/docs/badge.svg) ![](../../workflows/wokwi_test/badge.svg) ![](../../workflows/fpga/badge.svg)

# 1-Bit Full Adder with Carry

A digital 1-bit full adder circuit designed for Tiny Tapeout. This project implements binary addition using basic logic gates, suitable for educational purposes and as a building block for larger arithmetic circuits.

- [View project documentation](docs/info.md)
- [View Wokwi project](https://wokwi.com/projects/your-wokwi-id) (Replace with your actual Wokwi ID)

## 📋 Overview

This full adder takes three 1-bit inputs and produces two 1-bit outputs:
- **Inputs:** A, B, and Carry-in (Cin)
- **Outputs:** Sum and Carry-out (Cout)

The circuit can be cascaded to create multi-bit adders for processors, calculators, and digital systems.

## 🔧 How It Works

The full adder implements binary addition using combinational logic:

### Logic Equations


### Truth Table

| A | B | Cin | Sum | Cout |
|---|---|-----|-----|------|
| 0 | 0 | 0   | 0   | 0    |
| 0 | 0 | 1   | 1   | 0    |
| 0 | 1 | 0   | 1   | 0    |
| 0 | 1 | 1   | 0   | 1    |
| 1 | 0 | 0   | 1   | 0    |
| 1 | 0 | 1   | 0   | 1    |
| 1 | 1 | 0   | 0   | 1    |
| 1 | 1 | 1   | 1   | 1    |

### Gate Implementation
- **2 XOR gates** - Generate the Sum output
- **2 AND gates** - Detect carry conditions
- **1 OR gate** - Combine carry outputs

## 🧪 How to Test

### Basic Testing
1. Apply inputs to A, B, and Cin using switches or push buttons
2. Observe Sum and Cout on LEDs
3. Verify against the truth table above

### Simulation Testing
The GitHub action automatically runs tests on your design. Check the Actions tab for results.

### Hardware Testing
1. Connect power (3.3V-5V) to VCC and GND
2. Connect input switches to A, B, and Cin pins
3. Connect LEDs (with 220-330Ω resistors) to Sum and Cout pins
4. Test all 8 input combinations

## 🔌 External Hardware Required

| Component | Quantity | Purpose |
|-----------|----------|---------|
| Push buttons or DIP switches | 3 | Inputs (A, B, Cin) |
| LEDs | 2 | Output indicators (Sum, Cout) |
| Resistors (220-330Ω) | 2 | Current limiting for LEDs |
| Breadboard | 1 | Prototyping |
| Jumper wires | ~10 | Connections |
| Power supply (3.3V-5V) | 1 | Circuit power |

## 📊 Implementation Stats

- **Cell count:** 55 logic cells
- **Utilization:** 0.94% of chip area
- **Wire length:** 443µm
- **Logic family:** Combinational (no clock required)

## 🚀 Tiny Tapeout Submission

This project is designed for Tiny Tapeout. The GitHub action automatically:
1. Fetches the netlist from Wokwi
2. Builds the ASIC files
3. Generates GDSII layout
4. Runs tests
5. Creates documentation

## 📁 Repository Structure
📦 your-repo-name/
│
├── 📂 .devcontainer/
│   └── devcontainer.json
│
├── 📂 .github/
│   └── 📂 workflows/
│       ├── gds.yaml
│       ├── docs.yaml
│       ├── wokwi_test.yaml
│       └── fpga.yaml
│
├── 📂 .vscode/
│   ├── settings.json
│   └── extensions.json
│
├── 📂 docs/
│   ├── 📂 images/
│   │   ├── circuit-diagram.png
│   │ 
│   │   └── wokwi-screenshot.png
│   ├── info.md
│   └── README.md
│
├── 📂 src/
│   ├── user_module.v
│   └── user_module_tb.v
│
├── 📂 test/
│   ├── 📂 data/
│   │   └── expected_outputs.txt
│   └── config.yaml
│
├── .gitignore
├── diagram.json
├── info.yaml
├── LICENSE
├── Makefile
└── README.md



## 🌐 Resources

- [Tiny Tapeout FAQ](https://tinytapeout.com/faq/)
- [Digital design lessons](https://tinytapeout.com/digital_design/)
- [Learn how semiconductors work](https://tinytapeout.com/siliwiz/)
- [Join the community on Discord](https://tinytapeout.com/discord)
- [Build your design locally](https://www.tinytapeout.com/guides/local-hardening/)

## 📈 Applications

- Building block for Arithmetic Logic Units (ALUs)
- Multi-bit adder circuits (cascade multiple 1-bit adders)
- Digital counters and accumulators
- Microprocessor design
- Educational tool for binary arithmetic

## 🎯 Next Steps

- [Submit your design to the next shuttle](https://app.tinytapeout.com/)
- Test your design with the FPGA workflow
- Share your project:

  | Platform | Link/Tag |
  |----------|----------|
  | LinkedIn | [#tinytapeout](https://www.linkedin.com/search/results/content/?keywords=%23tinytapeout) [@TinyTapeout](https://www.linkedin.com/company/100708654/) |
  | Mastodon | [#tinytapeout](https://chaos.social/tags/tinytapeout) [@matthewvenn](https://chaos.social/@matthewvenn) |
  | X (Twitter) | [#tinytapeout](https://twitter.com/hashtag/tinytapeout) [@tinytapeout](https://twitter.com/tinytapeout) |
  | Bluesky | [@tinytapeout.com](https://bsky.app/profile/tinytapeout.com) |

## 📝 License

This project is open source hardware/software.

## 🙏 Acknowledgments

- Tiny Tapeout team for the educational shuttle
- Wokwi for the online simulator
- Open source EDA tools community

---

**Happy building!** 🎉
