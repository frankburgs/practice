
# Books
- dart e-book program

# C++ Homework
- rename file as needed
- save as .doc

# Deadlines
- Discussions by Friday
- Responses and homework and quizzes by Sunday



https://youtu.be/8jLOx1hD3_o?t=41640


# C++
- direct/uniform initialization 

## memory
- system
- stack: stores local variables
  dev is not in control of memory lifetime (scope mechanism)
- heap: additional memory that can be queried @ run time
  dev in full control of memory here (new and delete operators)

- data:
- text: ide?

## conventions
- variable names must start with a letter

## strings
- end an array of chars with \0 for cpp to recognize end of string
- this is a cstring and is null terminated

## memory
- using keyword new adds allocates memory on the heap
- use keyword delete to manage memory, and reassign related pointers to nullptr
- never delete twice

## ********************* CODE EXAMPLE ********************************
``` c++
std::cin >> name >> age; // single line gets two inputs

std::getline(std::cin,full_name); // get whole line as one variable

int number1 = 15;
int number2 = 017;
int number3 = 0x0f; // 0x in front denotes hexadecimal, and c++ knows it
int number4 = 0b00001111;

int count{}; // initializes to zero

int count; // initializes with possible garbage
int number5; // outputs garbo
int number6{}; // ouputs 0

int x = 9.999f; // if you don't include the suffix it will be defaultly interpreted as a double

std::boolalpha // outputs booleans as alpha instead of numeric

int* p_number{}; // initializes as a nullptr, never use uninitialized ptrs
// never do *p_number = 33; as this is writing to nowhere
int int1 = 43;
int int2 = 45;
int *p_int{&int1}; // output of p_int is 43
p_int = &int2; // re-assigns the pointer

*p_int = 55; // re-assign the value located at that memory address

char * p_message { "hello mundo" }; // points to the first character of the string
const char * message2 {"hello k"};
char message1[] {"hello there"};
message1[0] = "t";

int *p_number1{};
p_number1 = new int; // Our memory on the heap not the stack
// alternately use new int (21) or new int{21}
delete p_number1;
p_number1 = nullptr;

// memory checks, std::nothrow is another approach
for (size_t i{} ; i < 1000000000 ; ++i>){
  try{
    int* lots_of_ints { new int[10000000]};
  }catch(std::exception& ex){
    std::cout << "caught exception " << ex.what() << std::endl;
  }
}

```
