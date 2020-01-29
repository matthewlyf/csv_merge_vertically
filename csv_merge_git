import pandas as pd
import glob

path =r'PUT YOUR PATH HERE WITH ALL CSVs'
allFiles = glob.glob(path + "/*.csv") #looks for  all files in path that have .csv extension
frame = pd.DataFrame()
list_ = [] 

def rawcompiler(path2, list_):
    allFiles2 = glob.glob(path2 + "/*.csv") #looks for  all files in path that have .csv extension
    for file_ in allFiles2: #opens all files and append it to list
        df = pd.read_csv(file_)
        list_.append(df)
    frame = pd.concat(list_)#concatenate all files to the empty dataframe
    print (len(frame))   
    frame = frame.sort_values('Date/Time', axis=0, ascending=True, inplace=False)    
    frame.to_csv('')
    
rawcompiler(path, list_)
