# MS-test
This is a python code for DNA replication basics
# First, create a string variable called ori that is equal to the Vibrio cholerae ori.
Don't forget to enclose your string in quotes!
ori ="ATCAATGATCAACGTAAGCTTCTAAGCATGATCAAGGTGCTCACACAGTTTATCCACAACCTGAGTGGATGACATCAAGAT
AGGTCGTTGTATCTCCTTCCTCTCGTACTCTCATGACCACGGAAAGATGATCAAGAGAGGATGATTTCTTGGCCATATCGCAATGAA
TACTTGTGACTTGTGCTTCCAATTGACATCTTCAGCGCCATATTGCGCTGGCCAAGGTGACGGAGCGGGATTACGAAAGCATGATCAT
GGCTGTTGTTCTGTTTATCTTGTTTTGACTGAGACTTGTTAGGATAGACGGTTTTTCATCACTGACTAGCCAAAGCCTTACTCTGCCTGA
CATCGACCGTAAATTGATAATGAATTTACATGCTTCCGCGACGATTTACCTCTTGATCATCGATCCGATTGAAGATCTTCAATTGTTAA
TTCTCTTGCCTCGACTCATAGCCATGATGAGCTCTTGATCATGTTTCCTTAACCCTCTATTTTTTACGGAAGAATGATCAAGCTGCTGCT
CTTGATCATCGTTTC"

# Then, print the length of ori
print (len(ori))

#code for patterncount
count = 0
     for i in range(len(Text)-len(Pattern)+1):
        if Text[i:i+len(Pattern)] == Pattern:
            count = count+1 
            
#code using function for patterncount
def PatternCount(Text, Pattern):
    # fill in your function here
    count = 0
    for i in range(len(Text)-len(Pattern)+1):
        if Text[i:i+len(Pattern)] == Pattern:
            count = count+1
    return count
    
#Exercise Break (1 point): Copy over your PatternCount function from the previous step.
    Then print  the number of times that the string Pattern = "TGATCA" occurs in the string Text
    corresponding to the Vibrio cholerae ori, which is found here.
# Copy your PatternCount function from the previous step below this line
def PatternCount(Text, Pattern):
    count = 0
    for i in range(len(Text)-len(Pattern)+1):
        if Text[i:i+len(Pattern)] == Pattern:
            count = count+1
    return count
# Now, set Text equal to the ori of Vibrio cholerae and Pattern equal to "TGATCA"
Text ="ATCAATGATCAACGTAAGCTTCTAAGCATGATCAAGGTGCTCACACAGTTTATCCACAACCTGAGTGGATGACATCAAGATAGGT
CGTTGTATCTCCTTCCTCTCGTACTCTCATGACCACGGAAAGATGATCAAGAGAGGATGATTTCTTGGCCATATCGCAATGAATACTTGTGAC
TTGTGCTTCCAATTGACATCTTCAGCGCCATATTGCGCTGGCCAAGGTGACGGAGCGGGATTACGAAAGCATGATCATGGCTGTTGTTCTGTTT
ATCTTGTTTTGACTGAGACTTGTTAGGATAGACGGTTTTTCATCACTGACTAGCCAAAGCCTTACTCTGCCTGACATCGACCGTAAATTGATAAT
GAATTTACATGCTTCCGCGACGATTTACCTCTTGATCATCGATCCGATTGAAGATCTTCAATTGTTAATTCTCTTGCCTCGACTCATAGCCATGAT
GAGCTCTTGATCATGTTTCCTTAACCCTCTATTTTTTACGGAAGAATGATCAAGCTGCTGCTCTTGATCATCGTTTC"
Pattern = "TGATCA"
# Finally, print the result of calling PatternCount on Text and Pattern.
print (PatternCount(Text,Pattern))
# Don't forget to use the notation print() with parentheses included!
Write a function ReverseComplement() to solve the Reverse Complement Problem, 
Reverse Complement Problem:  Find the reverse complement of a DNA string.
     Input: A DNA string Pattern.
     Output: The reverse complement of Pattern
#Input:  A DNA string Pattern
# Output: The reverse complement of Pattern
def ReverseComplement(Pattern):   
    # your code here
    Pattern = Reverse(Pattern) # reverse all letters in a string
    Pattern = Complement(Pattern) # complement each letter in a string
    return Pattern
# Copy your Reverse() function here.
def Reverse(Pattern):
    # your code here
    reverse = ''
    for char in Pattern:
        reverse = char + reverse
    return reverse

# Copy your Complement() function here.
def Complement(Pattern):
    # your code here
    basepairs = {"A":"T", "G":"C", "T":"A", "C":"G"}
    complement = ""
    for base in Pattern:
        complement += basepairs.get(base)
    return complement
    
Write a function PatternMatching that solves the Pattern Matching Problem.  
# fill in your PatternMatching() function along with any subroutines that you need.
def PatternMatching(Pattern, Genome):
    positions = [] # output variable
    # your code here
    for i in range(len(Genome)-len(Pattern)+1):
        if Pattern == Genome[i:i+len(Pattern)]:
            positions.append(i)
    return positions

Pattern matching code for Vibrio cholerae
    # Copy your PatternMatching function below this line.
