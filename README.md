# Generations-in-The-Mexican-Chamber-of-Deputies-by-state
The goal of this project is to provide an approach to mexican politics by using the data from government. We will extract some information about the mexican deputies with BeautifulSoup, a library from Python and use it to visualize the generations in the Chamber of Deputies by state using Seaborn. 
Web scrapping of five hundred pages was performed, it is possible to find the data in the following link: http://sitl.diputados.gob.mx/LXIV_leg/curricula.php?dipt=127 This web page corresponds to the information of a single deputy, to navigate between the profiles of deputies, you can replace the last two characters with a number in the range 1 – 500.
We created two data sets in this script. The first with nine string columns with the data of the main table in each deputy’s profile:
•	  'nombre': Deputy’s name [string]
•	  'tipo_elec': Kind of election [string]
•	  'onomastico': Date of birth [string]
•	  'suplente': Substitute’s name [string]
•	  'edo': State of birth [string]
•	  'ent': Details about State (District)
•	  'ent_2': Details about State [string]
•	  'correo': E-mail [string]
•	  'ext': Phone extension. [string]
The second data set, called ‘cleanedData, has the following columns:
•	  ‘name’: Deputy’s name [string]
•	  ‘state’: State of birth [string]
•	  ‘date_birth’: Date of birth [string]
•	  ‘year_birth’ : Year of birth (integer)
•	  ‘gen’: Generation based on year of birth [string]
Some data, like the dates of birth can be in Spanish, so for further analysis we encourage researchers to find a way to directly convert the strings in Spanish to a datetime column and extract the part of year.
