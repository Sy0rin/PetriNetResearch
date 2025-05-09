Absolutely — here's a clean, professional **README.md** you can use for your project. It explains the project, the Petri Net syntax, and how to use the tool.

---

## 🧠 Petri Net Syntax Translator & Simulator

A web-based tool for modeling, simulating, and analyzing **Petri Nets** using a **simple text-based syntax**, complete with:

* Visual graph rendering using Cytoscape.js
* Transition firing and reachability analysis
* Support for inhibitor arcs
* Import/export functionality

---

## 📄 Syntax Guide

Write your Petri Net model in the text area using the following commands:

### 🔵 `PLACE`

Defines one or more **places**.

```text
PLACE P1 P2 P3
```

### 🔴 `TRANSITION`

Defines one or more **transitions**.

```text
TRANSITION T1 T2
```

### ➡️ `ARC`

Creates a **directed arc** from a place to a transition or from a transition to a place.

```text
ARC P1 T1      # from place P1 to transition T1  
ARC T1 P2      # from transition T1 to place P2
ARC P2 T2 2    # optional weight (defaults to 1)
```

### 🚫 `INHIBITOR`

Creates an **inhibitor arc**, which prevents a transition from firing if the given place has any tokens.

```text
INHIBITOR P3 T1   # T1 is inhibited if P3 has any tokens
```

### 🔢 `MARKING`

Initial marking — assigns a **number of tokens** to places.

```text
MARKING P1 1 P2 0 P3 0
```

---

## 🚀 Features

* **Translate** text-based Petri Net descriptions to JSON and render them visually.
* **Simulate** transition firing based on the current marking.
* **Handle inhibitor arcs** (places that block transitions if tokens are present).
* **Visualize** the **Reachability Graph** (all reachable markings from the initial state).
* **Export** and **import** models as JSON.
* **Display all possible firing sequences** (step-by-step recursive analysis).

---

## 🖥️ Usage Instructions

1. Paste your Petri Net description into the text box.
2. Click **Translate** to build and render the Petri Net.
3. Click **Play** to simulate one valid set of transitions.
4. Click **Transition Map** to view all possible markings and firing paths (recursively generated).
5. Click **Reachability Graph** to see the full state-space as a graph.
6. Use **Download JSON** to save your net, or **Upload JSON File** to reload one.

---

## 📌 Example Petri Net Input

```text
PLACE P1 P2 P3
TRANSITION T1 T2
ARC P1 T1
ARC T1 P2
ARC P2 T2
ARC T2 P3
INHIBITOR P3 T1
MARKING P1 1 P2 0 P3 0
```

---

## 🛠 Technologies Used

* [Cytoscape.js](https://js.cytoscape.org/)
* [jQuery](https://jquery.com/)
* [Tailwind CSS](https://tailwindcss.com/)
* [Bootstrap 5](https://getbootstrap.com/)

---