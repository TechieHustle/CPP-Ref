#### Tuple
- Used to store a collection of different types. The values assigned must be in the order of declaration.
  ```cpp
  // C++ code to demonstrate tuple, get() and make_pair()
  #include<iostream>
  #include<tuple> // for tuple
  using namespace std;
  int main()
  {
  	// Declaring & assigning tuple
  	tuple <char, int, float> geek;
  	geek = make_tuple('a', 10, 15.5);
    
  	// tuple <char, int, float> geek = make_tuple('a', 10, 15.5);
  	// tuple <char, int, float>geek = {'a', 10, 15.5};
  
  	// Initial tuple values using get()
  	cout << "The initial values of tuple are : ";
  	cout << get<0>(geek) << " " << get<1>(geek) << " " << get<2>(geek) << endl;
  
  	// Use of get() to change values of tuple
  	get<0>(geek) = 'b';
    
  	// Printing modified tuple values
  	cout << "The modified values of tuple are : ";
  	cout << get<0>(geek) << " " << get<1>(geek) << " " << get<2>(geek) << endl;
  
  	return 0;
  }
  ```

