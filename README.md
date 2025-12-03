## Analysis of Stack Overflow 2024 Survey
### Source: [survey.stackoverflow.co](https://survey.stackoverflow.co/2024)
This analysis summarizes the feedback from the survey according to the title and shows significant insights from it.
### Libraries used
- pandas
- numpy
- matplotlib
- collections
- plotly
### Steps Followed
- Loaded .csv File for Analysis in Pandas.
- Used separate functions per analysis.
- Created a visual presentation of each survey question.
### Sample Function
A function that categorises the developer responses into 4 main areas:
```
def get_category_of_interest(cleaned_data, category_filter='All Respondents'):
    """ Filters a data frame  to get the category of interest."""
    
    filter_criteria = ['Professional Developer', 'Learning to Code', 'Other Coders', 'All Respondents']
    try:
        if category_filter not in filter_criteria:
            raise ValueError('Invalid filter criteria provided.')

        if category_filter == 'Professional Developer':
            return cleaned_data.loc[cleaned_data[cleaned_data.columns[0]] == 'I am a developer by profession']

        elif category_filter == 'Learning to Code':
            return cleaned_data.loc[cleaned_data[cleaned_data.columns[0]] == 'I am learning to code']

        elif category_filter == 'Other Coders':
            return cleaned_data.loc[~(
                (cleaned_data[cleaned_data.columns[0]] == 'I am a developer by profession') |
                (cleaned_data[cleaned_data.columns[0]] == 'I am learning to code')
            )]

        else:
            return cleaned_data  

    except ValueError as e:
        print(e)
        return None  
```
### Sample Visual
Visual representation of Median Annual Salary in USD Vs Work Experience:
![Line Chart.](linechartsample.png)
