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

Motif count
# Input:  A set of kmers Motifs
# Output: Count(Motifs)
def Count(Motifs):
    count = {} # initializing the count matrix
    k = len(Motifs[0]) # length of the first kmer (but all are same length)
    for symbol in "ACGT":
        count[symbol] = [] # count matrix now has keys A, C, T, and G all with values of empty list
        for j in range(k):
            count[symbol].append(0) # count matrix now has keys A, C, G, and T all with values of a list of zeroes of length equal to the length of a kmer
    t = len(Motifs) # length of Motifs, a list of kmers (strings)
    for i in range(t): # for each kmer in Motifs
        for j in range(k): # for each element of the kmer
            symbol = Motifs[i][j] # assigns the key (symbol) to a nucleotide (ACGT) in Motifs
            
            #count[symbol] corresponds to the key of the dictionary count
            #count[symbol][j] corresponds to the position in the list assigned to the key
            count[symbol][j] += 1 # adds 1 to the position in the list assigned to the key
    return count
Write a function Profile(Motifs) that takes Motifs as input and returns their profile matrix as a dictionary of lists. Then place this function into Motifs.py. Make sure that you use the Count(Motifs) function that we already wrote as a subroutine!

# Insert your Count(Motifs) function here from the last Code Challenge.
# Input:  A set of kmers Motifs
# Output: Count(Motifs)
def Count(Motifs):
    count = {} # initializing the count matrix
    k = len(Motifs[0]) # length of the first kmer (but all are same length)
    for symbol in "ACGT":
        count[symbol] = [] # count matrix now has keys A, C, T, and G all with values of empty list
        for j in range(k):
            count[symbol].append(0) # count matrix now has keys A, C, G, and T all with values of a list of zeroes of length equal to the length of a kmer
    t = len(Motifs) # length of Motifs, a list of kmers (strings)
    for i in range(t): # for each kmer in Motifs
        for j in range(k): # for each element of the kmer
            symbol = Motifs[i][j] # assigns the key (symbol) to a nucleotide (ACGT) in Motifs
            
            #count[symbol] corresponds to the key of the dictionary count
            #count[symbol][j] corresponds to the position in the list assigned to the key
            count[symbol][j] += 1 # adds 1 to the position in the list assigned to the key
    return count

# Input:  A list of kmers Motifs
# Output: the profile matrix of Motifs, as a dictionary of lists.
def Profile(Motifs):
    t = len(Motifs)
    k = len(Motifs[0])
    profile = {}
    # insert your code here
    profile1 = Count(Motifs)
    for key in "ACGT":
        for key in profile1:  
            profile[key] = [x / t for x in profile1[key]]
    return profile
Implement the function Score(Motifs). (Make sure you use Consensus(Motifs) as a subroutine!)  Then add Score(Motifs) to Motifs.py.
# Copy your Consensus(Motifs) function here.
def Consensus(Motifs):
    k = len(Motifs[0])
    count = Count(Motifs)

    consensus = ''

    for j in range(k):
        m = 0
        frequentSymbol = ''
        for symbol in 'ACGT':
            if count[symbol][j] > m:
                m = count[symbol][j]
                frequentSymbol = symbol
        consensus += frequentSymbol
    return consensus

# Copy your Count(Motifs) function here.
def Count(Motifs):
    count = {} # initializing the count matrix
    k = len(Motifs[0]) # length of the first kmer (but all are same length)
    for symbol in "ACGT":
        count[symbol] = [] # count matrix now has keys A, C, T, and G all with values of empty list
        for j in range(k):
            count[symbol].append(0) # count matrix now has keys A, C, G, and T all with values of a list of zeroes of length equal to the length of a kmer
    t = len(Motifs) # length of Motifs, a list of kmers (strings)
    for i in range(t): # for each kmer in Motifs
        for j in range(k): # for each element of the kmer
            symbol = Motifs[i][j] # assigns the key (symbol) to a nucleotide (ACGT) in Motifs
            
            #count[symbol] corresponds to the key of the dictionary count
            #count[symbol][j] corresponds to the position in the list assigned to the key
            count[symbol][j] += 1 # adds 1 to the position in the list assigned to the key
    return count

