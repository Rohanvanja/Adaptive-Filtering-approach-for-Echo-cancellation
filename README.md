# 🔊 Adaptive Echo Cancellation using LMS & NLMS

## 📌 Overview

This project implements **Adaptive Echo Cancellation (AEC)** using two widely used algorithms:

* Least Mean Squares (LMS)
* Normalized Least Mean Squares (NLMS)

The system simulates a real-world echo scenario where an input signal passes through an unknown echo path, and the goal is to **estimate and remove the echo** from the received signal.

---

## 🎯 Objective

To design an adaptive filter that:

* Learns the unknown echo path dynamically
* Estimates the echo signal
* Cancels echo from the microphone signal
* Produces a clean output signal

---

## ⚙️ Methodology

1. **Signal Generation**

   * A random input signal is generated.
   * An echo path is simulated using convolution.
   * Noise is added to mimic real-world conditions.

2. **Adaptive Filtering**

   * LMS and NLMS algorithms are used to estimate the echo.
   * The filter weights are updated iteratively using error feedback.

3. **Echo Cancellation**

   * Estimated echo is subtracted from the received signal.
   * The error signal represents the cleaned output.

---

## 🧠 Algorithms Used

### 🔹 LMS (Least Mean Squares)

* Simple and computationally efficient
* Updates weights using:

  `w(n+1) = w(n) + μ x(n) e(n)`

---

### 🔹 NLMS (Normalized LMS)

* Improved version of LMS
* Faster convergence and stability
* Uses normalization based on input signal power:

  `w(n+1) = w(n) + (μ / ||x(n)||²) x(n) e(n)`

---

## 📊 Results

* Effective echo reduction observed in output signal
* NLMS shows faster convergence compared to LMS
* Error power decreases over iterations

---

## 📁 Project Structure

```
├── adaptive_echo_cancellation.ipynb   # Main Jupyter Notebook
├── README.md                         # Project documentation
```

---

## 🚀 How to Run

1. Clone the repository:

```
git clone https://github.com/your-username/adaptive-echo-cancellation.git
```

2. Install dependencies:

```
pip install numpy matplotlib
```

3. Run the Jupyter Notebook:

```
jupyter notebook
```

---

## 🛠️ Tools & Technologies

* Python
* NumPy
* Matplotlib
* Jupyter Notebook

---

## 📌 Applications

* Hands-free telephony
* Video conferencing systems
* Hearing aids
* Voice-controlled devices

---

## 🔮 Future Improvements

* Implementation using real audio signals (WAV files)
* Integration of RLS algorithm for faster convergence
* Real-time echo cancellation system
* Deep learning-based echo suppression

--- 

## 👨‍💻 Citation
Patil, A. P., and M. R. Patil, “Performance Analysis of Adaptive Filtering Algorithms for Acoustic Echo Cancellation,” International Journal of Engineering Research & Technology (IJERT), vol. 7, no. 8, Aug. 2018.
