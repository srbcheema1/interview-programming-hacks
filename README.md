# Interview-programming-hacks
#### This repository contains simple hacks that you must remember for interview programming contest.

## Strings
  - string to integer
    - res = std::stoi(str)
  - integer to string
    - res = std::to_string(x)
  - reverse string
    - std::reverse(str.begin(),str.end())
  - string to char array
    - const char * a = str.c_str()  // this returns const pointer
    - char a[str.size() + 1];
    - strcpy(a,str.c_str()] // copy const c_string into non-const c_string
  - char array to string
    - char a[] = "helloworld";
    - std::string res = std::string(ch)
  - substring of string
    - string a = str.substr(i,l) // here it does [i,i+l)
    
## Char
  - check if char is digit, alpha or alphanumeric
    - isdigit(ch), isalpha(ch), isalnum(ch)
    
## vectors
  - copy a vector into another
    - another_vec.assign(vec.begin(),vec.end())
      - assign will erase old content of the another_vec that is assigned.
  - fill a vector with some number
    - std::fill(vec.begin(),vec.end(),0)
    - std::fill(vec.begin(),vec.end(),vector<int>(m,0)) // fill 2D array with 0.
    
## Map
  - iterate over map
    - instead of using for each loop use:
      - for(map<int,int>::iterator x = freq.begin(); x!=freq.end(); x++) int a = x->first, b = x->second;
        - remember that we cant use comparision operator sometimes, always write `x!=freq.end()`


# C language tricks
  - pass 2d array to function
    - instead of passing 2D array to function declare a global array and use it.
 
## python language tricks
  - declare 2d array
    - a = [[0] * cols for _ in range(rows)]
    - a = [[0] * cols] * rows     # wrong way coz inner arrays are reffering to same array.
