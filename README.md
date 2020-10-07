# Pandas Challenge

## Use **Pandas and Jupyter Notebook** to analyze a large data set

### *Please look inside the jupyter notebook for notes within the python code and in markdown cells.*

This analysis is for a ficticious gaming software company; PyMoli. 

## **The code is designed to work in Jupyter Notebook. Viewing in other software might not render the HTML formatiing correctly**

The exercises are designed to use Pandas to perform calculations on large datasets and return tables of data to the screen (dataframes)

First Pandas was used to read a .csv file into a dataframe :

    - df = pd.read_csv()
    
Later dataframes were created from the results of pandas methods:

    - df =pd.DataFrame({})

Pandas dataframe methods used include:

    1. dtypes() - Were used to determine data type but removed before final code was submitted
    2. nunique() - Count unique values
    3. mean() - Calculate Mean (Average)
    4. count() - Count entries
    5. sum() - Calculate sum of table column
    6. concat() - Concatenate two dataframes - must have the same rows!
    7. drop_duplicates() - Remove duplicate values from a dataframe
    8. sort_values() - Sort values in the dataframe based on column and ascending/descending as specified
    9. groupby() - Creates a dataframe groupby object that is grouped by the data in column(s) specified. This oject can then be used to gather useful statistics about the dataset 
    10. head() - Displays the first 5 rows in a dataframe(or more if specified) as well as the column titles
   
Pandas binning was also used to group data into age groups for analysis of purchasing patterns by age group:

    1. bins = [0,9.99,14.99,19.99,24.99,29.99,34.99,39.99,120]
    2. age_group = ["<10",'10-14','15-19','20-24','25-29','30-34','35-39','40+']
    3. pd.cut() [More about cut](https://pandas.pydata.org/pandas-docs/stable/reference/api/pandas.cut.html?highlight=cut#pandas.cut)
    
To display the data in desired formats two methodologies were used:

    1. map("{:.2f}%".format) to change the values to percentage format for display purposes. (note: Do not use this untill all calculations have been done. The format mapping changes the entries to objects)

    2. IPython.display HTML was used to align headers and table cells to improve readability of output
    
            ```from IPython.display import HTML

            styles = [
                dict(selector="td", props=[("font-size", "100%"),
                                           ("text-align", "center")]),
                dict(selector="th", props=[("font-size", "110%"),
                                           ("text-align", "center")]),
            ]
            html = age_demographics_df.style.set_table_styles(styles)
            html