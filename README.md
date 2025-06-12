# 📊 **Matplotlib: The Visual Language of Python**

### *A JupyterLab Documentary on Data Visualization*

---

## 🎬 Chapter 1: What is Matplotlib?

**Matplotlib** is a powerful Python library used to create static, animated, and interactive visualizations.

* Most commonly used module: `pyplot`
* Think of it like a drawing board for your data

```python
import matplotlib.pyplot as plt
```

---

## 🎬 Chapter 2: Your First Plot

```python
x = [1, 2, 3, 4, 5]
y = [2, 3, 5, 7, 11]

plt.plot(x, y)
plt.title("Prime Numbers")
plt.xlabel("Index")
plt.ylabel("Prime Value")
plt.show()
```

🧠 **Concepts Introduced**:

* `plot()`: draws a line
* `show()`: displays the figure
* `title()`, `xlabel()`, `ylabel()`: labels for clarity

---

## 🎬 Chapter 3: Different Plot Types

```python
# Line Plot
plt.plot([1, 2, 3], [4, 5, 6])

# Bar Plot
plt.bar(["A", "B", "C"], [10, 15, 7])

# Scatter Plot
plt.scatter([1, 2, 3], [4, 1, 6])

# Histogram
import numpy as np
data = np.random.randn(1000)
plt.hist(data, bins=30)
```

🧠 **Concepts Introduced**:

* Choose plot based on **data type and purpose**
* Histogram shows frequency; bar plot compares categories

---

## 🎬 Chapter 4: Styling the Plots

```python
plt.plot(x, y, color='green', marker='o', linestyle='--', linewidth=2)
plt.grid(True)
```

🧠 **Key Styling Options**:

* `color`, `marker`, `linestyle`
* `grid()` to add a background grid

| Option    | Example          |
| --------- | ---------------- |
| color     | 'red', '#FF8800' |
| marker    | 'o', '^', 's'    |
| linestyle | '-', '--', ':'   |
| linewidth | 1, 2, 3          |

---

## 🎬 Chapter 5: Multiple Plots on One Graph

```python
plt.plot(x, y, label="Prime Numbers")
plt.plot(x, [i**2 for i in x], label="Squares")
plt.legend()
```

🧠 **Concepts Introduced**:

* `label=` gives name to line
* `legend()` shows names

---

## 🎬 Chapter 6: Subplots (Multiple Graphs)

```python
fig, axs = plt.subplots(2, 2)  # 2x2 grid

axs[0, 0].plot(x, y)
axs[0, 1].bar(x, y)
axs[1, 0].scatter(x, y)
axs[1, 1].hist(data, bins=10)

plt.tight_layout()
```

🧠 **Concepts Introduced**:

* `subplots()` returns figure and axes array
* Each `ax` is like its own canvas

---

## 🎬 Chapter 7: Saving Your Figures

```python
plt.plot(x, y)
plt.savefig("my_plot.png")
```

🧠 Save plots in PNG, PDF, SVG, etc.

---

## 🎬 Chapter 8: Advanced Features (Optional Preview)

* **Animations**: using `FuncAnimation`
* **Interactive Plots**: with `%matplotlib notebook` or `plotly`
* **3D Plots**: via `mpl_toolkits.mplot3d`

---

## 🎬 Chapter 9: Matplotlib in JupyterLab

In JupyterLab, to ensure plots display:

```python
%matplotlib inline
```

✅ Place this at the **top of your notebook**

---

## 🎬 Bonus Chapter: Themes and Styles

```python
plt.style.use('ggplot')  # 'seaborn', 'bmh', 'dark_background', etc.
```

🧠 Use built-in styles for a quick aesthetic upgrade!

---

## 📘 Summary Table

| Concept      | Function                          |
| ------------ | --------------------------------- |
| Line Plot    | `plot()`                          |
| Bar Chart    | `bar()`                           |
| Scatter Plot | `scatter()`                       |
| Histogram    | `hist()`                          |
| Labels       | `title()`, `xlabel()`, `ylabel()` |
| Legend       | `legend()`                        |
| Grid         | `grid(True)`                      |
| Subplots     | `subplots()`                      |
| Save Plot    | `savefig()`                       |

---

## ✅ Ready-to-Use Cell for JupyterLab

```python
%matplotlib inline
import matplotlib.pyplot as plt
import numpy as np

x = np.linspace(0, 10, 100)
y = np.sin(x)

plt.plot(x, y, color="blue", label="Sine Wave")
plt.title("Sine Wave Example")
plt.xlabel("Time")
plt.ylabel("Amplitude")
plt.legend()
plt.grid(True)
plt.show()
```

---


