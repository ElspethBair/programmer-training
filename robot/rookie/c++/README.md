#Introduction to C++
Here you will learn the basics of the main language that robot programming uses, C++

###C++ Program Structure

Every C++ program starts with *include statements*. They let you use functions and classes that have been declared in other *header files*. 
  example:
    
    #include <iostream>

(The header `<iostream>` gives you access to input and output helpers, like std::cin and std::out. )

`include` statements are the equivalent of `import` statements. 

Another important part of your program is the *main function definition*. This defines a **special** function called "main" that tells the computer where to begin executing code. 

At the end of, but still inside your main function, add a return statement:
    
    return 0;

At this point, the `return` statement is not technically required, but it is good practice. This is an error code for your program - a value of 0 tells the computer that the program has finished executing successfully. 

The next, very important part of your program is the *executable code*. This is the code that actually runs in your program. The executable code is inside your main function. 

An example of a running program:

    #include <iostream>

    int main() {
      int x = 527;
      int result = 2 * x;
      std::cout << “The answer is: “ << result << std::endl;

      return 0;
    }


    


### Differences from Python

**Type Declarations**

In C++, the computer doesn't automatically assume what type the variable is. You have to explicity declare the type. 

example:
    
    float age = 15;

We have to tell the computer that the variable age is a float, because it won't recognize that itself. 

**Console Input/Output**

Including `<iostream>` allows you to use `std::cin` and `std::cout`. `std::cout` is the C++ equivalent of the `print()` function in Python. `std::cin` is the C++ equivalent of the `input()` function. 

**More Misc. Initialization Syntax** 

    TypeName var_name = to_copy;
    TypeName var_name {param1, param2};
    auto var_name = TypeName{param1, param2};

(this is pseudocode)

**Function Declaration**

 in Python:

     def squared(x):
     	return x * x

     print (squared(5))

 the same function in C++:

     int Squared(int x) {
     	return x * x;
     }

     std::cout << Squared(5) << std::endl;

When you declare a function in C++, you have to also declare the type that whatever the function returns will be. In the above function, saying `int Squared` means that the function will return a variable of the type `int`.

**Strings**

C++:

    std::string msg = "A string in C++";

Python: 

    msg = "A string in Python"
 
**Classes**

Python: 

     class Person:
       // Initialize firstName and lastName
       def __init__(self, first, last):
         self.firstName = first
         self.lastName = last

      def greet(self,name):
         return "Hi, “,name,”! I'm ”,self.firstName, self.lastName,”!"

C++:

     class Person {
      public:
       // Initialize first_name and last_name
       Person(std::string first, std::string last) : 
       first_name(first), last_name(last) {}

       std::string Greet(std::string name) {
          return "Hi, " + name + "! I'm " + first_name + " " + last_name + "!";
      }
  
     private:
      std::string first_name, last_name;
    };

In Python, constructors are always called `__init__`, however in C++, when you are naming your constructors, it is important that the constructor always has the same name as the class. For example, in the class above, the calss is named Person, and so is the constructor. 

**Dynamic-size Arrays**

A dynamic size array is an array that can be added to or taken away from. They are used to store values. 
C++:

    auto nums = std::vector<int> {1,2,3,5,7,11};
    std::vector<std::string> strings = {"hello", "how are you", "goodbye"};

    // Iteration
for (int n = 0; n < 8; n++){

      std::cout << n << std::endl;
    }

    // Check size
    std::cout << nums.size() << std::endl;

    nums.push_back(7); // Add value

Python:

    nums = [1,2,3,5,7,11]
    strings = ["hello", "how are you", "goodbye"]

    // Iteration
    for n in nums:
      print(n)

    // Check size
    println(len(num))

    nums.append(7) // Add value

(`std::vector` is defined in `<vector>` so remember to add it in your includes!)