def PatternMatching(Pattern, Genome):
    positions = [] # output variable
    # your code here
    for i in range(len(Genome)-len(Pattern)+1):
        if Pattern == Genome[i:i+len(Pattern)]:
            positions.append(i)
    return positions
# The following lines will automatically read in the Vibrio cholerae genome for you and store it in a variable named v_cholerae
import sys                              # needed to read the genome
input = sys.stdin.read().splitlines()   #
v_cholerae = input[1]                   # store the genome as 'v_cholerae'


# Call PatternMatching with Pattern equal to "CTTGATCAT" and Genome equal to v_cholerae,
# and store the output as a variable called positions
print(PatternMatching("CTTGATCAT",v_cholerae))

# print the positions variable
 Pattern count of Thermotoga petrophila against Vibrio dnaA box seq
 How many combined occurrences of "ATGATCAAG" and "CTTGATCAT" can you find in this region? 
 # Copy your PatternCount function below here
def PatternCount(Text, Pattern):
    count = 0
    for i in range(len(Text)-len(Pattern)+1):
        if Text[i:i+len(Pattern)] == Pattern:
            count = count+1
    return count


# On the following line, create a variable called Text that is equal to the oriC region from T petrophila
Text ="AACTCTATACCTCCTTTTTGTCGAATTTGTGTGATTTATAGAGAAAATCTTATTAACTGAAACTAAAATGGTAGGTTTGGTGGTAGGTTTTGTGTACATTTTGTAGTATCTGATTTTTAATTACATACCGTATATTGTATTAAATTGACGAACAATTGCATGGAATTGAATATATGCAAAACAAACCTACCACCAAACTCTGTATTGACCATTTTAGGACAACTTCAGGGTGGTAGGTTTCTGAAGCTCTCATCAATAGACTATTTTAGTCTTTACAAACAATATTACCGTTCAGATTCAAGATTCTACAACGCTGTTTTAATGGGCGTTGCAGAAAACTTACCACCTAAAATCCAGTATCCAAGCCGATTTCAGAGAAACCTACCACTTACCTACCACTTACCTACCACCCGGGTGGTAAGTTGCAGACATTATTAAAAACCTCATCAGAAGCTTGTTCAAAAATTTCAATACTCGAAACCTACCACCTGCGTCCCCTATTATTTACTACTACTAATAATAGCAGTATAATTGATCTGA"

# On the following line, create a variable called count_1 that is equal to the number of times
# that "ATGATCAAG" occurs in Text.
count_1 = PatternCount(Text, "ATGATCAAG")

# On the following line, create a variable called count_2 that is equal to the number of times
# that "CTTGATCAT" occurs in Text. 
count_2 = PatternCount(Text, "CTTGATCAT")


# Finally, print the sum of count_1 and count_2
print(count_1+count_2)

# Input:  Strings Genome and symbol
# Output: SymbolArray(Genome, symbol)
def SymbolArray(Genome, symbol):
    # type your code here
    array = {}
    n = len(Genome)
    ExtendedGenome = Genome + Genome[0:n//2]
    for i in range(n):
        array[i] = PatternCount(symbol, ExtendedGenome[i:i+(n//2)])
    return array

# Reproduce the PatternCount function here.
def PatternCount(Text, Pattern):
    Count = 0
    n=len (Pattern)
    k=len (Text)
    for i in range (n-k+1):
        if Pattern[i:i+k]==Text:
            Count+=1
    return Count
            
    # type your code here
# Input:  Strings Genome and symbol
# Output: FasterSymbolArray(Genome, symbol)
def FasterSymbolArray(Genome, symbol):
    array = {}
    l=len(Genome)
    ExtendedGenome=Genome+Genome[0:l//2]
    array[0]=PatternCount(ExtendedGenome[0:l//2],symbol)
    for i in range(1,l):
        array[i]=array[i-1]
        if ExtendedGenome[i-1]==symbol:
            array[i]-=1
        if ExtendedGenome[i+l//2-1]==symbol:
            array[i]+=1
    # your code here
    return array

# Input: Strings Text and Pattern
# Output: The number of times Pattern appears in Text
# HINT: This code should be identical to when you last implemented PatternCount
def PatternCount(Pattern, Text):
    count = 0 # output variable
    k=len(Text)
    n=len(Pattern)
    for i in range(n-k+1):
        if Pattern[i:i+k]==Text:
            count+=1
    return count

### DO NOT MODIFY THE CODE BELOW THIS LINE ###
import sys
lines = sys.stdin.read().splitlines()
print(FasterSymbolArray(lines[0],lines[1]))

# Input:  A String Genome
# Output: The skew array of Genome as a list.
def SkewArray(Genome):
    # your code here
    Array = [0]
    BaseValue = { "C": -1, "G" : 1, "A": 0, "T" : 0 }
    for i in range(len(Genome)):
        Array.insert(i+1,  BaseValue.get(Genome[i])+Array[i])
    return Array

 
def SkewArray(Genome):
    # your code here
    Array = [0]
    BaseValue = { "C": -1, "G" : 1, "A": 0, "T" : 0 }
    for i in range(len(Genome)):
        Array.insert(i+1,  BaseValue.get(Genome[i])+Array[i])
    return Array
