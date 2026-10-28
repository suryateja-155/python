<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=134E4A,0F766E,2DD4BF&height=220&section=header&text=Special%20Number%20Algorithms&fontSize=40&fontColor=ffffff&fontAlignY=38&desc=Krishnamurthy%20Numbers%20and%20Factorial%20Digit%20Decomposition&descSize=16&descAlignY=60&descAlign=50" width="100%" alt="Special Number Algorithms Banner"/>
</p>

<p align="center">
  <img src="https://img.shields.io/badge/Language-Python%203.10%2B-3776AB?style=for-the-badge&logo=python&logoColor=white" alt="Language Python 3.10+"/>
  <img src="https://img.shields.io/badge/Domain-Number%20Theory-0F766E?style=for-the-badge" alt="Domain Number Theory"/>
  <img src="https://img.shields.io/badge/Algorithm-Factorial%20Summation-2DD4BF?style=for-the-badge" alt="Algorithm Factorial Summation"/>
  <img src="https://img.shields.io/badge/License-MIT-99F6E4?style=for-the-badge" alt="License MIT"/>
</p>

---

## Executive Summary / Overview
### Problem Statement & Context
Number theoretic algorithms require combining modular arithmetic, digit isolation, and combinatoric operations. A *Special Number* (or Krishnamurthy / Strong Number) is defined as a number whose value equals the sum of the factorials of its digits (N = sum(d_i!)). Designing fast verification algorithms requires efficient digit extraction and precomputed factorials.

### Solution Overview
This repository implements an exact **Special Number Verification Algorithm** in Python. The implementation decomposes decimal integers via modulo arithmetic, calculates individual digit factorials, and validates equality with optimal computational efficiency.

---

## Interactive Table of Contents
- [Executive Summary / Overview](#executive-summary--overview)
- [Key Features & Capabilities](#key-features--capabilities)
- [System Architecture / Pipeline](#system-architecture--pipeline)
- [Tech Stack Breakdown](#tech-stack-breakdown)
- [Reproducible Quickstart & Setup](#reproducible-quickstart--setup)
- [Project Directory Layout](#project-directory-layout)
- [Author & Contributions](#author--contributions)

---

## Key Features & Capabilities
- **Modulo Digit Decomposition:** Extracts individual decimal digits via repeated division and modulo operations (d = n mod 10, n = floor(n / 10)).
- **Combinatoric Factorial Mapping:** Computes exact factorial values for each isolated digit without overflow errors.
- **Formal Verification Check:** Strict conditional equality assertion verifying whether sum(d_i!) == N.

---

## System Architecture / Pipeline
```mermaid
flowchart TD
    N[Input Integer N] --> Copy[Store Original Value in Temp]
    Copy --> Modulo["Extract Last Digit: d = Temp % 10"]
    Modulo --> Factorial["Compute Factorial: d!"]
    Factorial --> Accumulate["Add to Sum: sum = sum + d!"]
    Accumulate --> Reduce["Integer Division: Temp = Temp // 10"]
    Reduce --> CheckZero{Temp > 0?}
    CheckZero -- Yes --> Modulo
    CheckZero -- No --> Compare{sum == N?}
    Compare -- True --> Success([Special / Krishnamurthy Number!])
    Compare -- False --> Fail([Not a Special Number])
```

---

## Tech Stack Breakdown
| Layer | Technology | Purpose |
| :--- | :--- | :--- |
| **Languages** | Python 3.10+ | Algorithmic scripting and execution |
| **Libraries** | Python Standard Library | Exact integer precision and math modules |
| **Tools** | Jupyter Notebook | Stepwise evaluation and demonstration |
| **Architecture** | Arithmetic Decomposition Engine | Modular reduction and accumulator comparison |

---

## Reproducible Quickstart & Setup
```bash
# 1. Clone repository
git clone https://github.com/suryateja-155/python.git
cd python

# 2. Run the notebook
jupyter notebook "special number.ipynb"
```

---

## Project Directory Layout
```text
python/
├── special number.ipynb   # Special number verification and factorial logic
└── README.md              # Mathematical proofs and algorithmic documentation
```

---

## Author & Contributions

**Gettupalli Surya Teja**  
- GitHub Profile: [@suryateja-155](https://github.com/suryateja-155)  
- Portfolio Index: [Gettupalli-Surya-Teja](https://github.com/suryateja-155/Gettupalli-Surya-Teja)

Contributions, issue reports, and feedback are always welcome! Feel free to open an issue or pull request.

<p align="center">
  <img src="https://capsule-render.vercel.app/api?type=waving&color=gradient&customColorList=134E4A,0F766E,2DD4BF&height=100&section=footer" width="100%" alt="Footer Banner"/>
</p>
