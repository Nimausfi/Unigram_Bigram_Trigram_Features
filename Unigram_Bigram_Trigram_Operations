from wordcloud import STOPWORDS
import pandas as pd
import re
import string


#unigram operation

def unigram_operation(project_path, csv_file_path_and_file_name):
    # Read the file
    df = pd.read_csv(project_path+csv_file_path_and_file_name, encoding="latin-1")
    text = df.values
    comment_words = ''
    stopwords = set(STOPWORDS)
     
    result = []    
    
    for val in text:
            val = str(val)
            tokens = val.split()
            for i in range(len(tokens)):
                tokens[i] = tokens[i].lower()
            new_tokens = []
            for i in range(len(tokens)):         
             if (tokens[i] not in stopwords):
                 tokens[i] = re.sub(r'\d+', '', tokens[i])
                 tokens[i] = tokens[i].translate(str.maketrans('','', string.punctuation))
                 if 'https' not in tokens[i] and 'us'!= tokens[i] and 'will' != tokens[i] and 'go' != tokens[i]: 
                    new_tokens.append(tokens[i])
            br = (new_tokens)
            result.append(br)
            print(br)
            comment_words += " ".join(new_tokens) + " "


#bigram operation

def process_word_list_into_bigram(one_word_list):
       result = []
       
       if len((one_word_list)) <= 2:
           one = ""
           for i in range(1, len(one_word_list)):
               one += one_word_list[i]
               if i != len(one_word_list):
                   one += " "
           result.append(one)
       else:
           for i in range(1, len(one_word_list)):
               result.append(str(one_word_list[i-1]) + " " + str(one_word_list[i]))
                             
       return result 

def bigram_operation(project_path, csv_file_path_and_file_name):
       df = pd.read_csv(project_path+csv_file_path_and_file_name, encoding="latin-1")
       text = df.values
       comment_words = ''
       stopwords = set(STOPWORDS)
   
       result = []    
       
       for val in text:
               val = str(val)
               tokens = val.split()
               for i in range(len(tokens)):
                    tokens[i] = tokens[i].lower()
               new_tokens = []
               for i in range(len(tokens)):         
                if (tokens[i] not in stopwords):
                  tokens[i] = re.sub(r'\d+', '', tokens[i])
                  tokens[i] = tokens[i].translate(str.maketrans('','', string.punctuation))
                  if 'https' not in tokens[i] and 'us'!= tokens[i] and 'will' != tokens[i] and 'go' != tokens[i]: 
                      new_tokens.append(tokens[i])
               br =  process_word_list_into_bigram(new_tokens)
               result.append(br)
               print(br)
               comment_words += " ".join(new_tokens) + " "
               

#trigram operation
            
def process_word_list_into_trigram(one_word_list):
       result = []
       
       if len((one_word_list)) <= 3:
           one = ""
           for i in range(1, len(one_word_list)):
               one += one_word_list[i]
               if i != len(one_word_list):
                   one += " "
           result.append(one)
       else:
           for i in range(2, len(one_word_list)):                       
               result.append(str(one_word_list[i-2])+ " " + str(one_word_list[i-1]) + " " + str(one_word_list[i]))
       return result 


def trigram_operation(project_path, csv_file_path_and_file_name):
    df = pd.read_csv(project_path+csv_file_path_and_file_name, encoding="latin-1")
    text = df.values
    comment_words = ''
    stopwords = set(STOPWORDS)
    
    result = []
    
    for val in text:
        
        val = str(val)
        tokens = val.split()
        for i in range(len(tokens)):
            tokens[i] = tokens[i].lower()
        new_tokens = []
        for i in range(len(tokens)):
            if (tokens[i] not in stopwords):
                tokens[i] = re.sub(r'\d+','',tokens[i])
                tokens[i] = tokens[i].translate(str.maketrans('','',string.punctuation))
                if 'https' not in tokens[i]:
                    new_tokens.append(tokens[i])  
        tr = process_word_list_into_trigram(new_tokens)
        result.append(tr)
        print(tr)
        comment_words += " ".join(new_tokens) + " "
        
        
               
if __name__ == '__main__':
    # folder address
    project_path = "D:\\....................................."
    # file name and its format (e.g. Data.csv)
    csv_file_path_and_file_name = "\\----------------------.csv"
    unigram_operation(project_path, csv_file_path_and_file_name)
    #bigram_operation(project_path, csv_file_path_and_file_name)
    #trigram_operation(project_path, csv_file_path_and_file_name)
