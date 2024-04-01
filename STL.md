#### Strings
- `stoi()` to get integer from string.\\
  NOTE: In case of negative numbers, they'll be rotated.
- Indexing a string would result in a char.
  ```cpp
  std::string s = "123"; \\s[0] is a char '1' with ascii 49
  ```
- `+` can be used to concatenate two strings.
- 
#### Tuple
- Used to store a collection of different types. The values assigned must be in the order of declaration.
  ```cpp
  // Declaring & assigning tuple
  tuple <char, int, float> geek;
  geek = make_tuple('a', 10, 15.5);
  
  // tuple <char, int, float> geek = make_tuple('a', 10, 15.5);
  // tuple <char, int, float>geek = {'a', 10, 15.5};

  cout << "The initial values of tuple are : ";
  cout << get<0>(geek) << " " << get<1>(geek) << " " << get<2>(geek) << endl;
  // C++ code to demonstrate tuple, get() and make_pair()
  // Use of get() to change values of tuple
  get<0>(geek) = 'b';
  
  // Printing modified tuple values
  cout << "The modified values of tuple are : ";
  cout << get<0>(geek) << " " << get<1>(geek) << " " << get<2>(geek) << endl;
  ```

#### Unordered set (most operations are O(1) - amortized constant)
  ```cpp
  std::unordered_set<std::string> str_lkup;
  str_lkup.insert("ab");  // insert
  str_lkup.erase("ab");  // remove
  ```
  - set of tuple: `std::unordered_set<std::tuple<int, int>> tup_lkup;`
#### Set
- Stores collections in sorted fashion and unique numbers.
  ```cpp
  std::set<int> a_set;
  a_set.insert(2); //{2}
  a_set.insert(0);  //{0, 2}
  a_set.insert(2);  //{0, 2}
  ```
- soreted in descending: `std::set<int, greater<int>> rev_set` it will have {2, 0}.
#### Unordered map (`unordered_map`)
- `unordered_map<string, double> umap; // Declaration`
- `umap["a"] = 97;` or `umap.insert({"a", 97})` for insertion.
- Element non-existant `umap.find(key) == umap.end()`
- Erase `umap.erase(key)` or `umap.erase(umap.begin())` or `auto itr = umap.being(); it++; umap.erase(it, umap.end()); // delete all except for the first`
