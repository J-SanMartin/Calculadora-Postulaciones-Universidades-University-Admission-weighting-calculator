🌐 [Leer en Español](./README.md)

# University Application Calculator
The main objective of this project is to consolidate the weighting of the PAES admission tests required by each university in Chile for their respective careers and build a calculator that delivers an approximate application score. it's important to note that the caculator was built for a type A School: scientific-humanistic, wich changes the conversion table used in NEM score

## Project Overview
1. **Objective**:Extract the weight of each test required by the 47 universities affiliated to the centralized admission system to build an application calculator.
2. **Data source**: all data used in this project was obtained through DEMRE official site (https://demre.cl)
3. **Result**: .xlsx file with all the needed information to build the calculator

## Steps
1. **PDF**: DEMRE delivers all the information about the application process and universities in the file 'Oferta Definitiva_DEMRE' where we can find, text, tables and mixed layouts with information of the 47 universities affiliated to the process, that's why we generate a new PDF file named 'solo tablas' that only contains the tables with the information needed
2. **Data extraction** Using 'Camelot' in Python, we extract the information contained in the previously generated PDF, saving all the information into one DataFrame.
3. **Data cleaning**: Once we have the info we need in a DataFrame, we make adjustments to column names, set the corresponding university to each carrer, etc. During this process we find minor details or errors in the parse process, that are corrected in excel.
4. **Data export**: All the obtained information is extracted in .xlsx format to check minor details and implement in the calculator.
5. **Calculator**: We use the obtained data to build the application calculator for high school students of a scientific-humanistic school

## about the calculator
- all cells and sheets of the excel document are protected, so that the final users can only do inputs in the required cells
- Calculadora: sheet where users can input their data and expected scores in each test (highlighted in light blue)
- Universidades: All the information extracted from the PDF file
- COD_UNI: Index table with every university and their corresponding ID code
- NEM: Conversion table from school grades to NEM score, valid for the 2026 admission process. It's important to consider that the grading system in Chile goes from 1.0 to 7, and the conversion table vary for different types of school.
- Ranking: sheet used for the calculation of Ranking score. It's important to note that Means and Max used in each year are simulated and must be adjusted for every school.
- Carreras: Sheet used as a filter for the available carrers in the university that the user selected in the 'calculator' sheet
