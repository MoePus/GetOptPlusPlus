##GetOpt++
GetOpt++ is a featherweight getopt lib written by C++

This is a **headOnly** lib 

##Usage
```
#include "GetOpt++.h"

    std::unordered_map<std::wstring, std::wstring> opts;
    try{
		opts=GetOpt::getOpt( L"i:o:input:output", GetCommandLineW());
	}
	catch (GetOpt::optException exp)
	{
		wcout << exp.getException() << endl;
	}

	wcout << opts[L"output"] << endl;
	wcout << opts[L"input"] << endl;
	wcout << opts[L"i"] << endl;
	wcout << opts[L"o"] << endl;
```
with args
```
--output myout --input myin -i I -o O -o O2
```
it will output
```
myout
myin
I
O2
```
