# 📊 Tech Community Profile Parser & Analyzer

_Extracting, cleaning, and analyzing unstructured social media profile data of the tech and startup community into structured formats using Python._

---

## 📌 Table of Contents
- <a href="#overview">Overview</a>
- <a href="#objective">Objective</a>
- <a href="#dataset">Dataset</a>
- <a href="#tools--technologies">Tools & Technologies</a>
- <a href="#project-structure">Project Structure</a>
- <a href="#data-cleaning--preparation">Data Cleaning & Preparation</a>
- <a href="#exploratory-data-analysis">Exploratory Data Analysis</a>
- <a href="#how-to-run-this-project">How to Run This Project</a>
- <a href="#future-scope">Future Scope</a>
- <a href="#author--contact">Author & Contact</a>

---
<h2><a class="anchor" id="overview"></a>Overview</h2>

This project processes raw, unstructured text data containing social media profiles of tech professionals, developers, founders, and communities. A complete data extraction pipeline was built using Python to parse, clean, and convert this text data into a structured JSON format, enabling subsequent exploratory data analysis to identify top influencers and community niches.

---
<h2><a class="anchor" id="objective"></a>Objective</h2>

Extracting insights from raw text dumps requires rigorous formatting. This project aims to:
- Process unstructured block-text data into individual profile records.
- Clean and normalize numerical metrics (e.g., converting "K" and "M" string suffixes into actual integers).
- Export the sanitized dataset into a structured JSON format.
- Perform exploratory analysis to identify profiles with the highest engagement metrics and categorize the community distribution.

---
<h2><a class="anchor" id="dataset"></a>Dataset</h2>

- Unstructured text files containing chunked profile information.
- **Data Attributes Parsed:** `username`, `no_of_posts`, `no_of_followers`, `no_of_following`, `name`, `type_of_page`, and `bio`.
- **Files used:** `initialdata.txt` (raw sample) and `finaldata.txt` (main text data for processing). The cleaned output is stored in `data.json`.

---

<h2><a class="anchor" id="tools--technologies"></a>Tools & Technologies</h2>

- **Programming Language:** Python 3
- **Environment:** Jupyter Notebooks
- **Data Formats:** Text (`.txt`), JSON (JavaScript Object Notation)
- **Concepts:** Data Parsing, String Manipulation, File I/O, Set Operations

---
<h2><a class="anchor" id="project-structure"></a>Project Structure</h2>

```text
social-media-parser/
│
├── README.md
│
├── coders_of_bd.ipynb           # Main Jupyter notebook for parsing & analysis
│
├── data.json                    # Structured output dataset
│
└── data/                        # Raw text datasets
    ├── initialdata.txt
    └── finaldata.txt
```
<h2><a class="anchor" id="data-cleaning--preparation"></a>Data Cleaning & Preparation</h2>

The raw text data (finaldata.txt) contained formatting inconsistencies. The parsing pipeline (coders_of_bd.ipynb) handled:

Data Chunking: Split the raw text using double newlines (\n\n) to isolate individual profiles and filtered out invalid chunks.

Metric Normalization: Stripped strings like " followers" and " following", removed commas, and mathematically converted values containing "K" (x1,000) and "M" (x1,000,000) into standard integers.

Missing Data Handling: Added conditional logic to assign "Unknown" to type_of_page and an empty string to bio if those fields were missing.

The parsed dictionaries were successfully exported as data.json for downstream use.

<h2><a class="anchor" id="exploratory-data-analysis"></a>Exploratory Data Analysis</h2>

1. Top Profile Identification

Logic: Iterates through the structured data to find maximum values for specific engagement metrics.

Outcomes: Successfully identified the accounts with:

Highest number of posts: startuphub_blr

Maximum followers: _anujsinghal

Maximum following: bangalore_tech_bro

2. Community Categorization

Logic: Extracts the type_of_page for all profiles and stores them in a Python set() to remove duplicates.

Outcomes: Identified 34 unique profile categories within the dataset (e.g., Media, Community, Developer, Entrepreneur).

<h2><a class="anchor" id="how-to-run-this-project"></a>How to Run This Project</h2>

Clone the repository:

Bash
git clone [https://github.com/tamimikbalcontact-prog/Analyzing-data-using-python.git](https://github.com/tamimikbalcontact-prog/Analyzing-data-using-python.git)
Navigate to the project directory and launch Jupyter:

Bash
jupyter lab
Open and run the notebook:

Plaintext
Open coders_of_bd.ipynb and execute the cells sequentially to parse the text data, generate data.json, and view the analysis outputs.
<h2><a class="anchor" id="future-scope"></a>Future Scope</h2>

Implement visual charts (bar charts, scatter plots) using Matplotlib or Seaborn to visualize follower vs. following ratios.

Migrate from static text parsing to fetching live data using official social media APIs.

Introduce NLP (Natural Language Processing) to perform keyword and sentiment analysis on the user bios.

<h2><a class="anchor" id="author--contact"></a>Author & Contact</h2>

Md. Tamim Ikbal Data Science

📧 Email: tamimikbal.contact@gmail.com