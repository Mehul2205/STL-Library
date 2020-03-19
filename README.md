# C++ Standard Template Library

# 1. String

```
Header File - #include <cstdio>
```

### Initialzation

```
string s0;                                       // s0 = “”
string s1(“Hello”);                               // s1 = “Hello”
string s2 (s1);                                  // s2 = “Hello”
string s3 (s1, 1, 2);                            // s3 = “el”
string s4 ("Hello World", 5);                     // s4 = “Hello”
string s5 (5, ‘*’);                              // s5 = “*****”
string s6 (s1.begin(), s1.begin()+3);              // s6 = “Hel”
```

* append(): Inserts additional characters at the end of the string. Its time complexity is O(N) where N is the size of the new string.
* assign(): Assigns new string by replacing the previous value.
* at(): Returns the character at a particular position. Its time complexity is O(1).
* begin(): Returns an iterator pointing to the first character. Its time complexity is O(1).
* clear(): Erases all the contents of the string and assign an empty string (“”) of length zero. Its time complexity is O(1).
* compare(): Compares the value of the string with the string passed in the parameter and returns an integer accordingly. Its time complexity is O(N + M) where N is the size of the first string and M is the size of the second string.
* copy(): Copies the substring of the string in the string passed as parameter and returns the number of characters copied. Its time complexity is O(N) where N is the size of the copied string.
* c_str(): Convert the string into C-style string (null terminated string) and returns the pointer to the C-style string. Its time complexity is O(1).
* empty(): Returns a boolean value, true if the string is empty and false if the string is not empty. Its time complexity is O(1).
* end(): Returns an iterator pointing to a position which is next to the last character. Its time complexity is O(1).
* erase(): Deletes a substring of the string. Its time complexity is O(N) where N is the size of the new string.
* find(): Searches the string and returns the first occurrence of the parameter in the string. Its time complexity is O(N) where N is the size of the string.
* insert(): Inserts additional characters into the string at a particular position. Its time complexity is O(N) where N is the size of the new string.
* length(): Returns the length of the string. Its time complexity is O(1).
* replace(): Replaces the particular portion of the string. Its time complexity is O(N) where N is size of the new string.
* resize(): Resize the string to the new length which can be less than or greater than the current length. Its time complexity is O(N) where N is the size of the new string.
* size(): Returns the length of the string. Its time complexity is O(1).
* substr(): Returns a string which is the copy of the substring. Its time complexity is O(N) where N is the size of the substring.

-------------------------------------------------------
# 2. Vector

```
Header File - #include <vector>
```

### Initialization

```
vector<int> a;                                       // empty vector of ints
vector<int> b (5, 10);                                // five ints with value 10
vector<int> c (b.begin(),b.end());                     // iterating through second
vector<int> d (c);                                   // copy of c
```

* at(): Returns the reference to the element at a particular position (can also be done using ‘[ ]’ operator). Its time complexity is O(1).
* back(): Returns the reference to the last element. Its time complexity is O(1).
* begin(): Returns an iterator pointing to the first element of the vector. Its time complexity is O(1).
* clear(): Deletes all the elements from the vector and assign an empty vector. Its time complexity is O(N) where N is the size of the vector.
* empty(): Returns a boolean value, true if the vector is empty and false if the vector is not empty. Its time complexity is O(1).
* end(): Returns an iterator pointing to a position which is next to the last element of the vector. Its time complexity is O(1).
* erase(): Deletes a single element or a range of elements. Its time complexity is O(N + M) where N is the number of the elements erased and M is the number of the elements moved.
* front(): Returns the reference to the first element. Its time complexity is O(1).
* insert(): Inserts new elements into the vector at a particular position. ts time complexity is O(N + M) where N is the number of elements inserted and M is the number of the elements moved .
* pop_back(): Removes the last element from the vector. Its time complexity is O(1).
* push_back(): Inserts a new element at the end of the vector. Its time complexity is O(1).
* resize(): Resizes the vector to the new length which can be less than or greater than the current length. Its time complexity is O(N) where N is the size of the resized vector.
* size(): Returns the number of elements in the vector. Its time complexity is O(1).


### Traversal
```
void traverse(vector<int> v)
{
    vector <int>::iterator it;
    for(it = v.begin();it != v.end();++it)
        cout << *it <<  ‘ ‘;
    cout << endl;
    for(int i = 0;i < v.size();++i)
        cout << v[i] << ‘ ‘;
    cout << endl;
 }
```

-------------------------------------------------------
## 3. List

```
Header File - #include <list>
```

### Initialization

```
list <int> LI;
list<int> LI1(5, 100)                    \\ here LI will have 5 int elements of value 100.
```

