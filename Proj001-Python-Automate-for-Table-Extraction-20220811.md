# Python Automate for Table Extraction Projects
11 Aug 2022
## Welcome! Selamat Datang! Irasshaimase!-いらっしゃいませ, Huānyíng!-欢迎, Bienvenidos, 
Eoseo osibsio!-어서 오십시오, Svaagat!-स्वागत, Dobro pozhalovat'!-Добро пожаловать, Bienvenue, 'Ahlan wasahlan!-,أهلا وسهلا

# Table Extraction (Basic for Beginner)

## Objectives
Operating **VSCode, Jupyter Notebook, Kaggle and Colab in Windows** to
> 1. Extract Table from file
>    Type of **file HTML, CSV and text-based PDF**
> 2. Practice (In order of section)
>    * Preparation - Prepare the Virtual Environment
>    * python
>    * pip 
>    * pandas
>    * lxml
>    * jupyter notebook
>    * VSCode
>    * tkinter
>    * ghostscript
>    * camelot

## Note:
> 1. Please **take your time to Read, Understand,** ***PRACTICE, PRACTICE, PRACTICE,*** and **Solve the problems Independently** before asking 
>    **Question**. *Like a detective solving his/her cases.* These will help you build self-reliance and grow to challenges. **Keep Curious, Passionate and Healthy**.
> 2. **Beginner or Newbie** should start learning by **focusing** only 1(one) operating system (e.g. Windows, Linux or macOS) and 1(one) IDE 
>    and/or Code Editor (e.g. VSCode, Anaconda, Sublime, etc). After understanding then move to Jupyter Notebook and/or Kaggle and/or Other 
>    Notebooks that you prefer. Codes in this article are for VSCode, code for jupyter notebook or other notebook nearly the same.
> 3. The projects in this article are operating in **Windows** and **VSCode**.
> 4. Certain problem solving challenges might be available in the end of the notebook and questions are welcomed. 
> 5. **Keep your spirit! Semangat! Ganbatei!-がんばって, Jiā yóu!-加油 Espíritu!, Hwaiting!-화이팅, Aatma!-आत्मा, Dukh!-дух, Esprit, Hamasa!-حَمَاسَة**
> 6. Share articles to be of use to others under Copyright 2022 Wahyu Ardhitama.

Thank you! Terima kasih! Arigatōgozaimashita!-ありがとうございました, Xièxiè nǐ!-谢谢你, Gracias!, Gamsahabnida!-감사합니다, Dhanyavaad!-धन्यवाद, 
Spasibo!-cпасибо, Merci, shkran lak!-شكرًا لك

## Let Us Begin Our Practice!

## Preparation 
## Operating in IDE and/or Code Editor (e.g. VSCode, Anaconda, Sublime, etc.)
Create a folder for your project, for example folder name "Automate with Python Table Extract" and open it in VSCode.
Example preparation in **VSCode**: 
> 1. From PowerShell (PS) change to Command Prompt type:
>    * cmd
> 2. In command terminal type pip list or pip show: 
>    * pip list          
>    * pip show virtualenv
> 3. Check for virtualenv availability
> 4. If virtualenv unavailable type in terminal:
>    * pip install virtualenv
>    * python -m venv venv   
>    * venv\Scripts\activate.bat
> 5. Look in the list for pandas, lxml, jupyter, tk ghostscript and camelot-py availability. If unavailable type in command terminal:
>    * pip list (optional if you need to see it again or just scroll from the previous list)
>    * pip show pandas lxml jupyter tk ghostscript camelot-py[all](optional if you feel better using pip show. If too much to see the mentioned libraries, show one-by-
       one)
>    * pip install pandas
>    * pip install lxml       
>    * pip install jupyter
>    * pip install tk
>    * pip install ghostscript
>    * pip install camelot-py[all]

If you want to go back to PowerShell type: powershell

## Operating in Jupyter Notebook
**Recommended** to use the jupyter notebook before kaggle as we can create an environment.
Example in **VSCode**
> 1. After going through point 1 to 5 of the previous section then start Jupyter Notebook through the operating IDE.
> 2. In command virtual environment's terminal type:
>    * python -m pip install ipykernel
>    * python -m ipykernel install --user
>    * python -m ipykernel install --user --name myenv --display-name "Python (myenv)"
>    * jupyter notebook    
> 3. **Copy link** and/or paste in browser to open. **Go to Link**.
> 4. Open New Notebook with python kernel along myenv. 

