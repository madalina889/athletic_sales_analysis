# athletic_sales_analysis
-python
-vscode
#Informations taken from sources 
##GPT chat
###Google
Notes : https://pythontutor.com/render.html#mode=edit 

Train in coding on python 
Stack overflow : https://stackoverflow.com/questions/ask ask a public question 
Pandas explanation : https://pandas.pydata.org/docs/user_guide/pyarrow.html
PANDA 1 appunti in classe 
The reason we use panda is because if we have big data is more appropriate , excel is heard as software to be used .
Conda dev 

PANDA CLASS 2 
DATA PROCESSING 
dataFrame : structures in which data are rappresent and learn how to do summery statistics 
Activity one , pandas is the name of the library and pd is how we input panda so we are inputting pandas as pd 
We need to import the data we need to tell panda where is the data living 
To tell in the unsolved which folder are we looking for so file = “../Resources .. 
Df is define 
Head : shows the five rows of that file you’re calling , like temperature_df.head(10) so I’ll have the next 5 columns . To rename the columns I take 

rename_df = temperature_df.rename (columns = {
              “Station (which is the key in this dictionary and the name of the first column)”: “Station”, this is the first pair I want to aggiust 
               “Date” :”date”, 
                “report_type”: report_type
})
How do we count the report type that are FM-16?
rename_ddf.loc[renamed_df[‘report_type’]==‘FM-16’] this is gone show all the fm -16 rows 
If I want to display the link I do Len(fm16_df).
We want to filter a specific temperature reading again so I do again
len(rename_df.loc[rename_df[‘hourly_temp’]>70]).
rename_df.iloc[275,3] 
If I do rename_df.iloc[500:506 , 1:3], is gone display the row from 500 to 505 
If we do -10 we show the last 10 rows : ewname_df.iloc[-10] or rename_def.head(-10), rename_df.tail(-10).
We wil be talking about sorting values to given columns 
Pathlib , I want to import vt_tax_statistics.
To sort from lowest to higher is taxes_df.sort_values(“Meals”), if I add .head is gone show me the first 5 if you sort a list of columns you use [ ] like taxes_df.sort_values([“meals count”, “Rent Count”] , ascending = False ).
If I tap taxes_df.columns is gone display the columns so I cn copy past for next operation 
If I do reset_index (drop=true) cause I. DO INDEX
   DROPAN IS A MISSING VALUE , SO THERE IS A WAY TO FIND  A ROW THAT MISS DATA 
