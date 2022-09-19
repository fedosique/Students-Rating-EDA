# Students-Rating-EDA
Scraper + EDA for SPbSUT students rating

## About

I've made a scraper, which obtains personal students data with their GPAs from official university website. 
For that I've used BeautifulSoup4. The stage of understanding, cleaning & analysis of the data was followed with pandas / numpy / seaborn usage. 

## Data structure

University rating is having such format (full name, faculties, year of studying, average grade for the whole period):

<img src="https://sun9-22.userapi.com/impg/nwMrlMFLPhMy0kCvPplXShuBuBuOSi0BjFT9NA/-WJWeb7zwZY.jpg?size=1208x540&quality=96&sign=dc1c19ded010e76d6472e3583fa1f1ad&type=album">

I scraped the data with \<table> tag, 'for' loop did the \<tr> storing in according lists. 

You can familiarize yourself with it by checking 'parse_sut.py'. 

After that, I import that module with lists above into the Jupiter Notebook (.ipynb) file and analysing the data.

## Details of analysis 

- First year students are already listed on the website, but they haven't had their exams passed yet. So, when we are analysing students' GPA, we won't consider them in statistics.

- University rating website has a full name of each student, which is three words in Russia (first name, second name and surname). I've split the string value 'name' and did the data sorting & labelling in Microsoft Excel. 

## Insights

- Median GPA in St. Petersburg State University of Telecommunications is 3,9 of 5,0.

- The distribution plot of grades

  It's shifted and tending to the Gaussian distribution. 
<img src="https://sun9-21.userapi.com/impg/HgxcIHlAIXltDJiznVy_xSis7qnFg_vhmVGa_g/P3idoKTrPG8.jpg?size=391x256&quality=96&sign=b1d47a58f5375f5e038018e5f2d7f25a&type=album">

- Proportion of male / female students in technical university

Male is approximately 71% of the whole number of students. 

<img src="https://sun9-13.userapi.com/impg/EpF7E_h7kfYesuVvAwm8DN9yTLwuEdGoTmGS1w/QPSYDQ9jeE0.jpg?size=387x245&quality=96&sign=50c6bd6f5fcf08bda628ff061627863e&type=album">

- GPA analysis for both genders 

But, female students perform better:

<img src = "https://sun9-62.userapi.com/impg/0jC5iYm7oiR6ueihbPR4dOPeHr58nCrOSASyIA/8KrZZFdt2-Y.jpg?size=280x159&quality=96&sign=c508be4a861677d4254b8b6b110d010f&type=album">

- The heatmap plot of GPA distributed for year of study and gender

<img src="https://sun9-55.userapi.com/impg/RVs9Ddcn5LHYb9txhs3bpJJWxddsvo7Z2UWkcA/MsBa98MEmRg.jpg?size=377x252&quality=96&sign=ac8dbd0daaa3995609e440e441ff1e69&type=album">
