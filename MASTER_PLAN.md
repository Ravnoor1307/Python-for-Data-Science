# 🗺️ MASTER PLAN — 00_Python (DS + AI Prerequisites Journey)

> ⭐ **Ye file hamari permanent memory hai.** Har topic ka structure, type
> (THEORY/PRACTICAL), notebooks, aur dataset mapping — sab yahin hai.
> Jab-jab topics complete honge, status update hota rahega.

**Journey root (workspace ke top level):**
`00_Python/` · `01_SQL/` · `02_Mathematics/` · `03_Software_Essentials/` ·
`04_Cloud_Fundamentals/` · `05_AI_Coding/` · `06_DSA_FOR_AI/` ·
`07_Data_Analysis_Process/` · `99_Prerequisites_Projects/`

---

## 📜 GROUND RULES (har topic ke notebooks me follow honge)

### Input format (user bhejega)
```
FOLDER: [subfolder name]
TOPICS: [topic 1], [topic 2], ...
```

### Har TOPIC ke liye
1. Numbered subfolder (spaces → underscores) — e.g. `07_Joins/`
2. Notebooks: `01_..._theory.ipynb` → `02_..._practical.ipynb` → `03_..._advanced.ipynb`
   (har .ipynb = ONE focused lesson)
3. `task.ipynb` — **SIRF PRACTICAL topics** me (5–8 tasks, EASY→HARD, hints
   dheere-dheere, starter code TODO ke saath, ✅ solutions LAST section me)
4. `README.md` — **hamesha** (5-line summary, real-world analogy, files list,
   syntax/formula cheat sheet, common mistakes table, "Aage kya" link)

### 👨‍🏫 Teacher Mode — progression pattern (HAR notebook)
🌍 Real-world hook → 📖 Simple definition (1 line) → 🔍 WHY (bina iske kya problem)
→ 📊 Visual (ASCII diagram/table) → 🐣 Basic example → 🐥 Intermediate →
🐔 Advanced → ⚠️ Common mistakes → 📌 Recap (bullets)

