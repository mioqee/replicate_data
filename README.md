# Personal Project: VHLSS (Vietnam Household Living Standard Survey)

## 🧠 Working Ideas File

🔗 https://docs.google.com/spreadsheets/d/1NHo0kn2O71mDjXBZyYbOe3yrdEdDOI4ifujwDu6o8OA/edit?gid=0#gid=0

---

## 🐍 Create Virtual Environment (Python)

```bash
python -m venv .venv
```

---

## 📦 Install Required Libraries

Only simple libraries are used.

```bash
pip install -r requirements.txt
```

---

## 📁 Dataset

👉 Download here:  
https://drive.google.com/file/d/1vG2iYbX8xnoRIbhGTc7Wq4ptsYtg6oEG/view?usp=sharing

Since the `data` folder is too large, it is stored on Google Drive.

After downloading `data.zip`, make sure to extract it to the correct location.

---

## 🗂️ Data Folder Structure

Make sure **no extra nested `data` folder** appears.

✅ Correct structure:

```
data
├── classify
├── dimension
├── non-use
```

---

## 🏗️ Full Project Skeleton

```
.venv
.gitignore
data
├── classify
├── dimension
├── non-use
├── survey_checkforprocessing
requirements.txt
preprocessing.ipynb
transform_and_clean.ipynb
```
## 📚 Additional Information About the `data` Folder

### 🚫 `non-use` folder
Contains datasets that are **not used** and **not required** for processing.

---

### 🧾 `dimension` folder
Contains data used for **mapping** and **redefining variables**.  
You can think of this as the **data dictionary / definitions**.

- Includes file **`dim.csv`**
- This file contains the meaning of each **`MUCxx.dta`** file in raw format

---

### 🔎 `survey_checkforprocessing` folder
Contains the **official survey details and requirements** that must be followed to correctly clarify and interpret the dataset for each **MUC**.

---

### 🏷️ `classify` folder

This folder contains:

```
classify
├── cleaned
├── raws
```

#### 📥 `raws`
- Each numbered folder corresponds to a module:
  
  ```
  1 → MUC1
  2 → MUC2
  ...
  8 → MUC8
  ```

- Folder **`HO`** contains summary data for each MUC at the **household level**

---

### 🔄 Variable Change Files

In some numbered folders, you will find files named:

```
variable_change_xx.md
```

These files document **variable renaming rules**, which directly affect the **column names** in the processed datasets.

⚠️ Make sure to check these files when working with column mappings.

