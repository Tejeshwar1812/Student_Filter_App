# 📘 Learnbasics Assignment Reference Guide

## 🎯 Task Overview

This assignment consists of **three main parts**:

1. **Creating a PostgreSQL Database on Render**
2. **Connecting the Database to Appsmith**
3. **Building an Appsmith Application** with dropdown filters to display student data dynamically.

---

## 🧩 Work done

- Used [Render](https://render.com) to **create a free PostgreSQL database**.
- Used **pgAdmin 4** to manage the PostgreSQL database and **import sample data**.
- Created an **Appsmith application** that:
  - Connected to PostgreSQL database
  - Included **dropdowns** for filtering by:
    - School Name
    - Class
    - Section
  - Displays the **filtered student data** in a table.
---

## 📋 Sample Features

- PostgreSQL schema to store student data.
- Dropdown UI elements for real-time filtering.
- Responsive Appsmith UI bound to SQL queries.
- SQL logic using dynamic bindings like:

  ```sql
  SELECT * FROM student_data
  WHERE school_name LIKE {{ SchoolDropdown.selectedOptionValue ? `'${SchoolDropdown.selectedOptionValue}'` : "'%'" }}
    AND class LIKE {{ ClassDropdown.selectedOptionValue ? `'${ClassDropdown.selectedOptionValue}'` : "'%'" }}
    AND section LIKE {{ SectionDropdown.selectedOptionValue ? `'${SectionDropdown.selectedOptionValue}'` : "'%'" }};
