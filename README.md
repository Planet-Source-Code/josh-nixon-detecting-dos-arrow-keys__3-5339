<div align="center">

## \[Detecting Dos Arrow Keys\]


</div>

### Description

This will just show how a person might use the arrow keys in DOS.
 
### More Info
 


<span>             |<span>
---                |---
**Submitted On**   |
**By**             |[Josh Nixon](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByAuthor/josh-nixon.md)
**Level**          |Beginner
**User Rating**    |4.7 (42 globes from 9 users)
**Compatibility**  |C\+\+ \(general\)
**Category**       |[Coding Standards](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByCategory/coding-standards__3-32.md)
**World**          |[C / C\+\+](https://github.com/Planet-Source-Code/PSCIndex/blob/master/ByWorld/c-c.md)
**Archive File**   |[](https://github.com/Planet-Source-Code/josh-nixon-detecting-dos-arrow-keys__3-5339/archive/master.zip)

### API Declarations

```
#include <iostream.h> //cout
#include <conio.h> //kbhit() getch()
```


### Source Code

```
#include <iostream.h>
#include <conio.h> //kbhit() getch()
//Getch()= retrieves the char and wait for it to be pressed
//kbhit() = keeps processing commands while you hit
//These are used for arrow keys since getch() does not return extended char
const char CPPKEYUP = 72;
const char CPPKEYLEFT = 75;
const char CPPKEYRIGHT = 77;
const char CPPKEYDOWN = 80;
int main()
{
 char Arrow = 0;
 Arrow = kbhit();
 while(Arrow !=27)
  {
  Arrow = getch();
   switch(Arrow)
   {
  case CPPKEYUP:
    cout<<" UP "
  break;
  case CPPKEYDOWN:
    cout<<" DOWN "
  break;
  case CPPKEYLEFT:
    cout<<" LEFT "
   break;
 case CPPKEYRIGHT:
    cout<<" RIGHT "
   break;
 }
}
return 0;
}
```

