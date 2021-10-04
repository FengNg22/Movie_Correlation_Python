# Movie_Correlation_Python
Using Python to do the data cleaning and look for the correlation of the Movie Data  
#### The technique included
+ pd.read_csv
+ for loop
+ df.isna().sum() -- _count the null values_ 
+ df.dropna(how='any',axis=0)
+ df.dtypes
+ df['budget']=df['budget'].astype('int64') -- _changing the type_
+ df['YearfromReleased'] = df['released'].astype(str).str.split(', ').str[-1].str[:4]
+ df.sort_values(by=['gross'], inplace=False, ascending=False) -- _sorting data_
+ pd.set_option('display.max_rows',None)
+ pd.reset_option("display.max_rows")
+ df['company'].drop_duplicates().sort_values(ascending=False) -- _drop duplicated data_
+ plt.scatter(x=df['budget'], y=df['gross']) -- _scatter graph_
+ sns.regplot(x='budget', y='gross', data=df, scatter_kws={"color":"red"},line_kws={"color":"blue"}) -- _scatter and smooth_line_
+ df.corr() -- _by default is using Pearson _
+ correlation_matrix=df.corr(method='pearson') 
+ sns.heatmap(correlation_matrix, annot=True)
+ df_numerized[col_name]=df_numerized[col_name].astype('category') -- _Numerization_


#### Refer to Video https://www.youtube.com/watch?v=iPYVYBtUTyE&t=1507s
