# Group-Project
Group Project
import random

#A subroutine to replace all "-" (empty characters) with a random letter
def randomFill(wordsearch):
  LETTERS="ABCDEFGHIJKLMNOPQRSTUVWXYZ"
  for row in range(0,a):
    for col in range(0,b):
      if wordsearch[row][col]=="-":
        randomLetter = random.choice(LETTERS)
        wordsearch[row][col]=randomLetter

a = 16
#sets the row length
b = 16
#sets the column width
b2 = b*2+1
#sets the top of the box
b3 = b*2-1
#sets the bottom of the box

#A subroutine to output the wordsearch on screen  
def displayWordsearch(wordsearch):
  print("","_"*int(b2))
  for row in range(0,a):
    line="| "
    for col in range(0,b):
      line = line + wordsearch[row][col] + " "
    line = line + "|"
    print(line)
  print("|","_"*int(b3),"|")  

#Create an empty wordsearch (list of lists)
wordsearch = []
for row in range(0,a):
  wordsearch.append([])
  for col in range(0,b):
    wordsearch[row].append("-")
    
    
#A subroutine to add a word to the wordsearch at a random position
def addWord(word,wordsearch):
    c = len(word)
    row=random.randint(0,a)
    col=random.randint(0,b-c)
    for i in range(0,len(word)):
        wordsearch[row][col+i]=word[i]
  #CHANGE THIS CODE TO
  # ----Randomly decide where the word will start
  # ----Decide if the word will be added horizontally, vertically or diagonally
  # ----Check that the word will fit in (within the 12 by 12 grid)
  # ----Check that the word will not overlap with existing letters/words in the wordsearch
  
  #Adding words to our wordsearch
addWord("PYTHON",wordsearch)    
addWord("ALGORITHM",wordsearch)    
addWord("CODING",wordsearch)    
addWord("PROGRAM",wordsearch)
addWord("FINDER",wordsearch)  

randomFill(wordsearch)

#All unused spaces in the wordsearch will be replaced with a random letter


#Display the fully competed wordseach on screen
displayWordsearch(wordsearch)
  
