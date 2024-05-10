The python script allows for the creation of a .jsnol file from a .CSV with paramters compatible for GPT fine tuning. The instructions for using the same are as follows:

step1 - build a .CSV file with three columns corresponding to the input from user,expected output from model and system prompt 
(sample .csv - https://docs.google.com/spreadsheets/d/1TcqFX9MIL1p7K6W5FRsFLww0i1bgyS00pfNqFlaeWbc/edit?usp=sharing) Do this for both the test and validation dataset.

step2 - Load the file with your file name at this line (df = pd.read_csv("Your_File_Name.csv") and at (dataset = pd.read_csv("Your_File_Name.csv"))

step3 - Run the entire code now and you now and you should get a .jsonl file called "converted_data.jsonl"

step4 - use the test and validation .jsnol generated as above to train the fine tuned model in GPT.

note: code was built using google collab so some of the script might require slight edits depending on the environment it will be run on
