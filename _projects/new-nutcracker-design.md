---
layout: project
title: New Nutcracker Design
description: ENGRD 2020 New Nutcracker
technologies: N/A
image: /assets/images/NewNutFBD.png
---

# Lever-Based Nutcracker Design (Note: Used Claude to aid with design) 

## 1. Given Information

| Parameter | Symbol | Value |
|---|---|---|
| Required cracking force | Fₒ | 222.18 N |
| Average human grip strength | Fᵢ | ≈ 40 kg → 392 N |
| Nut diameter | d | 2 cm |
| Actuator force (linear) | Fᵢ (act) | 169 lb → 751.7 N |

---

## 2. Lever Model & Approach

Moment equilibrium gives:

$$\sum M = 0 \quad \Rightarrow \quad F_o \cdot L_n = F_i \cdot L_c \quad \Rightarrow \quad \frac{F_o}{F_i} = \frac{L_c}{L_n}$$

Where:
- **Fₒ** = output (cracking) force at the nut
- **Fᵢ** = input (grip / actuator) force
- **Lc** = distance from pivot to input force (handle length)
- **Lₙ** = distance from pivot to nut contact point

### Required Mechanical Advantage

$$MA = \frac{F_o}{F_i} = \frac{222.18}{40} = 5.55$$

---

## 3. Linear Actuator Design

Actuator force: 169 lb × 4.448 N/lb = **751.7 N**

### Mechanical Advantage (actuator)

$$MA_{act} = \frac{F_o}{F_{i,act}} = \frac{222.18}{751.7} \approx 0.296$$

Because the actuator already exceeds the required cracking force, MA < 1. The lever is used primarily for positioning, not amplification.

$$L_c = MA_{act} \times L_n = 0.296 \times 4 \ \text{cm} \approx 1.18 \ \text{cm}$$


$$H_m = \frac{L_n \times H_c}{L_c} \approx 4.49 \ \text{cm}$$

| Parameter | Symbol | Value |
|---|---|---|
| Actuator force | Fᵢ_act | 751.7 N |
| Mechanical advantage | MA_act | 0.296 |
| Nut contact distance | Lₙ | 4 cm |
| Required arm length | Lc | ≈ 1.18 cm |
| Actuator mount height | Hm | ≈ 4.49 cm |

---

IMA (Ideal Mechanical Advantage) Actuator Design

The IMA actuator analysis applies the same lever equilibrium using the actuator force as the input. Two arm lengths are evaluated.

### 5.1 Given & Setup

| Parameter | Symbol | Value |
|---|---|---|
| Required cracking force | Fₒ | 222.18 N |
| Actuator output force | Fᵢ_act | 169 lb = 751.7 N |
| Nut contact distance | Lₙ | 4 cm (fixed) |

The IMA of a lever is defined as:

$$IMA = \frac{L_c}{L_n}$$

The required IMA to crack the nut:

$$IMA_{required} = \frac{F_o}{F_{i,act}} = \frac{222.18}{751.7} \approx 0.296$$

---

Actuator Arm Length Lc = 50 cm

With Lₙ = 4 cm and Lc = 50 cm:

$$IMA = \frac{L_c}{L_n} = \frac{50}{4} = 12.5$$

Output force delivered to nut:

$$F_o = IMA \times F_{i,act} = 12.5 \times 751.7 \ \text{N} = 9{,}396 \ \text{N}$$

**Safety factor vs. required: SF = 9,396 / 222.18 ≈ 42.3× → greatly exceeds requirement**

$$H_m = \frac{L_n \times H_c}{L_c} = \frac{4 \times 50}{50} = 4.0 \ \text{cm}$$

| Parameter | Symbol | Value |
|---|---|---|
| Actuator arm length | Lc | 50 cm |
| Nut contact distance | Lₙ | 4 cm |
| IMA | IMA | 12.5 |
| Force delivered to nut | Fₒ | 9,396 N |
| Safety factor | SF | ≈ 42.3× |
| Actuator mount height | Hm | 4.0 cm |

---

Actuator Arm Length Lc = 20 cm

With Lₙ = 4 cm and Lc = 20 cm:

$$IMA = \frac{L_c}{L_n} = \frac{20}{4} = 5.0$$

Output force delivered to nut:

$$F_o = IMA \times F_{i,act} = 5.0 \times 751.7 \ \text{N} = 3{,}758 \ \text{N}$$

**Safety factor vs. required: SF = 3,758 / 222.18 ≈ 16.9× → still well above requirement**


$$H_m = \frac{L_n \times H_c}{L_c} = \frac{4 \times 20}{20} = 4.0 \ \text{cm}$$

| Parameter | Symbol | Value |
|---|---|---|
| Actuator arm length | Lc | 20 cm |
| Nut contact distance | Lₙ | 4 cm |
| IMA | IMA | 5.0 |
| Force delivered to nut | Fₒ | 3,758 N |
| Safety factor | SF | ≈ 16.9× |
| Actuator mount height | Hm | 4.0 cm |

---


| Parameter | Case 1 (50 cm) | Case 2 (20 cm) | Required |
|---|---|---|---|
| Lc | 50 cm | 20 cm | — |
| IMA | 12.5 | 5.0 | 0.296 |
| Fₒ | 9,396 N | 3,758 N | 222.18 N |
| Safety Factor | 42.3× | 16.9× | ≥ 1.0× |
| Hm | 4.0 cm | 4.0 cm | — |

---

Usability Discussion

Both IMA actuator cases comfortably exceed the 222.18 N cracking requirement:

- The **50 cm arm** delivers over 42× the required force — suitable where compactness at the nut end is prioritised and over-force is acceptable (e.g., batch cracking).
- The **20 cm arm** delivers nearly 17× the required force, producing a more compact and controllable device with less risk of shell fragmentation.
- Both cases share the same actuator mount height (Hm = 4.0 cm) because the ratio Lₙ/Lc remains constant when Hc is proportional to Lc.



