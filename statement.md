# description: 
 3 times.  One time for the first virtual occurences of BS in the heirarchy and once for each non-virtual occurence of BS.  mid1 and mid2 together have one.  mid3 and mid4 each have one.
```C++ runnable
#include <iostream>

struct BS
{
  BS()
  {
    std::cout << "Hello World" << std::endl;
  }
  unsigned int color;
};

struct mid1 : virtual public BS { };
struct mid2 : virtual public BS { };
struct mid3 : public BS { };
struct mid4 : public BS { };

struct DR : public mid1, public mid2, 
            public mid3, public mid4 { };

int main(int argc, char** argv) 
{ 
  DR d;
  return 0; 
}
