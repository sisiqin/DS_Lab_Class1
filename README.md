#### (1) Write a function **countVowels** to count up the number of vowels contained in a given string. Valid vowels are: 'a', 'e', 'i', 'o', 'u'. 
#####For example, countVowels('aeiou') should return 5. 


    def countVowels(n):
    count_number = 0
    for i in n:
        if i in "aeiouAEIOU":
            count_number +=1
    return count_number
#### (2) Write a function count_nyc to count up the number of times the string 'nyc' occurs in a given string.
#####For example, count_nyc('Welcome to nyc(NYC) DATA SCIENCE ACADEMY!') should return 1, which means the function is case sensitive, "NYC" is not equivalent to "nyc".

    def count_nyc(s):
    count = 0
    if len(s)<3: 
        return 0
    for i in range(len(s)-2):
        if s[i] =='n' and s[i+1] =='y' and s[i+2] =='c': 
            count+=1
    return count


####(3) Write a function countString with two arguments raw_string and string_to_count. Your function should return the number of times of string_to_count occurs in the the raw_string argument. In addition, Your function should be case insensitive in this time.
#####For example, countString('welcome to nyc(NYC) data science academy!', 'nyc') should return 2.

    def  countString(raw_string, string_to_count):
    lower_raw_string = raw_string.lower()
    lower_string_to_count = string_to_count.lower()
    return lower_raw_string.count(lower_string_to_count, 0, len(lower_raw_string))