* begin( ): It returns an iterator pointing to the first element in list.Its time complexity is O(1).
* end( ): It returns an iterator referring to the theoretical element(doesn’t point to an element) which follows the last element.Its time complexity is O(1).
* empty( ): It returns whether the list is empty or not.It returns 1 if the list is empty otherwise returns 0.Its time complexity is O(1).
* assign( ): It assigns new elements to the list by replacing its current elements and change its size accordingly.It time complexity is O(N).
* back( ): It returns reference to the last element in the list.Its time complexity is O(1).
* erase( ): It removes a single element or the range of element from the list.Its time complexity is O(N).
* front( ): It returns reference to the first element in the list.Its time complexity is O(1).
* push_back( ): It adds a new element at the end of the list, after its current last element. Its time complexity is O(1).
* push_front( ): It adds a new element at the beginning of the list, before its current first element. Its time complexity is O(1).
* remove( ): It removes all the elements from the list, which are equal to given element. Its time complexity is O(N).
* pop_back( ): It removes the last element of the list, thus reducing its size by 1. Its time complexity is O(1).
* pop_front( ): It removes the first element of the list, thus reducing its size by 1. Its time complexity is O(1).
* insert( ): It insert new elements in the list before the element on the specified position. Its time complexity is O(N).
* reverse ( ): It reverses the order of elements in the list. Its time complexity is O(N).
* size( ): It returns the number of elements in the list. Its time complexity is O(1).

-------------------------------------------------------
## 4. Pair

```
Header File - #include <utility>
```

### Initialization

```
pair <int, char> p1;                    // default
pair <int, char> p2 (1, 'a');            // value inititialization
pair <int, char> p3 (p2);               // copy of p2
```

* make_pair(x, y): will return a pair with first element set to x and second element set to y.
* first: return the first element(variable)
* second: return the second element (variable)

-------------------------------------------------------
## 5. Set

```
Header File - #include <set>
```

### Initialization

```
set<int> s1;                               // Empty Set
int a[]= {1, 2, 3, 4, 5, 5};
set<int> s2 (a);                           // s2 = {1, 2, 3, 4, 5}
set<int> s3 (s2);                          // Copy of s2
set<int> s4 (s3.begin(), s3.end());         // Set created using iterators
```

* begin(): Returns an iterator to the first element of the set. Its time complexity is O(1).
* clear(): Deletes all the elements in the set and the set will be empty. Its time complexity is O(N) where N is the size of the set.
* count(): Returns 1 or 0 if the element is in the set or not respectively. Its time complexity is O(logN) where N is the size of the set.
* empty(): Returns true if the set is empty and false if the set has at least one element. Its time complexity is O(1).
* end(): Returns an iterator pointing to a position which is next to the last element. Its time complexity is O(1).
* erase(): Deletes a particular element or a range of elements from the set. Its time complexity is O(N) where N is the number of element deleted.
* find(): Searches for a particular element and returns the iterator pointing to the element if the element is found otherwise it will return the iterator returned by end(). Its time complexity is O(logN) where N is the size of the set.
* insert(): insert a new element. Its time complexity is O(logN) where N is the size of the set.
* size(): Returns the size of the set or the number of elements in the set. Its time complexity is O(1).

-------------------------------------------------------
## 6. Map

```
Header File - #include <map>
```

### Initialization

```
map <char ,int > mp;
mp['b']  = 1;
mp['a']  = 2;
```

* at( ): Returns a reference to the mapped value of the element identified with key.Its time complexity is O(logN).
* count( ): searches the map for the elements mapped by the given key and returns the number of matches.As map stores each element with unique key, then it will return 1 if match if found otherwise return 0.Its time complexity is O(logN).
* clear( ): clears the map, by removing all the elements from the map and leaving it with its size 0.Its time complexity is O(N).
* begin( ): returns an iterator(explained above) referring to the first element of map.Its time complexity is O(1).
* end( ): returns an iterator referring to the theoretical element(doesn’t point to an element) which follows the last element.Its time complexity is O(1).
* empty( ): checks whether the map is empty or not. It doesn’t modify the map.It returns 1 if the map is empty otherwise returns 0.Its time complexity is O(1).
* erase( ): removes a single element or the range of element from the map.
* find( ): Searches the map for the element with the given key, and returns an iterator to it, if it is present in the map otherwise it returns an iterator to the theoretical element which follows the last element of map.Its time complexity is O(logN).
* insert( ): insert a single element or the range of element in the map.Its time complexity is O(logN), when only element is inserted and O(1) when position is also given.

-------------------------------------------------------