TO REPLACE 
Df.dtypes 
Df.astype this data convert , I want to convert the zip code limn in str df.astrype ({“zip” : str}, error = ‘raise’)
df[employer’].unique is showing the unique employers and to count how much are them we just do 
len(df[employer’].unique).
When I want to replace I [put the name of what it was and : and the name of what is gone be 

To save that column you have to put df[‘empoloyer’] = in the front and not just df cause you’re gone loose the other columns 
If you want to print values and labels together 
print(f”The count is {df[‘Amount’].count()}”)
print(f”The minimum  is {df[‘Amount’].min()}”)
print(f”The maximum is {df[‘Amount’].max()}”)

df.to_csv("../Resources/donors2021.csv", index=False, encoding="ISO-8859-1")

This is gone save the new one in a new folder 
Numpy is more advance and more row level functionalities
Matrices (4d , 5d, very complex data type ) 
sciPy is another kind of library , is scientific , is to work with optimization algebra , science oriented functionality 
Numpy is imported as np 
Is I do scipy.stats as its is because I’m importing just the stats of scipy.
To add a column to a dataframe i put my old temperature_df[“z_scores”] = z_scipy , between [ ] is my new column .
Mean , median , mode . For mean and median we calculate it with Numby and the mode with spicy even if is possible to do it with Numby too . Numpy is faster then scipy and more compatible with the other libraries. 
| this means or ..
../Resources : the .. means the relative path and resources the folder where is the file / the name of the file 
1.First step , create a variable file = “..Resource/ , like where you import your css file (all the data ) 
2. Crate your data frame temperature_df (df is data frame ) then we call panda with pd(which is panda ).read_csv (because we reading csv) then (file) recall the file 
3. Temperature_df.hrad() we need to see the first 5 rows 
4. rename_df = temperature_df.rename(columns = {
             “STATION”(is the key ) : “Station”
              “DATE”: :date”…and change anything you want 
})
(how is gone be the new name, Station)
Columns get normally a dictionary 
How do we count the report type ? We need to filter (in that case of fm16 ). We will filter the data frame by rename_df.loc (this is use to filter the data frame ,you need to remantion the data frame so rename_df.loc[rename_df] now you  have to say that you want to filter report type so rename_df.loc[rename_df[“report_type”]==]
If you do = is like true or false so we do == , with filter is always like that ==. Then you say what filter you want to use which is fm -16 so :
rename_df.loc[rename_df[“report_type”]== “FM-16”] so what this code mean is :get me the renamedataframe ,get all the rows that has a value of fm-16 inside report type. 
If you want to be more organize you can do :
fm16_df = rename_df.loc[rename_df[“report_type”]== “FM-16”]
len(fm16_df) show me the link of this data frame 
Over 70 ..: we will filter again with this 70 
len(Rename_df.loc[rename_df[“hourly_temp”] >70])
rename_df.iloc[275 , 3] this is happening because 275 is row 276 and 3 is column number 3 . With bloc you have to know which column number you have 
Rename_df.iloc[500:506,1:3]so you want the rows between 500 and 505 and the columns between 1 and 3 .
rename_dftail() shows the last data frame or .iloc[-10] is also the last 10 data frame 
Another way is also .head(-10) but shows you the first 10 and last 10 . Best way is tail . 
Talking about sorting . We import the package and as pd (which is also panda) then you also have another library pathlib so from path lab import path .
So we want to sort the database sort by one of those column in this case meals . From lowest to highest 
meals_taxes_df = taxes_df.sort_values(“Meals”)

 you take the data frame say that you want to sort and which column you want to sort , you can run it like that or say how much rows you want to see by .head()this is gone be the 5 if you don’t put a number .
meals_taxes_df = taxes_df.sort_values(“Meals”)
meal_taxes_df.head()
meals_taxes_df = taxes_df.sort_values(“Meals”, ascending=False ) with this you ask panda to show the data frame in a descending order ,so the higher meals number is coming first . 
taxes_df.sort_values([“MealsCount”,”Rent count],ascending= False )I’M sorting by meals count then rent count ,then to have it more organized we have to call this operation and create a variable :
Meals_and_rent_count_df = taxes_df.sort_values([“MealsCount”,”Rent count],ascending= False )

meals_and_alcohol_count_df =taxes_df.sort_values([“Meals count”,”Alcohol Count”], ascending = False )

New_index_df = Meals_and_alcohol_count_df.reset_index(drop = True)
new_index_df.head() and it show the right index but you saved the old one also.
dropna(how=“any”) means drop all the na , how = any means all the values that are na so missing values. 
If we want to put a value per NaN you do data frame .fillna(value=<value>)
To replace we need the data frame and the work with dictionaries df[“Empluer”] = df[“Empluer”].replace({“self”: “self-employed”,”self employed”:self-employed”}) so you got the dictionary and say that you want all the values for self-employed ,so you change self and self employed that doesn’t have an hyphen (-).then you do .value_count()
Sometimes you need to specify the format that a file was safe by encoding so df = pd.read_csv(file, encoding=“iso-8859-1”) in case you have some specific alphabets (in latin normally should be fine) 
If we have a column thats NaN we delete not : del(delete) del df[“Memo_CD”]
df.head()
Df.count() counts values in each columns 
df_dropna(how=“any”) you drop row or column without information which has an NaN then to check the values you do df.count() 
Another thing we do is data type : df.dtypes , sometimes not all the columns are datatype  , you can have string float or integer so what comes out is what you have , object float int .if panda takes something as integer but is a string we have to convert it . How to? With as type and it takes dictionaries :
Df.astype({“zip”:str}, errors “raise”)so you say that the values in zip column into a string and to verify is changed you do df.dtypes and run it and is gone be an object .
If I want to check all the unique values of a column df[“employer”].unique() is gone give the list or if you want the total number you do len(column df[“employer”].unique()) 
When you replace in order to safe the old column just in case you have to df[“employer”] = … not only df[“employer”].replace({“self”:self-emp[loyer”, …]) this is how to but you have to put the first column before in order to save it 
For a statistical overview of a data is describe : df.descrive() it says that your data sets has the count of blah blah then the mean ,standard daviation max etc 
If I want to print with f I put it in the data frame ..
How we save to csv after the changes : df.to_csv(“../Resources?donors0000.csv”, index=False,encoding= “iso-8859-1”) and once you run it you’ll see appear another file with the modified one. 
Python is the language and the we use packages which contains codes to code datas ,panda is a package and numpy is another one with other specialities and numpy is for working with arrays so a lot of lists and matrices multidimensional array(very complex datatypes) ; scimpy has other specialities .
We import numpy as np
Import spicy.stats as its states because we import just that from the module .
If you filter the demperature_[‘hourly…’] and it came out with no name is because is a series ,usually they don’t have name ,has index value , no column name .
np.median(temperature) average ; sts.mode(temperature);np.var(temperature) is the variation ;np.std(temperature) standard deviation ; sts.(zscore(temperature) the score is the score that says how far away from mean is it with a number ,the closer the number is from 0 mean the closer to the average is it . So to apply another column to my old data frame : 
z_scimpy= its.zscores(temperature)
temperature_df[“z_score”] = z_scimpy so I take data frame and say what will be the name of new column z_score and apply with = the variable I did before .
Variance describe how much variation there is in a data set ,if the value is far from the average  means that there is a lot of variation so everything depends on how far the variance is from the mean.
Standard deviation is the square root of the variance . If the code is positive the value is grater then the mean and vice versa 
| means or so on 6 activity means that loc is filtering the hourly.. <45 or …>69.
Activity 7 
PANDA 3 CLASS 
 6 JAN
PANDAS was made to emulate the functionality..
Create a new columns , why I want a new columns? When we have to do an operation between two columns so you don’t want to replace you just need a third column . Data cleaning , if we want to remove something .
Describe() is gone describe statistics. 

If I put one bracket [ ] is a series so one column and if I specify [[ ]] is two columns and inside I put two definitions 
If we want to create a new column which display the amount in thousands without losing the first value . So:
Thousands_of_dollars = data_file_df[“Amount”]/1000
Data_file_df[“thousands of dollars”] = thousands_of_dollars
For the unique method unique = training_df["Trainer"].unique()
unique 
Is the same as training_df["Trainer"].unique()

To see for each trainer how many people they have we do [trainer].value_counts().
The apply function is the functionality of a function , is something specific that you’re doing for you . 
We crate a function : def match_amount(amount):
If amount<500:
   Return amount *0.1
Return amoutn*.2 
donors_df[“match amount’] = donors_df[‘Amount’].apply(mach_amount).
Tax rate (ex4) is the new column where we applied the function we created . If we want to add more logic and add 1% , we want to get the year again 2019.
Exercise for data cleaning .

Repeat this class 
So import panda as pd 
We need to create the variable “file = “../Resources (file is the variable and the resources is where is the file 
The .. is represents the relative path so which is resources the if you open resources on your left on vs code you have another file which is Tax_dataframe.cvs  
Then we create our first data frame with df so , temperature_df= pd.read_csv(file)
To visualize the data frame we do : temperature_df.head()
How we rename the columns ? We need to clean up a little so we initiate a variable Called renamed_df = temperature_df.rename(columns ={
             “STATION”:”Station
               “DATE”: “Date”
     …….EVERY OTHER THING YOU NEED TO RENAME 
})
Columns normally gets dictionary we  will open up a dictionary 
SO IF I WANT TO FILTER DATAFRAME I USE LOC and I need to name data frame twice : rename_df.loc[rename_df[“report_type”]== “FM-16”]
 my filter is fm16 and that means that I’m asking for all the values that have fm16 inside the report type . 
fm16_df = rename_df.loc[renamed_df[“report_type”]==FM-16”]
We can also do Len (fm16_df) 

If I wanna do how many reading measured a temp over 70 : len(renamed_df.loc[renamed_df(“hourly_temp”]>70])
And to see what was the temperature for 276th reading I do : renamed_df.iloc[275, 3] 275 because we know we don’t count from one but from 0 and that will be the row and the 3 denotes column number 3 (orientale )

Exploring data analysis(EDA) PANDAS GUIDED PROHJECTS FOR PORTFOLIO , DATA SCIENTIST 

PANDA 4 CLASS 
 Concatenation is when I want 2 data frames to be together so two columns united. We use axis 1 for horizontal  and 0 or vertical. Joining is used to comb one DataFrames across columns on a common index. instead of append two tables , join is gone combine in order of index .
Merging is going to be similar to the join , we can combine data frames across columns .
If I wanna see prices from apple , google , Facebook , I have 3 data frames and I want to concatenate them : joined_data_row = pd.concat([apple_data, google_data, facebook_data)], axis=“rows”, join=“inner”) meta and fb is the same thing 
Now because I combined them in rows I’ll still have the same number of rows , also I have to put joined_data_row.head(10) and I see , but this is not great because is not picky so we want to do it by columns 
pd.concat([apple_data, google_data, facebook_data)], axis=“columns”, join=“inner”)
joined_data_col.head(30), this is better but we still don’t know which one is for apple ,google and meta .
So we copy the first code again pd.concat([apple_data, google_data, facebook_data)], axis=“rows”, join=“inner”)(so I have a list that I want to concat and axis is telling me that I want to concat  in columns and we add keys that is gone tell me what info more I want : 
pd.concat([apple_data, google_data, facebook_data)], axis=“rows”, join=“inner”,keys[“apple”,”google”,”meta”])
We can do the same thing for rows also .
We use inner in the code , inner is going to match the same column names so we’ll have the same names that exist in the two data frames . If we don’t put inner we’ll have NaN
Now we talk about Joining , this is instead of doing it by column and rows we do by index , the problem is that we have the same names in the column so 
Activity number 3 : we have the datas for 3 different years  in country so we have  countries in vertical and the names , and horizontal crops year and value , and if we want to compare all this data and put all together into one , country is the index ,, the country is gone stay same 
Japan
Korea
Mexico 
Etc same order : wheat_2918_19_data = wheat_2018_df.join(wheat_2019_df)
wheat_2018_19_data.head() but is wrong cause I have to create a suffix to specify better 
wheat_2918_19_data = wheat_2018_df.join(wheat_2019_df, lsuffix= “_2018”, rsuffix+”_2019”)
wheat_2018_19_data.head()
We did a list of the data I want to join and I did a suffix and the I did the code for join and at the end I write again 
wheat_data_cpountry
But is better if I use the suffix and the join in the same code cause even if is longer is easier and refactoring is better (meaning making shorter the codes). 
At combine point :
We do a new variable inner_joined_2018_2019_data = wheat_2019_df.join(wheat_2018_df.set_index([‘Country
‘,’Crop’])) like that we set the index 

Activity 4 when I added with suffix to say where to stay tp the left of right then I added the other years but I don’t want to be confusing so I add the year close to the name .
 If I want to drop something I don’t like I just use drop in th code .
Merging is matching datasets together that something 
If I don’t specify  the code is gone think inner but I have to specify cause ..
If I put the code how=outer we’ll have every information but some of the info are going to be NaN.
 
Activity 7 :
We merge them by date , apple google, meta .
Date means that is the first name in the column 
If I do the code and pd.merge, as soon as columns coming out with the name and _x and _y we do rename , like open _x : apple_open , we do the same for all the variable we want to change .
Is still confusing so we do again the rename “open”:.. 
	merge() for combining data on common columns or indices
	.join() for combining data on a key column or an index
	concat() for combining DataFrames across rows or columns
Merge, join, concatenate and compare#
pandas provides various methods for combining and comparing Series or DataFrame.
concat(): Merge multiple Series or DataFrame objects along a shared index or column
DataFrame.join(): Merge multiple DataFrame objects along the columns
DataFrame.combine_first(): Update missing values with non-missing values in the same location
merge(): Combine two Series or DataFrame objects with SQL-style joining
merge_ordered(): Combine two Series or DataFrame objects along an ordered axis
merge_asof(): Combine two Series or DataFrame objects by near instead of exact matching keys
Series.compare() and DataFrame.compare(): Show differences in values between two Series or DataFrame objects

https://pandas.pydata.org/docs/user_guide/merging.html 

Review of 1 preparing data with panda 
Differences between merging ,joining and concatenations.
Concatenation is the process of combining DataFrames across rows or columns. Put to tables together like two data frames becoming one only. : pd.concat([state_popilation, state_capitals[“capitals”]], axis=1) so the first two are the two data frames and capital is the extra column between all of them thats gone geo in with the others. 
Joining is used to combine Dataframe across columns on a common index . instead of appending one table to the other join is gone comb one them by the index , sometimes index is not 1,2,3,4 but maybe are dates or idk and we need to put this value matching by date so by index .
Merging is how we can match two data frames by column and indexes .
When you concat 3 different csv we do , define the csv first of the 3 datas and save them with different names , select_data_row = pd.concat[{apple_data , google_data , meta_data} ,axis= “rows”, join=“inner ”] so axis is because I want the data one on top of each other . But we need to understand which data is giving what info . If I do same thing with axis = column I’m gone have .
I need to add to the code keys=[“apl”,”googlel”, “meta”] and this is gone save names if what we have per data in the column .
If I have a join code and then I want to add a suffix for every word in the column tittle thatsthe same we do lsuffix= _2019 ,suffix = 2018 is the left suffix and the right suffix .
Mergin is combining two tables that share something in common. (Data frame with sharing columns and multiple columns) . Join (combines data frame with same index).

Panda class 5
groupby() 
Activity 1 we need to remove everything that has a nan  clean_uf_df = ufo_df.dropna(how=“any”) 
clean_ufo_df.count()
Then we have to check the data type : clean_ufo_df.info()
If I convert ..
grouped_usa_df + usa_ufo_df.groupby([“state’])
Name of data frame (usa_ufo_df) then I put. groupby([“”]).count or I can do .min , .sum… then I put a list 
Then I see if I want to count the info in there , or if I want to specify the column (“state”) [“city”]

REVIEW CLASS 2 PROGRAMMING DATA (PANDA CLASS 5)
GROUPING, AGGREGATING, BINNIN DATA 
GROUPBY ALLOW TO FORM GROUPS , LETS SAY THAT I HAVE AN AVARAGE FORM CLASSES BUT I DONT HAVE THE INDIVIDUAL RESULT . 
When I have data I need to aggregate based on the statistic data I’m analyzing . We are going to aggregate the data and transform this data so we don’t have one observation but one group , in the group we’re gone perform , standard deviation etc . 
We’ll gone work on ufo which are gone have observation in different countries . We have a lot of info also across of the USA and we can analyze . 
In the first activity we have ufo_df =pd.read_cvs(csv_path, low_memory = False) low memory which is a parameter is gone read every row at the time in csv if is false ,true :is gone read in in chunk and read 10 to 10 to 10 until 100 , so is the way it reads the data . 
ufo_df.shape is gone say the amount of rows , now we need to clean the data so I see we have NAN so clean_ufo_df = ufo_df.dropna(how=“any”)
clean_ufo_df.count()
clean_ufo_df.head() 
Then I can check what data type this is it : is with info or types (info is more complete) 
CLEAN_UFO_DF.INFO() / clean_info_df.dtype . so I see that objects and a float . Then I wan tto make a copy so : converted_ufo = clean_ufo_df.copy()
Now I can use the new variable to convert the values of duration column to numeric :
converte_ufo[“duratio(secondo)”] = converted_ufo_loc[:,”duration(second)”].astype(float) this is gone to cast each value as a float then we check how it looks converted_ufo.head()
Then we filter only the use so create a new variable /dataframe Called dusa_ufo_df
usa_ufo_df = converted_ufo.loc[converted_ufo[“country”] ==“us,:]
usa_ufo_df.head() and I’m gone have all the info just for the usa.
Then it asks to count how many sightings (avvistamenti) have occurred within each state : usa_ufo_df[“state”].value_count()
Now I have the count of each state so then I store it in a new data frame 
state_counts = usa_ufo_df[“state”].value_count().
Now we’ll gone group grouped_usa_df = usa_ufo_df.groupby([“state”])
print(grouped_usa_df) the value is gone print ,is gone have a number after the object which is the place where were seen the ufo ; so we created a group that’s all we did for now ,if we want to have the values as value_count we need to specify what we want to focus on with the group ,so after that code : group_usa_df.count().herad() so I tell that I want a count of that group if we want to filter by column : group_usa_df.count().herad()[“state”] example  whatever ;
If we want to do a sum we take the data frame we need grouped_usa_df then we take the column we need to apply on the sum [“duration(second)”]  and put .sum 
grouped_usa_df [“duration(second)”].sum()
Save it in a new data frame state_duration = grouped_usa_df [“duration(second)”].sum()
state_duration.head() 
Then it asks us to do a new data frame using duration and counts :
state_summary_table = pd.DataFrame(this is the new data frame we create)
 
so             state_summary_table = pd.DataFrame( {“Number of       Sighting” :state_counts,
          “Total Visit Tima” : state_duration }) those are the last two variables I created and maybe modified cleaned or whatever 
state_summary_table.head
Ricapitolando recap: to group we need the name of the variable which shows the data frame usa_ufo_df.groupby and then I open a list ([“state”]) 
and I put the column I want to groupby (state) ,I can also do multiple columns but we see that later . Then we need to indicate what operation we want to apply on that : .max, .min..ecc then I can specify the column [“city”] 
usa_ufo_df.groupby(“state”)[“city”].count()
Activity number 2 : when we get to the groupby and we groupby average trainers , we see that there is a little disorder so we gone sort by descending by putting the code trainers_means.sort_values(by=“memberhip(Days)”, ascending =False) ascending false says that we want it descending . So in the data frame we’ll face the groupby which is trainer and in columns what we want to see membership days and weight ..
Now we see aggregations , if we want to group by more then one column , so we are doing groups of more then one column 
So we have groiuped_ufo_duration_shape = converted_ufo_df.groupby(“shape”)[[“duration (seconds)”]].mean()
converted_ufo_df.groupby.head() , so what I did ? I groupby by each shape  and choose the duration (in second ) columns   to be applied on it , then we need to put sort_value and ascending=false (dal pie grande galore al piu piccolo ), so we are doing the average of the duration of each shape . But we also want to see the sum :
groiuped_ufo_duration_shape = converted_ufo_df.groupby(“shape”)[[“duration (seconds)”]].agg(“mean”,”sum”) so instead of doin .mean().sum() we just do an aggregation .agg and add all the math I want to apply on the code .
Now let’s assume I want to group. By country and state and they have to be in a list and go in order : converted-ufo_df.groupby([“country”,’state”]).count() I will have all the values in the columns for those two cropped by and if I want just duration and the average of it I need to put   
ufo_df.groupby([“country”,’state”])[“duration(second)”].mean()
Then we aggregate more functions of this durations on the country and state : 
ufo_df.groupby([“country”,’state”])[“duration(second)”].agg([“count”,”mean”,”sum”]). So we see that we have different indexes country and state and also count and mean and sum . So we want to flat two of them to get just one row country_state_duration_flatten = country_state_duration_metrics.copy() we copy it so we save it 
just one row country_state_duration_flatten.columns.to_flat_index() : this is gone give me the list of index , we need to put those tuples together . 
We need to have a list (comprehension list )for all the columns  like 
[ x**2 for x in range(10)] like this one. So we need to loop thru all the names 
[ ‘_’.join(column) for column in country_state_duration_metrics.columns]
after this if we run the code is gone show up like this :
 [‘duration (seconds)_count”,
‘Duration (seconds)_mean”,
‘Duration (seconds)_sum”] _ is the one “_” before .join 
Level 0 is duration (seconds) ,so we’ll have to three times cause is base on mean count and sum 
And if I do value (1 ) is gone be just count sum mean . So now to have it displayed with duration seconds united to count mean and sum we do :
country_state_duration_metrics.columns = level_0+ ”_” +level_1
country_state_duration_metrics
And is gone come out the two country and states which we groupby and 3 columns with duration (seconds)_count, duration (seconds)_mean, duration (seconds)_sum .
But we don’t like it named like that se let’s rename:
country_state_duration_metrics =. country_state_duration_metrics.rename(columns=here dictionary Wirth the older name and new name :
country_state_duration_metrics =. country_state_duration_metrics.rename(columns={“duration(seconds)_count” : “Number of Sighthings”, …etc}, lovel_0)
What is I want an index for each day within certain period of time  : lets say I want to have multiple periods by day and I want to have period 1 from 9 to 9.30 , period 2 from 9.30 to 10 etc and then I want to see which period I have per day and I want to get it for one year , so its a massive data . 
Create a function def  custom_avg(x):
                                 Returns.mean()
To apply a custom function to a groupby we need to bring “apply”
converted_ufo_df.groupby(“shape”).apply(lambda x: custom_avg(x)) 
So what was is lambda x: x is gone bring me all the data but I want lambda x : x[“duration (seconds0”]) , if I don’t want all the duration but only the avarage  (lambs x : custom_avg([“duration(seconds]))
But could give me an error because wrote like that is a series so in this case we have to specify :  (lambs x : pd.Series(custom_avg([“duration(seconds]))) , apply is gone let you use custom function that was created before to the column that I wanted .
We can do the same thing for country and state :
converted_ufo_df.groupby([“country”,”state”]).apply(lambda x : pd.Series({“Avg_Duration(seconds)” : custom_avg(x[“duration(seconds)”])}))
So avg_duration(second) is gone be the name displayed on the column of and is gone show the function we did before per country and state .
Then I want to add a count : def custom_count(x): return x.count()
And also another one def custom_sum(x): return x.sum() , now if I want to apply :
 converted_ufo_df.groupby([“country”,”state”]).apply(lambda x : pd.Series({“Avg_Duration(seconds)” : custom_avg(x[“duration(seconds)”])
                    “Total Duration” : custom_sum(x[“duration (seconds)”]
                     Other function created under some name 
}))
So now we have an aggregation between country and states and them total sights , avg duration and total duration . In panda series you’re gone have a dictionary with the name that contain the function applied before 
In the next when we do the function def custom_percentage (x): if x.count()>0: 
Return (x.sum()/x.count()*100).round(2)
Else:
Return 0 . So it has to be >0 because then if you multiply something for 0 is gone turn 0 so is fundamental , then you divide the sum by the count and multiply per 100. round(2) is the round by decimals 
You should save the come with the pd.series and lambda so you can use it all the time and just change the names. 
BINI ,create in bins . When you convert a numerical data in a categorical data and you need to specify what represents what. Like if I get 84 at my homework means that I’ve got a B categorical , then see how many people got a B or an A … 
So we have class_data= { “class”: [“oct”,
                                           “Name”: [“Logan”,…
                                             “Test score”:[90,59..  ]}
test_score_df = pd.DataFrame(class_data)
test_scores_df
Those are the informations and are going in order like: oct, Logan, 90 

Bins = [0, 59.9, 69.9,..]
Create the names for the 5 beans 
group_names = [“F”, “D”..]
test-score_df[“test score summary”] = pd.cut(test_scores_df[“test score”],
                                                                         Bins,
                                                                          Labels = group_names,
                                                                           include_lowest = true)
test_score_df 
Then we just sort the values .
Activity 8 so we need to split the two groups because the min and max are too different and we need  to group it , so I created the bins and the group_labels , so from 0to 2.4k is gone be in 0 etc . So then we are ready to do the binning so we put the movies_df which is the one containing the numerical that I want to have as bins, then we put bins and finish with labels . If we don’t put labels is not gone give me error but we have to put it or is confusing . Now that I have a column I can do groups then the count and then just closing the columns we want to display that.

Cut creates the bins then we bring the name of the data frame ,then choose the name of the value that contains the numerical value [“test score”]

PANDA 5 (PREPARING DATAS WITH PANDAS 3) 

Pivot tables allows you to reshape columns to row and vice versa in excel 
We need columns ,index and values to do a pivot (index are for example the books).
When we do loc.[:,[3,4,0,1,2] is basecally in order about the months but we put the numbers because is the position of the dates and we know it starts with 0 , like we need first august so is in position 3 ecc. 
If we want to specify what aggregation we need to add in the application we use pivot table . Aggfung = ‘mean’ is helping with average so we know for the inventory what we need more 


REVIW CLASS PREPARING DATA WITH PANDA 3 
What are the trends that we are observing for the hobbit , is the data is the whole one is messy so I want the dates in columns the books are still as a row and then I have the total sales . Thats the pivot table . To create a pivot we need columns index (column(date) to use to make us the new frame (the books) and values (columns that I want to see the aggregation before so is gone be the total sales .
We do book_sales_df[“book_name”].unique() to see the books  we have then same for [“data_ending”] to see the dates but we do that just to see the data we work with not because is necessary for the pivot table .
Let’s create the pivot : there is two ways 
Pd.pivot(book_sales_df)
book_sales_df.pivot() 
Lets start with the first one 
pivot_date_short_form = Pd.pivot(book_sales_df, columns = ‘dateending’,inde= ‘book_name’, values=“total_sales”)
pivot_date_short_form

The second way : pivot_date_short_form = book_sales_df.pivot(columns=“date_ending’, index=‘boo_name’,value..)  pivot_date_short_form  we run this and is gone be the same .
Then we have the dates not in order so we relocate them 
pivot_date_short_form.iloc[:,[3, 4,0,1,2]] so whatever is on 3 is gone be displayed first the what is in 4 etc 
[:, means that the rows has to be same order 
Then we can do change the columns and index to have the table on reverse , the we can pivot_date_short_form.reindex([“8/…”,”other date ]) the order we want to have .

pivot_table() are capable to put more attention into things by doing custom aggregation so is still a pivot but we can aggregate with aggfunc = ‘mean’

pivot_table_books_avg = book_sales_df.pivot_table(values= ‘total_sales, columns= “book_name”, aggfunc= ‘mean”) no index 
pivot_table_books_avg
So here we’ll have the average for each month .
pivot_table_books_avg.rename(column={“old_column”:New_column”}) so {‘total_sales’ :' avg_sales’ }, here we will change the name 
round(1) is gone display 1 decimal 111.1 after the point just one more number . aggfunc=(“mean’,”sum”)) is a tuple thats why is between () mean and sum .
We have index and values we aggregate thru the columns  ,so we’ll have the dates and the mean and sum of it ,then we do reindex for right order of the dates .
Recap . Pivot Reshape the data ,making columns into row and viceveersa , we need to put all three values 
We neet two out of those three value index and column and the add aggfunc ,because we are going more in the specific . The third is where we are going to be performing the aggregation function. 
To get just the columns : data_fram.column .
Resample : aggregate data by time , it work only if the index is a date sales_df.resample(‘W’).sum() here I’m gone see everything by week , every data on every week by going higher .
Melt : is gone change the disposition of my table , I can see the values differently . After I creat a pivot ,if I want to see the first table (similar) I do melt .