### Style rules
- Language: **HINGLISH** (technical terms English me, tone: "Dekho, ye concept
  bilkul waise hi hai jaise...")
- Cell markers: `# %% [markdown]` / `# %%` (jupytext / VS Code compatible)
- Code: WORKING + Hinglish comments + `# Expected OUTPUT:`
- DSA topics: Time/Space complexity **WITH full calculation**
  (bina calculation ke sirf O(?) likhna = 🚫 FORBIDDEN)
- Math/ML: visual diagrams jahan possible ho
- ⚡ Quality: files COMPLETE — cut/summary allowed nahi.
  Lamba content ho toh user "continue" bolega, tab agla part.

---

## 📂 00_Python — FULL STRUCTURE & NOTEBOOK MAP

Legend: 📊 = dataset linked · 📝 = task.ipynb included

### ✅ 00_Resources/ — **READY (2026-09-16)**
```
playlist_links.md · docs_links.md
datasets/: generate_data.py, DATASETS_INFO.md, EXTERNAL_DATASETS.md
  + students_marks.csv, sales_data.csv, sales_data.json, employee_data.csv,
    employee_data_GANDA.csv, weather_data.csv, products_catalog.csv,
    Zomato_mini_dataset.csv, student_notes.txt
```

### 01_Python_Core_Fundamentals/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Syntax_Indentation_PEP8 | THEORY | 01_syntax_indentation_theory, 02_pep8_style_guide | — (no task) |
| 02 | Variables_DataTypes_TypeCasting | PRACTICAL 📝 | 01_variables_theory, 02_data_types_deep_dive, 03_type_casting | chhote examples |
| 03 | Input_Output_Comments_Docstrings | PRACTICAL 📝 | 01_input_output_theory, 02_print_formatting_fstrings, 03_comments_docstrings | input() examples |
| 04 | Control_Flow_IfElse_Loops | PRACTICAL 📝 | 01_if_else_elif_theory, 02_for_while_loops, 03_break_continue_pass, 04_nested_loops_patterns | 📊 students_marks.csv |
| 05 | Functions_Arguments_Return | PRACTICAL 📝 | 01_functions_basics_theory, 02_arguments_types, 03_return_values_scope | 📊 students_marks.csv → calculate_grade(), is_pass(), class_average() |
| 06 | Lambda_Functions | PRACTICAL 📝 | 01_lambda_theory, 02_lambda_with_map_filter | 📊 products_catalog.csv → 10% discount map, price>500 filter |
| 07 | Comprehensions | PRACTICAL 📝 | 01_list_comprehension_theory, 02_dict_set_comprehensions, 03_nested_conditional_comprehensions | 📊 sales_data.csv → category lists, high-qty filter |

### 02_Built_in_Data_Structures/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Lists | PRACTICAL 📝 | 01_lists_theory, 02_list_methods_operations, 03_list_slicing_indexing | 📊 students_marks.csv (list of lists, top 10 slicing) |
| 02 | Tuples | PRACTICAL 📝 | 01_tuples_theory, 02_tuples_vs_lists_packing_unpacking | 📊 employee_data.csv (records as tuples, unpacking) |
| 03 | Sets | PRACTICAL 📝 | 01_sets_theory, 02_set_operations | 📊 sales_data.csv (unique cities/products, 2-month intersection) |
| 04 | Dictionaries | PRACTICAL 📝 | 01_dicts_theory, 02_dict_methods_nested | 📊 employee_data.csv ({emp_id: details}, dept-wise count) |
| 05 | Strings | PRACTICAL 📝 | 01_strings_theory_immutability, 02_string_methods, 03_slicing_formatting | 📊 employee_data.csv (name formatting, city cleaning) |
| 06 | Arrays | PRACTICAL 📝 | 01_arrays_module_theory, 02_array_vs_list_comparison | 📊 weather_data.csv (temp array, memory comparison) |

### 03_Pythonic_Thinking/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Iterators_Generators | PRACTICAL 📝 | 01_iterators_theory, 02_generators_yield | 📊 sales_data.csv lazy row-by-row (memory bachao) |
| 02 | Zip_Enumerate_Map_Filter_Reduce | PRACTICAL 📝 | 01_zip_enumerate_theory, 02_map_filter_reduce | 📊 students + products (names+marks zip, ranks) |
| 03 | Shallow_vs_Deep_Copy | THEORY | 01_copy_concepts_theory, 02_memory_diagrams_demo | nested dict copy 🤯 demo |
| 04 | Mutability_vs_Immutability | THEORY | 01_mutability_theory, 02_memory_behavior_experiments | id() memory experiments |
| 05 | Args_Kwargs | PRACTICAL 📝 | 01_args_kwargs_theory, 02_unpacking_use_cases | 📊 products → flexible *args discount function |

### 04_OOP/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Classes_Objects | PRACTICAL 📝 | 01_classes_objects_theory, 02_creating_first_class | Student class (marks.csv → objects) |
| 02 | Constructors_Instance_Class_Vars | PRACTICAL 📝 | 01_init_constructor_theory, 02_instance_vs_class_variables | Student + BankAccount (total_students count) |
| 03 | Methods_Dunder_Methods | PRACTICAL 📝 | 01_instance_class_static_methods, 02_dunder_magic_methods | Product class: __str__, __lt__ (sorting) |
| 04 | Inheritance_Overriding | PRACTICAL 📝 | 01_inheritance_types_theory, 02_method_overriding_super | Person→Student→GradStudent; Employee→Manager |
| 05 | Polymorphism | PRACTICAL 📝 | 01_polymorphism_theory, 02_duck_typing_overloading | Shape family: Circle, Rectangle, Triangle area() |
| 06 | Encapsulation_Abstraction | PRACTICAL 📝 | 01_encapsulation_private_protected, 02_abstraction_abc | BankAccount private balance, getter/setter |
| 07 | Dataclasses | PRACTICAL 📝 | 01_dataclass_decorator_theory, 02_dataclass_real_usecases | 📊 employee_data.csv → 100 clean objects (DS pipelines!) |

### 05_Error_Handling_Debugging/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Exceptions_TryExceptFinally | PRACTICAL 📝 | 01_exceptions_theory, 02_try_except_else_finally, 03_common_builtin_exceptions | 📊 GANDA data → ValueError/FileNotFoundError handling |
| 02 | Custom_Exceptions | PRACTICAL 📝 | 01_custom_exceptions_theory | InvalidMarksError (marks > 100) |
| 03 | Common_Runtime_Errors | THEORY | 01_common_errors_reference, 02_debugging_techniques | errors intentionally generate |

### 06_Modules_Packages_Environments/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Import_System | PRACTICAL 📝 | 01_import_from_as_theory | math, random, datetime imports |
| 02 | Creating_Modules_Packages | PRACTICAL 📝 | 01_own_modules_theory, 02_packages_structure | apna grade_utils.py module |
| 03 | Virtual_Environments | PRACTICAL (no task — terminal) | 01_venv_theory_setup, 02_conda_uv_environments | terminal commands |
| 04 | Dependency_Management | PRACTICAL (no task — terminal) | 01_pip_requirements_theory, 02_uv_poetry_basics | requirements.txt banana |
| 05 | Understanding_Main | THEORY | 01_name_main_theory, 02_script_vs_module_demo | 2 .py files interaction |

### 07_File_Handling_Serialization/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Text_Files | PRACTICAL 📝 | 01_file_reading_writing_theory, 02_with_statement_modes | 📄 student_notes.txt (create/read/append) |
| 02 | CSV_JSON | PRACTICAL 📝 | 01_csv_handling_theory, 02_json_handling_theory | 📊 sales_data.csv + sales_data.json |
| 03 | Pickle | PRACTICAL 📝 | 01_pickle_theory_pros_cons | objects pickle (ML model save preview — joblib ka bhai) |
| 04 | Directories_os_pathlib | PRACTICAL 📝 | 01_os_module_theory, 02_pathlib_modern_way | folder structure create/explore |
| 05 | Logging_to_Files | PRACTICAL 📝 | 01_logging_basics_theory, 02_logging_levels_config | sales processing log file |

### 08_Numerical_Computing_NumPy/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Arrays_Shapes_Dtypes | PRACTICAL 📝 | 01_numpy_arrays_theory, 02_shapes_dtypes_reshape, 03_indexing_slicing_numpy | 📊 students_marks.csv → (50×5) array |
| 02 | Broadcasting | PRACTICAL 📝 | 01_broadcasting_theory_rules, 02_broadcasting_visual_examples | 📊 products → 18% GST scalar broadcast |
| 03 | Vectorized_Operations | PRACTICAL 📝 | 01_vectorization_vs_loops_theory, 02_aggregations_axis | 📊 weather 365 days → loop vs vectorized ⚡ |
| 04 | Linear_Algebra_Basics | PRACTICAL 📝 | 01_matrix_operations_numpy, 02_solving_equations_numpy | synthetic matrices (ML weights jaisa) |
| 05 | Random_Sampling | PRACTICAL 📝 | 01_random_module_theory, 02_distributions_sampling | dice/coin sims, normal distribution |

### 09_Data_Analysis_Pandas/  ⭐ CampusX DSMP datasets mapped!
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Series_DataFrames | PRACTICAL 📝 | 01_series_theory, 02_dataframes_theory, 03_creating_reading_data | batsman_runs_ipl, kohli_ipl, subs; movies, bollywood; attendance (Excel) |
| 02 | Indexing_Filtering | PRACTICAL 📝 | 01_loc_iloc_theory, 02_boolean_filtering_query | matches (season/city/winner), imdb-top-1000 |
| 03 | GroupBy_Aggregation | PRACTICAL 📝 | 01_groupby_theory_split_apply, 02_multiple_aggregations | ipl_deliveries ⭐, IPL_Matches, retail_sales, carvana |
| 04 | Missing_Values | PRACTICAL 📝 | 01_missing_values_detection, 02_fillna_dropna_strategies | employee_1000_with_missing ⭐, Titanic (age/cabin) |
| 05 | Merging_Joining | PRACTICAL 📝 | 01_merge_concat_join_theory, 02_concat_vertical_stacking, 03_real_world_merging | customers+orders+products+payments ⭐⭐, reg-month1/2, quarters 1/2/3, matches+deliveries |
| 06 | TimeSeries_Basics | PRACTICAL 📝 | 01_datetime_indexing_theory, 02_resampling_rolling | expense_data ⭐, google stock (59MB), covid time_series, PowerGeneration |

> ⚠️ **CampusX datasets note:** Ye real files user ke local machine pe hain.
> Section 09 start hote hi: user upload karega YA main CampusX GitHub (raw) se
> fetch karunga; fallback = hamare synthetic datasets (students/sales/employee)
> se same concepts. Lessons me pehle synthetic pe concept, phir real pe practice.

### 10_Data_Visualization/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Matplotlib | PRACTICAL 📝 | 01_matplotlib_basics_theory, 02_line_scatter_bar_charts, 03_subplots_customization | 📊 weather (line/bar/scatter) |
| 02 | Seaborn | PRACTICAL 📝 | 01_seaborn_theory_distributions, 02_categorical_heatmap_plots | 📊 students (hist), employee (boxplot dept-wise) |
| 03 | Plotly | PRACTICAL 📝 | 01_plotly_interactive_theory, 02_interactive_charts | 📊 sales — hover pe details! |
| 04 | Plot_Types_for_EDA | PRACTICAL 📝 | 01_which_plot_when_theory, 02_eda_plots_in_action | 📊 Zomato_mini ⭐ complete mini-EDA |

### 11_Standard_Library/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | os_sys | PRACTICAL 📝 | 01_os_sys_theory | system operations |
| 02 | pathlib | PRACTICAL 📝 | 01_pathlib_theory | datasets folder programmatically explore |
| 03 | datetime_time | PRACTICAL 📝 | 01_datetime_theory, 02_time_calculations | 📊 weather dates |
| 04 | math_random | PRACTICAL 📝 | 01_math_random_theory | math formulas + dice games |
| 05 | logging | PRACTICAL 📝 | 01_logging_module_theory | pipeline logging |

### 12_Async_Parallel_Python/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Multithreading_vs_Multiprocessing | THEORY+DEMO | 01_concepts_theory, 02_comparison_demo | badi file parallel read demo |
| 02 | Async_Await | PRACTICAL 📝 | 01_async_await_theory, 02_async_examples | 3 fake API calls parallel |
| 03 | Async_IO_Basics | PRACTICAL 📝 | 01_asyncio_basics_theory | multiple downloads simulate |
| 04 | When_to_Use_Each | THEORY | 01_decision_guide_theory | decision flowchart |

### 13_Other_Libraries/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | FastAPI | PRACTICAL 📝 | 01_fastapi_basics_theory, 02_building_first_api | 📊 students API se serve |
| 02 | Pydantic | PRACTICAL 📝 | 01_pydantic_validation_theory | Student model validation (age 0–100) |
| 03 | Flask_WebDev | PRACTICAL 📝 | 01_flask_basics_theory, 02_routes_templates | 📊 products website |
| 04 | Streamlit_Dashboards | PRACTICAL 📝 | 01_streamlit_theory, 02_building_data_app | 📊 Zomato explorer app ⭐ |
| 05 | Dash_Plotly_Dashboards | PRACTICAL 📝 | 01_dash_theory_layouts | 📊 sales dashboard |
| 06 | Tkinter_GUI | PRACTICAL 📝 | 01_tkinter_basics_theory | marks calculator GUI |
| 07 | PyQt_GUI | PRACTICAL 📝 | 01_pyqt_basics_theory | employee manager desktop app |
| 08 | Gradio_AI_Demos | PRACTICAL 📝 | 01_gradio_theory, 02_ml_model_demo_app | marks-predictor demo (ML ke baad reuse 🔥) |

### 14_Production_Ready_Mindset/
| # | Topic | Type | Notebooks | Data/Concept |
|---|-------|------|-----------|--------------|
| 01 | Clean_Readable_Code | THEORY | 01_clean_code_principles_theory, 02_before_after_examples | GANDA code vs CLEAN code |
| 02 | Modular_Design | THEORY | 01_modular_design_theory, 02_refactoring_demo | 1 badi script → 3 clean modules |
| 03 | Logging_Monitoring_Mindset | THEORY | 01_logging_mindset_theory | concept examples |
| 04 | Reading_Others_Code | THEORY | 01_reading_code_strategies_theory | GitHub mini repo padhna |

### 99_Practice_Projects/ (00_Python ke andar)
| Project | Data/Concept |
|---------|--------------|
| mini_calculator | pure logic |
| todo_list_cli | todo_data.json (JSON save) |
| password_generator | random module |
| file_organizer | messy test_folder organize |
| web_scraper_basics | live website → CSV |

**Counts:** 14 sections · 74 topics · ~63 practical (task 📝) · ~11 theory-only

---

## 📊 DATASETS MASTER TABLE (00_Resources/datasets/ me READY ✅)

| Dataset | Rows | Columns | Kis Section Me |
|---|---|---|---|
| students_marks.csv | 50 | name, roll_no, math, science, english, hindi, computer, age, city | Loops, Functions, Lists, NumPy, Seaborn, FastAPI |
| sales_data.csv | 500 | order_date, product_name, category, quantity, unit_price, region | Comprehensions, Sets, Generators, GroupBy, Merge, Plotly |
| sales_data.json | 500 | (same as CSV) | JSON handling |
| employee_data.csv | 100 | emp_id, name, department, salary, join_date, city, experience_years | Tuples, Dicts, Strings, Dataclasses, Filtering |
| employee_data_GANDA.csv | 100 | (same + NaN 15%, -ve salary 5, duplicates 8, mixed formats) | Missing Values, Error Handling |
| weather_data.csv | 365 | date, temperature, humidity, rainfall_mm, city (Delhi 2024, seasonal!) | Arrays, NumPy Vectorized, Matplotlib, TimeSeries |
| products_catalog.csv | 30 | product_id, product_name, category, price, stock (15 sold + 15 unsold → JOIN demos) | Lambda, OOP, Broadcasting, Flask, Merge partner |
| Zomato_mini_dataset.csv | 100 | restaurant_name, cuisine, rating, cost_for_two, city, online_order | EDA Plots, Streamlit ⭐ |
| student_notes.txt | — | text | File Handling |

Regenerate: `cd 00_Python/00_Resources/datasets && python3 generate_data.py`
External/Kaggle links → `EXTERNAL_DATASETS.md`

---

## 🗓️ PROGRESS TRACKER

Legend: ✅ done · 🔨 in-progress (n/x topics) · ⬜ pending
Build system: `_build/ipynb_builder.py` (percent `# %%` source → real .ipynb,
code cells execute hoke outputs embed hote hain — sources `_build/src/` me).

| Section | Status |
|---|---|
| 00_Resources | ✅ DONE (2026-09-16) |
| 01_Python_Core_Fundamentals | ✅ 7/7 COMPLETE! 🎉 (01→07 all topics shipped: Syntax → Comprehensions) |
| 02_Built_in_Data_Structures | ✅ 6/6 COMPLETE! 🎉 (01_Lists → 06_Arrays all shipped; 181 code cells, 0 errors) |
| 03_Pythonic_Thinking | ✅ 5/5 COMPLETE! 🎉 (01_Iterators_Generators → 05_Args_Kwargs all shipped; 99 code cells, 0 errors) |
| 03_Pythonic_Thinking | ⬜ |
| 04_OOP | ✅ (7 topics + BankAccount BONUS capstone) |
| 05_Error_Handling_Debugging | ✅ (3 topics — 05.01 GANDA-cleaner + 05.02 MarksGate + 05.03 reference/debug) |
| 06_Modules_Packages_Environments | ✅ (3 topics — imports shield + own-modules lab + env-castles) |
| 07_File_Handling_Serialization | ✅ (5 topics — text-fortress + CSV/JSON conversion-cross + pickle-vault + directory-maze + logging-tower) |
| 08_Numerical_Computing_NumPy | ✅ (5 topics — array-arena + broadcast-blasts + vector-turbo + linalg-kingdom + casino-lab) |
| 09_Data_Analysis_Pandas | ⬜ |
| 10_Data_Visualization | ⬜ |
| 11_Standard_Library | ⬜ |
| 12_Async_Parallel_Python | ⬜ |
| 13_Other_Libraries | ⬜ |
| 14_Production_Ready_Mindset | ⬜ |
| 99_Practice_Projects | ⬜ |