# Input:  A set of k-mers Motifs
# Output: The score of these k-mers.
def Score(Motifs):
    # Insert code here
    result = Consensus(Motifs)
    counts = Count(Motifs)
    score = 0
    i = 0
    for symbol in result:

        # Score is the sum of (total number of elements per column MINUS

        # the number of occurence of the most frequent symbol per column)   

        score += len(Motifs) - counts[symbol][i]  
        i += 1
    return score



    
    # Insert code here
Greedy motif
# Input:  String Text and profile matrix Profile
# Output: Pr(Text, Profile)
    # insert your code here
def Pr(Text, Profile):
    # insert your code here
    pr = 1
    t = len(Text)
    for i in range(t):
        pr = pr*Profile[Text[i]][i]
    return pr
  
def Count(Motifs):
    count = {} # initializing the count dictionary
    # your code here
    k = len(Motifs[0])
    for symbol in "ACGT":
        count[symbol] = []
        for j in range(k):
            count[symbol].append(0)
    t = len(Motifs)
    for i in range(t):
        for j in range(k):
            symbol = Motifs[i][j]
            count[symbol][j] += 1
    return count

def Consensus(Motifs):
    # insert your code here
    k = len(Motifs[0])
    count = Count(Motifs)
    consensus = ""
    for j in range(k):
        m = 0
        frequentSymbol = ""
        for symbol in "ACGT":
            if count[symbol][j] > m:
                m = count[symbol][j]
                frequentSymbol = symbol
        consensus += frequentSymbol
    return consensus

def Profile(Motifs):
    t = len(Motifs)
    k = len(Motifs[0])
    profile = Count(Motifs)
    for i in 'ACTG':
        for j in range(k):
            profile[i][j] = profile[i][j]/t  
    return profile

def Score(Motifs):
    # Insert code here
    score = 0
    k = len(Motifs[0])
    count = Count(Motifs)
    max_symbol = Consensus(Motifs)
    sum1 = 0
    for j in range(k):
        m = 0
        for symbol in "ATCG":
            if count[symbol][j] > m:
                sum1 += count[symbol][j]
    for j in range(k):
        m = 0
        for symbol in "AGTC":
            if count[symbol][j] > m:
                m = count[symbol][j]
        score += m  
    return sum1-score

def Pr(Text, Profile):
    p=1
    k = len(Profile["A"])
    for i in range(len(Text)):
        p=p*Profile[Text[i]][i]
    return p


def ProfileMostProbablePattern(text,k,profile):
    p=-1
    result=text[0:k]
    for i in range(len(text)-k+1):
        seq=text[i:i+k]
        pr=Pr(seq,profile)
        if pr>p:
            p=pr
            result=seq
    return result

def GreedyMotifSearch(Dna,k,t):
    BestMotifs = []
    for i in range(0, t):
        BestMotifs.append(Dna[i][0:k])
    n = len(Dna[0])
    for m in range(n-k+1):
        Motifs = []
        Motifs.append(Dna[0][m:m+k])
        for j in range(1, t):
            P = Profile(Motifs[0:j])
            Motifs.append(ProfileMostProbablePattern(Dna[j], k, P))
        if Score(Motifs) < Score(BestMotifs):
            BestMotifs = Motifs
    return BestMotifs

Use GreedyMotifSearch to look for motifs in the DosR dataset with k-mer length equal to 15 (click here to download).
# Copy your GreedyMotifSearch function (along with all required subroutines) from Motifs.py below this line

# Copy the ten strings occurring in the hyperlinked DosR dataset below.


# set t equal to the number of strings in Dna and k equal to 15

# Call GreedyMotifSearch(Dna, k, t) and store the output in a variable called Motifs

# Print the Motifs variable

# Print Score(Motifs)
def Count(Motifs):

    count = {}

    k = len(Motifs[0])

    for symbol in "ACGT":

        count[symbol] = []

        for j in range(k):

            count[symbol].append(0)

    t = len(Motifs)

    for i in range(t):

        for j in range(k):

            symbol = Motifs[i][j]

            count[symbol][j] += 1

    return count

 

