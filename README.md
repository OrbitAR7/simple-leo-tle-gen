# **LEOTLE Constellation Generator**

A lightweight app for generating and visualizing LEO satellite constellations (Walker configurations), producing valid TLE files and interactive Earth-map visualizations.

---

## **Features**

* Generate Two-Line Element (TLE) files for custom LEO constellations
* Support for Walker Delta and Circular configurations
* Visualize satellite orbits and positions on a realistic Earth map
* Download generated TLE files and plots
* Simple, interactive Streamlit interface

---

## **Installation & Running the App**

### **1. Requirements**

* Python **3.9+**
* `pip`

### **2. (Optional but recommended) Create a virtual environment**

```sh
python -m venv venv
source venv/bin/activate
```

### **3. Install dependencies**

```sh
pip install -r requirements.txt
```

### **4. Launch the app**

```sh
streamlit run streamlit_app.py
```

### **5. Open the link in your terminal**

Streamlit will print a local URL (e.g., `http://localhost:8501`).
Open it in your browser to start using the tool.

---

## **Notes**

* If any modules are missing, you can install them manually with `pip install <package>`.
* Using a virtual environment avoids dependency conflicts.
* **Future versions** will include:

  * Repeat-ground-track constellation generation
  * Additional visualization modes

