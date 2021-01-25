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
    - std::string res = std::string(a)
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
  - reverse access of vector
    - for(auto x = vec.rbegin(); x != vec.rend(); x++) // note `x++` here, incrementing reverse iterator goes back
  - `upper_bound` vs `lower_bound`, REMEMBER WORD FIRST
    - upper bound is FIRST greater than element
    - lower bound is FIRST greater than or equals to
    - these both are same when element is not found
    - difference of both tell us number of times an element is present
    - HACK-TO-REMEMBER: remember in both the definitions there is word "first"
      - there are 4 things possible, first smaller, first smaller equal, first greater, first greater equals
      - just feel first smaller and first smaller equal has got no significance. as they may always be element 0 mostly.
    
## Map
  - iterate over map
    - instead of using for each loop use:
      - for(map<int,int>::iterator x = freq.begin(); x!=freq.end(); x++) int a = x->first, b = x->second;
        - remember that we cant use comparision operator sometimes, always write `x!=freq.end()`
        
## Bitset
  - assign value
    - bitset<5> a(3); // gets value 3 .. i.e "00011"
    - a = bitset<5>(5); // assigns value to 5 ... i.e "00101"
  - select elem
    - a[1] = 1; a[0]^=1; // here `0 stands for least significant bit`.
  - print bitset
    - cout << a << endl; // same as `a.to_string()`, prints in reverse order, 0th bit at last. here "00110" is 6.
  - convert to integer
    - a.to_ulong() // to convert into unsigned long
    - a.to_ullong() // to convert into unsigned long long
  - NOTE: always while playing with bitset try to use unsigned long long.


# C language tricks
  - pass 2d array to function
    - instead of passing 2D array to function declare a global array and use it.
 
## python language tricks
  - declare 2d array
    - a = [[0] * cols for _ in range(rows)]
    - a = [[0] * cols] * rows     # wrong way coz inner arrays are reffering to same array.