def Consensus(Motifs):

  

    k = len(Motifs[0])

    count = Count(Motifs)

    consensus = ""

    for j in range(k):

        m = 0

        frequentSymbol = ""

        for symbol in "ACGT":

            if count[symbol][j] > m:

                m = count[symbol][j]

                frequentSymbol = symbol

        consensus += frequentSymbol

    return consensus

 

def Profile(Motifs):

    t = len(Motifs)

    k = len(Motifs[0])

    profile = Count(Motifs)

    for i in 'ACTG':

        for j in range(k):

            profile[i][j] = profile[i][j]/t  

    return profile

 

def Score(Motifs):

    # Insert code here

    score = 0

    k = len(Motifs[0])

    count = Count(Motifs)

    max_symbol = Consensus(Motifs)

    sum1 = 0

    for j in range(k):

        m = 0

        for symbol in "ATCG":

            if count[symbol][j] > m:

                sum1 += count[symbol][j]

    for j in range(k):

        m = 0

        for symbol in "AGTC":

            if count[symbol][j] > m:

                m = count[symbol][j]

        score += m  

    return sum1-score

 

def Pr(Text, Profile):

    p=1

    k = len(Profile["A"])

    for i in range(len(Text)):

        p=p*Profile[Text[i]][i]

    return p

 

#Finally solved it

def ProfileMostProbablePattern(text,k,profile):

    p=-1

    result=text[0:k]

    for i in range(len(text)-k+1):

        seq=text[i:i+k]

        pr=Pr(seq,profile)

        if pr>p:

            p=pr

            result=seq

    return result

 

def GreedyMotifSearch(Dna,k,t):

    BestMotifs = []

    for i in range(0, t):

        BestMotifs.append(Dna[i][0:k])

    n = len(Dna[0])

    for m in range(n-k+1):

        Motifs = []

        Motifs.append(Dna[0][m:m+k])

        for j in range(1, t):

            P = Profile(Motifs[0:j])

            Motifs.append(ProfileMostProbablePattern(Dna[j], k, P))

        if Score(Motifs) < Score(BestMotifs):

            BestMotifs = Motifs

    return BestMotifs