## Operating in Kaggle

> 1. Open Kaggle and Login with Gmail.
> 2. Open new notebook or import notebook file .ipynb from the jupyter notebook that you have created (please be aware that the 
  packages version may differ). 
  
## Key Practicing Points:
## Command
>    1. **pip list, pip show and pip install**
>    2. **python -m** (!python is used in notebooks) , python -m venv venv (the last venv is the environment's name)
>    3. **python -m ipykernel install** (in the ipykernel, myenv is the environment's name)
>    4. **venv\Scripts\activate.bat** to activate virtual environment (venv is the environment's name)
 
## Definition
   1. **ipykernel**. 
      The kernel is the part of the backend responsible for executing code written by the user in the web application.
   2. **jupyter**.
      The original web application for creating and sharing computational documents.    
   3. **lxml**.
      A python library which allows for easy handling of XML and HTML files, and can also be used for web scraping.
   4. **Module**
      A module is a Python file that (generally) has only definitions of variables, functions, and classes. A library can contain 
      many modules, 
      but they are usually all connected by some theme.
   5. **Pandas**.
      Open-source library that provides high-performance data manipulation in Python.
   6. **pip**.
      The package installer for Python.List to list packages, show to show version and install to install.
   7. **PowerShell** is the shell framework developed by Microsoft for administration tasks such as configuration management and 
      automation of repetitive jobs. Where the code's ***Output*** is displayed in VSCode.
   8. **Python -**.
      A high-level, interpreted, interactive and object-oriented scripting language.
   9. **Virtual Environment**.
      One of your projects might require a different version of an external library than another one. New virtual environment 
      becomes self-contained and has its own pip to install libraries,its own libraries folder, where new libraries are added, and its 
      own Python interpreter for the Python version you used to  activate the environment.
   10. **Web scraping**. 
      Process of collecting and parsing data from the web.

# 1. Web
Check for the version and the packages availabilit, if unavailable then pip install (example in the section "3,PDF").

'''Project #1 Table Extraction - Extract Tables from Websites
Target website https://www.idxchannel.com/market-stock.php 
Extract tables on the website - using pandas'''
import pandas as pd
import lxml

market_stock_072522 = pd.read_html('https://www.idxchannel.com/market-stock')

print (len(market_stock_072522) #in VSCode type: print(len(market_stock_072522)))

print(market_stock_072522) # or just type: market_stock_072522
...
[         No.    Code                                       Name  Prev.  Close  \
 0        1.0    AALI                    Astra Agro Lestari Tbk.   9350   9450   
 1        2.0    ABBA                          Mahaka Media Tbk.    278    278   
 2        3.0  ABBA-R                  Right VI Mahaka Media Tbk      0      0   
 3        4.0    ABDA               Asuransi Bina Dana Arta Tbk.   6075   6050   
 4        5.0    ABMM                         ABM Investama Tbk.   2500   2490   
 ...      ...     ...                                        ...    ...    ...   
 1139  1140.0  ZBRA-R               Right II Zebra Nusantara Tbk      0      0   
 1140  1141.0    ZINC                     Kapuas Prima Coal Tbk.     81     82   
 1141  1142.0    ZONE                         Mega Perintis Tbk.   1150   1150   
 1142  1143.0    ZYRX               Zyrexindo Mandiri Buana Tbk.    500    520   
 1143  1144.0  ZYRX-W  Waran Seri I Zyrexindo Mandiri Buana Tbk.     33     35   
 
       Change       %  
 0        100   1.07%  
 1          0   0.00%  
 2          0   0.00%  
 3        -25  -0.41%  
 4        -10  -0.40%  
 ...      ...     ...  
 1139       0   0.00%  
 1140       1   1.23%  
 1141       0   0.00%  
 1142      20   4.00%  
 1143       2   6.06%  
 
 [1144 rows x 7 columns]]...
 
## Key Practicing Points:
## Code
>    1. **import module as library** and **import module**
>    2. **print** (required in 
>    3. **read_html()** 

## Command
>    1. **pip show**
>    2. **python -m  and python --version** (!python is used in notebooks)

## Definition
   1. __import__() function.
   Import in python is similar to #include header_file in C/C++. Python modules can get access to code from another module by importing the file/function using import.    The import statement is the most common way of invoking the import machinery, but it is not the only way.
     * **import as**
     * **import**   
     * from
     * import *    
   2. **Pandas read_html()**. 
   Quick and convenient way for scraping data from HTML tables.
   3. **Code runs in a sequential order**. 
   
   

# 2. CSV
Check for the version and the packages availability, if unavailable then pip install. 
In this section, we follow the sequence from previous steps thus carry on with the previous codes (example pip install shown in the section "3,PDF '').

''' Jakarta Stock Exchange
Target website https://query1.finance.yahoo.com/v7/finance/download/%5EJKSE?period1=1628687576&period2=1660223576&interval=1d&events=history&includeAdjustedClose=true 
Extract tables on the website - using pandas'''
import pandas as pd

df_historical_price210811_220811 = pd.read_csv('https://query1.finance.yahoo.com/v7/finance/download/%5EJKSE?period1=1628687576&period2=1660223576&interval=1d&events=history&includeAdjustedClose=true')

print(df_historical_price210811_220811)
'''
      Date	    Open	       High	       Low	       Close	   Adj Close	 Volume
0	2021-08-12	6092.245117	6139.808105	6051.852051	6139.651855	6139.651855	206955800
1	2021-08-13	6154.051758	6179.895996	6113.263184	6139.492188	6139.492188	163739300
2	2021-08-16	6144.942871	6147.304199	6056.736816	6087.913086	6087.913086	171745600
3	2021-08-18	6109.561035	6136.282227	6040.603027	6118.149902	6118.149902	208983000
4	2021-08-19	6110.549805	6111.012207	5958.043945	5992.321777	5992.321777	214361500
...	...	...	...	...	...	...	...
240	2022-08-05	7057.348145	7090.767090	7045.981934	7084.654785	7084.654785	173887000
241	2022-08-08	7084.654785	7100.808105	7050.824219	7086.849121	7086.849121	219012400
242	2022-08-09	7086.849121	7144.202148	7086.849121	7102.879883	7102.879883	263201500
243	2022-08-10	7102.879883	7104.034180	7021.672852	7086.235840	7086.235840	200438400
244	2022-08-11	7086.275879	7181.100098	7086.275879	7160.384766	7160.384766	0
245 rows × 7 columns'''

print(len(df_historical_price210811_220811))

df_historical_price210811_220811.rename(columns={'Close':'Close Price adj for splits','Adj Close':'Adjusted Close Price for splits&dividen&/cap gain'},inplace=True)

print(df_historical_price210811_220811)

'''
	   Date	       Open	       High      	Low	  Close Price adj for splits	Adjusted Close Price for splits&dividen&/cap gain	Volume
0	2021-08-12	6092.245117	6139.808105	6051.852051	6139.651855	                 6139.651855	                               206955800
1	2021-08-13	6154.051758	6179.895996	6113.263184	6139.492188	                 6139.492188	                               163739300
2	2021-08-16	6144.942871	6147.304199	6056.736816	6087.913086	                 6087.913086	                               171745600
3	2021-08-18	6109.561035	6136.282227	6040.603027	6118.149902	                 6118.149902	                               208983000
4	2021-08-19	6110.549805	6111.012207	5958.043945	5992.321777	                 5992.321777	                               214361500
...	...	...	...	...	...	...	...
240	2022-08-05	7057.348145	7090.767090	7045.981934	7084.654785	               7084.654785	                              173887000
241	2022-08-08	7084.654785	7100.808105	7050.824219	7086.849121	               7086.849121	                              219012400
242	2022-08-09	7086.849121	7144.202148	7086.849121	7102.879883	               7102.879883	                              263201500
243	2022-08-10	7102.879883	7104.034180	7021.672852	7086.235840	               7086.235840	                              200438400
244	2022-08-11	7086.275879	7181.100098	7086.275879	7160.384766	               7160.384766	                                  0
245 rows × 7 columns'''


## Key Practicing Points:
## Code
>    1. **read_csv()**
>    2. **DataFrame.rename**     
 
## Definition
   1. **Pandas DataFrame.rename**. 
      One way of renaming the columns in a Pandas Dataframe is by **using the rename() function**. This method is quite useful when 
      we need to rename some selected columns because we need to specify information only for the columns which are to be renamed. 
      Different ways as follows:
      * **Using rename() function** columns and multiple columns
      * By assigning a list of new column names
      * Rename column names using DataFrame set_axis() function
      * Rename column names using DataFrame add_prefix() and add_suffix() functions
      * Replace specific texts of column names using Dataframe.columns.str.replace function    
   2. **Pandas read_csv()**
      Used to load a CSV file as a pandas dataframe. Most of the data for analysis is available in the form of a tabular format 
      such as  Excel and Comma Separated files(CSV). To access data from a csv file, we require a function read_csv() that retrieves 
      data in the form of a data frame.
      
      
# 3. PDF
Check for the version and the packages availability, if unavailable then pip install. 
In this section, In this section, we follow the sequence from previous steps thus carry on with the previous codes.

pip show tk ghostscript camelot camelot-py

pip install tk ghostscript

## Important
Check in  C:\Program Files\gs\gs9.55.0\bin if available or not. 
If unavailable, go to link https://ghostscript.com/releases/gsdnld.html and choose the general public license and install it to acquire it.

pip install camelot-py[all]

''' Company's Economy Research
Target website https://www.bca.co.id/-/media/Feature/Report/File/S8/Laporan-Riset-Ekonomi/2022/20220808-gdp-solidifying-momentum-amid-mounting-uncertainties-5-aug-2022.pdf
Extract tables on the website - using pandas'''
import camelot

tables = camelot.read_pdf("https://www.bca.co.id/-/media/Feature/Report/File/S8/Laporan-Riset-Ekonomi/2022/20220808-gdp-solidifying-momentum-amid-mounting-uncertainties-5-aug-2022.pdf", pages='4-6', split_text=True)

print(tables[0]) 

Access the table using the index 0 and take a look at its shape.

print(len(tables))

print(tables)

tables[0].parsing_report #in VSCode type: print(tables[0].parsing_report)

#out: {'accuracy': 96.0, 'whitespace': 2.0, 'order': 1, 'page': 4}

The accuracy is 96% and whitespace 2%, most likely the table was extracted correctly. 
You can access the table as a pandas DataFrame (df) by using the table object’s df property.

print(tables[0].df

	0	1	2	3	4	5	6	7	8	9
0		2020		2021		Q2-21	Q3-21	Q4-21	Q1-22	Q2-22
1		Rp Tn	Share	Rp Tn	Share	Rp Tn	Rp Tn	Rp Tn	Rp Tn	Rp Tn
2	Agriculture, livestock, \nforestry, and fishery	2,115.4	13.7	2,253.8	13.3	596.9	619.4	512.2	566.7	638.8
3	Mining and quarrying	993.5	6.4	1,523.7	9.0	338.0	413.1	469.1	472.9	642.5
4	Manufacturing \nindustry	3,068.0	19.9	3,266.9	19.3	805.6	828.4	845.4	866.3	877.8
5	Electricity and gas	179.7	1.2	190.0	1.1	46.1	47.6	49.7	50.0	50.5
6	Water provisioning \nand waste recycling	11.3	0.1	12.0	0.1	3.0	3.0	3.1	3.0	3.2
7	Construction	1,652.7	10.7	1,771.7	10.4	422.5	449.3	471.3	470.4	449.5
8	Wholesale trade and \nrepairs	1,994.1	12.9	2,200.5	13.0	546.3	562.9	571.9	590.9	625.1
9	Transportation and \nwarehousing	689.6	4.5	719.6	4.2	176.0	168.9	205.2	208.5	235.9
10	Hotels, restaurant, \nand catering	394.1	2.6	412.3	2.4	103.5	97.6	109.7	110.1	116.2
11	Information and \ncommunication	696.0	4.5	748.8	4.4	185.3	189.0	192.7	196.0	201.6
12	Financial services and \ninsurance	696.1	4.5	736.2	4.3	184.4	184.4	185.5	195.9	203.6
13	Real estate	453.8	2.9	468.2	2.8	116.3	118.3	119.3	120.4	121.4
14	Business services	294.3	1.9	301.1	1.8	75.5	73.7	77.2	81.0	84.5
15	Govt. administration , \ndefence, and social ...	582.6	3.8	584.4	3.4	158.1	127.6	159.8	138.8	154.3
16	Educational services	549.6	3.6	556.3	3.3	141.1	132.8	153.6	128.6	139.6
17	Healthcare and social \nservices	201.2	1.3	227.0	1.3	52.2	60.9	64.2	52.3	56.2
18	Other services	302.6	2.0	312.2	1.8	77.4	76.5	81.4	84.7	87.2
19	GROSS DOMESTIC \nPRODUCT	15,438.0	100.0	16,970.8	100.0	4,176.4	4,325.2	4,498.0	4,513.3	4,919.9

Export the table as a CSV file using its to_csv() method. The csv file(s) if you are working in VSCode is available in folder.

tables[0].to_csv('EconomyResearch20220808.csv')

Export all tables at once, using the tables object’s **export()** method.

tables.export('EconomyResearch20220808.csv', f='csv')

## Key Practicing Points:
## Code
>    1. .df, .to_csv(), .export() and .parsing_report   
>    2. **read_pdf()**
 
## Definition
   1. **.df**.
      Data frame is a two-dimensional data structure, i.e., data is aligned in a tabular fashion in rows and columns. Pandas DataFrame consists 
      of three principal components, the data, rows, and columns
   2. **.export()**.
      The export() method exports files with a page-*-table-* suffix. Single table in the list will be exported to filename-page-1-table-1.csv. 
      If the list contains multiple tables, multiple CSV files will be created. Use compress=True, which will create a single ZIP file at your 
      path with all the CSV files.
   3. **.to_csv()**.
      Pandas DataFrame to_csv() function converts DataFrame into CSV data.
   4. **.parsing()**.   
      Analyse (a string or text) into logical syntactic components. A command for dividing the given program code into a small piece of code for 
      analyzing the correct syntax becoming more functional..
   5. **Camelot**. 
      Python library that can help you extract tables from PDF.   
   6. **Ghostscript**.
      Interpreter for the PostScript language and for PDF.
   7. **read_pdf**.
      Reading a PDF to extract tables
   6. **tkinter**.
      The standard Python interface to the Tk Graphical User interfaces (GUI) toolkit, and is Python's de facto standard GUI an interface that is 
      drawn on the screen for the user to interact with. Create an instance of tkinter frame. 

## Problem Solving

## Create Virtual Environment
1. In this article, we are **focusing** in **virtualenv**. Another command is **virtualenvwrapper**, it provides a set of commands which makes 
   working with virtual environments much more pleasant as it places all your virtual environments in one place. (source: https://docs.python-
   guide.org/dev/virtualenvs/). Don't get mixed up.
2. Remember in VSCode the code in the code editor and if you run the code, please ensure the terminal in the powershell. All of the commands can 
   be typed in the terminal command. Don't get mixed up.

## Table Extraction in PDF
Again in this article, we are focusing on getting the table from the website.
1. **If there is a problem linking with the path in the website**, you can download the pdf and place it in your chosen folder. 
   In the path in your code, you use double slash (**\\\**) example: "E:**\\\**2022**\\\**00. BODY of KNOWLEDGE**\\\**filename.pdf"
2. **Module error** , module 'camelot' has no attribute 'read_pdf'. 
   In this article, we use pip *install camelot-py[all]* rather than camelot or just camelot-py to resolve it.
3. **RuntimeError**: Please make sure that Ghostscript is installed for Windows.
   This solution is solved by downloading ghostscript as mentioned in the beginning.
4. There is also the next level to learn where we need to open the url if we can not get the file in the url, in this article we go to no.1 or download.
5. Ensure it is a **text-based pdf**. If not, that is another topic to learn.

Copyright 2022 Wahyu Ardhitama
