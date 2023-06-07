This repository focuses on converting Excel files into JSON format, primarily intended for data uploading into MongoDB. The conversion process utilizes the pandas library, which can be installed via the following command:

pip install pandas

Additionally, the repository relies on the openpyxl library for handling Excel files. If openpyxl is not already installed in your environment, you can install it using the following command:

pip install openpyxl

These dependencies are necessary for the smooth execution of the Excel-to-JSON conversion functionality provided by this repository.

Import the pandas library using import pandas as pd. This library provides powerful data manipulation and analysis tools.

Load an Excel file into a pandas DataFrame using df = pd.read_excel('demo.xlsx'). The read_excel() function reads the Excel file named "demo.xlsx" and creates a DataFrame object called df to store the data.

Convert the DataFrame into a JSON string using json_data = df.to_json(orient='records'). The to_json() method converts the DataFrame df into a JSON string representation. The orient='records' parameter ensures that each row of the DataFrame is represented as a separate JSON object.

Save the JSON data to a file named "output.json" using with open('output.json', 'w') as file: file.write(json_data). The with statement opens the file in write mode, and the JSON data stored in the json_data variable is written to the file. After writing, the file is automatically closed.

At the end user will get JSON file (untracked form).

User can convert untracked form into tracked form using these steps :

Alt + Shift + F

By following these steps, the code loads an Excel file, converts its contents into JSON format, and saves the resulting JSON data to a file. This can be useful for tasks such as uploading data from Excel to MongoDB.