Dna = ["GCGCCCCGCCCGGACAGCCATGCGCTAACCCTGGCTTCGATGGCGCCGGCTCAGTTAGGGCCGGAAGTCCCCAATGTGGCAGACCTTTCGCCCCTGGCGGACGAATGACCCCAGTGGCCGGGACTTCAGGCCCTATCGGAGGGCTCCGGCGCGGTGGTCGGATTTGTCTGTGGAGGTTACACCCCAATCGCAAGGATGCATTATGACCAGCGAGCTGAGCCTGGTCGCCACTGGAAAGGGGAGCAACATC", "CCGATCGGCATCACTATCGGTCCTGCGGCCGCCCATAGCGCTATATCCGGCTGGTGAAATCAATTGACAACCTTCGACTTTGAGGTGGCCTACGGCGAGGACAAGCCAGGCAAGCCAGCTGCCTCAACGCGCGCCAGTACGGGTCCATCGACCCGCGGCCCACGGGTCAAACGACCCTAGTGTTCGCTACGACGTGGTCGTACCTTCGGCAGCAGATCAGCAATAGCACCCCGACTCGAGGAGGATCCCG", "ACCGTCGATGTGCCCGGTCGCGCCGCGTCCACCTCGGTCATCGACCCCACGATGAGGACGCCATCGGCCGCGACCAAGCCCCGTGAAACTCTGACGGCGTGCTGGCCGGGCTGCGGCACCTGATCACCTTAGGGCACTTGGGCCACCACAACGGGCCGCCGGTCTCGACAGTGGCCACCACCACACAGGTGACTTCCGGCGGGACGTAAGTCCCTAACGCGTCGTTCCGCACGCGGTTAGCTTTGCTGCC", "GGGTCAGGTATATTTATCGCACACTTGGGCACATGACACACAAGCGCCAGAATCCCGGACCGAACCGAGCACCGTGGGTGGGCAGCCTCCATACAGCGATGACCTGATCGATCATCGGCCAGGGCGCCGGGCTTCCAACCGTGGCCGTCTCAGTACCCAGCCTCATTGACCCTTCGACGCATCCACTGCGCGTAAGTCGGCTCAACCCTTTCAAACCGCTGGATTACCGACCGCAGAAAGGGGGCAGGAC", "GTAGGTCAAACCGGGTGTACATACCCGCTCAATCGCCCAGCACTTCGGGCAGATCACCGGGTTTCCCCGGTATCACCAATACTGCCACCAAACACAGCAGGCGGGAAGGGGCGAAAGTCCCTTATCCGACAATAAAACTTCGCTTGTTCGACGCCCGGTTCACCCGATATGCACGGCGCCCAGCCATTCGTGACCGACGTCCCCAGCCCCAAGGCCGAACGACCCTAGGAGCCACGAGCAATTCACAGCG", "CCGCTGGCGACGCTGTTCGCCGGCAGCGTGCGTGACGACTTCGAGCTGCCCGACTACACCTGGTGACCACCGCCGACGGGCACCTCTCCGCCAGGTAGGCACGGTTTGTCGCCGGCAATGTGACCTTTGGGCGCGGTCTTGAGGACCTTCGGCCCCACCCACGAGGCCGCCGCCGGCCGATCGTATGACGTGCAATGTACGCCATAGGGTGCGTGTTACGGCGATTACCTGAAGGCGGCGGTGGTCCGGA", "GGCCAACTGCACCGCGCTCTTGATGACATCGGTGGTCACCATGGTGTCCGGCATGATCAACCTCCGCTGTTCGATATCACCCCGATCTTTCTGAACGGCGGTTGGCAGACAACAGGGTCAATGGTCCCCAAGTGGATCACCGACGGGCGCGGACAAATGGCCCGCGCTTCGGGGACTTCTGTCCCTAGCCCTGGCCACGATGGGCTGGTCGGATCAAAGGCATCCGTTTCCATCGATTAGGAGGCATCAA", "GTACATGTCCAGAGCGAGCCTCAGCTTCTGCGCAGCGACGGAAACTGCCACACTCAAAGCCTACTGGGCGCACGTGTGGCAACGAGTCGATCCACACGAAATGCCGCCGTTGGGCCGCGGACTAGCCGAATTTTCCGGGTGGTGACACAGCCCACATTTGGCATGGGACTTTCGGCCCTGTCCGCGTCCGTGTCGGCCAGACAAGCTTTGGGCATTGGCCACAATCGGGCCACAATCGAAAGCCGAGCAG", "GGCAGCTGTCGGCAACTGTAAGCCATTTCTGGGACTTTGCTGTGAAAAGCTGGGCGATGGTTGTGGACCTGGACGAGCCACCCGTGCGATAGGTGAGATTCATTCTCGCCCTGACGGGTTGCGTCTGTCATCGGTCGATAAGGACTAACGGCCCTCAGGTGGGGACCAACGCCCCTGGGAGATAGCGGTCCCCGCCAGTAACGTACCGCTGAACCGACGGGATGTATCCGCCCCAGCGAAGGAGACGGCG", "TCAGCACCATGACCGCCTGGCCACCAATCGCCCGTAACAAGCGGGACGTCCGCGACGACGCGTGCGCTAGCGCCGTGGCGGTGACAACGACCAGATATGGTCCGAGCACGCGGGCGAACCTCGTGTTCTGGCCTCGGCCAGTTGTGTAGAGCTCATCGCTGTCATCGAGCGATATCCGACCACTGATCCAAGTCGGGGGCTCTGGGGACCGAAGTCCCCGGGCTCGGAGCTATCGGACCTCACGATCACC"]

 

# set t equal to the number of strings in Dna and k equal to 15

k = 15

t = 10

# Call GreedyMotifSearch(Dna, k, t) and store the output in a variable called Motifs

Motifs = GreedyMotifSearch(Dna, k, t)

# Print the Motifs variable

print(Motifs)

# Print Score(Motifs)

print(Score(Motifs))
