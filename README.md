# Avril - LIBRARY Template for Write Enable For Threads At Stack.
## Request, Wait, Write for Threads at Stack Control, Dynamic Link Library.

## Similar Repository
 - https://github.com/cameron314/readerwriterqueue

### Using C++

### Using Windows 11 Home
Edition: Windows 11 Home OEM System Builder

Version: 24H2

### Using Microsoft Visual Studio Professional 2022 (64-bit) - Current

Version 17.13.4

## TestBench
 - 

## Using
### C++
#### LIB_WriteEnableForThreadsAt_SERVERINPUTACTION.h
````
#ifdef LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_EXPORTS
#define LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_API __declspec(dllexport)
#else
#define LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_API __declspec(dllimport)
#endif


namespace Avril_FSD
{
	// This class is exported from the dll
	class LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_API CLIBWriteEnableForThreadsAtSERVERINPUTACTION {
	public:
		CLIBWriteEnableForThreadsAtSERVERINPUTACTION(void);
		// TODO: add your methods here.
		static void* Initialise_WriteEnable();
		static void Write_End(class WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* obj, unsigned char coreId);
		static void Write_Start(class WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* obj, unsigned char coreId);

	private:
		static class WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* Get_Framework_WriteEnable();
		static void Set_writeEnable(class WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* writeEnable);
	};
}
````
#### LIB_WriteEnableForThreadsAt_SERVERINPUTACTION.cpp
````
#include "pch.h"
#include "framework.h"
#include "LIB_WriteEnableForThreadsAt_SERVERINPUTACTION.h"

Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* ptr_WriteEnableForThreadsAt_SERVERINPUTACTION_Framework = NULL;

// This is an example of an exported variable
LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_API int nLIBWriteEnableForThreadsAtSERVERINPUTACTION=0;

// This is an example of an exported function.
LIBWRITEENABLEFORTHREADSATSERVERINPUTACTION_API int fnLIBWriteEnableForThreadsAtSERVERINPUTACTION(void)
{
    return 0;
}
void* Avril_FSD::CLIBWriteEnableForThreadsAtSERVERINPUTACTION::Initialise_WriteEnable()
{
    Set_writeEnable(new class Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework());
    while (Get_Framework_WriteEnable() == NULL) {}
    return (void*)Get_Framework_WriteEnable();
}
void Avril_FSD::CLIBWriteEnableForThreadsAtSERVERINPUTACTION::Write_End(Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* obj, unsigned char coreId)
{
    obj->Get_writeEnable()->Write_End(obj, coreId);
}
void Avril_FSD::CLIBWriteEnableForThreadsAtSERVERINPUTACTION::Write_Start(Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* obj, unsigned char coreId)
{
    obj->Get_writeEnable()->Write_Start(obj, coreId);
}
Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* Avril_FSD::CLIBWriteEnableForThreadsAtSERVERINPUTACTION::Get_Framework_WriteEnable()
{
    return ptr_WriteEnableForThreadsAt_SERVERINPUTACTION_Framework;
}
void Avril_FSD::CLIBWriteEnableForThreadsAtSERVERINPUTACTION::Set_writeEnable(Avril_FSD::WriteEnableForThreadsAt_SERVERINPUTACTION_Framework* writeEnable)
{
    ptr_WriteEnableForThreadsAt_SERVERINPUTACTION_Framework = writeEnable;
}
````
#### LIB_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE.h
````
#ifdef LIBWRITEENABLEFORTHREADSATSERVEROUTPUTRECIEVE_EXPORTS
#define LIBWRITEENABLEFORTHREADSATSERVEROUTPUTRECIEVE_API __declspec(dllexport)
#else
#define LIBWRITEENABLEFORTHREADSATSERVEROUTPUTRECIEVE_API __declspec(dllimport)
#endif

namespace Avril_FSD
{
	class LIBWRITEENABLEFORTHREADSATSERVEROUTPUTRECIEVE_API Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE {
	public:
		Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE();
		static void* Initialise_WriteEnable();
		static void Write_End(class WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* obj, unsigned char coreId);
		static void Write_Start(class WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* obj, unsigned char coreId);

	private:
		static class WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* Get_Framework_WriteEnable();
		static void Set_writeEnable(class WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* writeEnable);
	};
}
````
#### LIB_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE.cpp
````
#include "pch.h"
#include "LIB_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE.h"

Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* ptr_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework = NULL;

Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE()
{

}
void* Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Initialise_WriteEnable()
{
    Set_writeEnable(new class Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework());
    while (Get_Framework_WriteEnable() == NULL) {}
    return (void*)Get_Framework_WriteEnable();
}
void Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Write_End(Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* obj, unsigned char coreId)
{
    obj->Get_writeEnable()->Write_End(obj, coreId);
}
void Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Write_Start(Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* obj, unsigned char coreId)
{
    obj->Get_writeEnable()->Write_Start(obj, coreId);
}
Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Get_Framework_WriteEnable()
{
    return ptr_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework;
}
void Avril_FSD::Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE::Set_writeEnable(Avril_FSD::WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework* writeEnable)
{
    ptr_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework = writeEnable;
}
````

### C#
#### IMPORT_LIB_WriteEnableForThreadsAt_CLIENTINPUTACTION.cs
````
﻿using System.Runtime.InteropServices;
using System.Security;
using System;

namespace Avril_FSD
{
    [SuppressUnmanagedCodeSecurity]
    public static class Library_For_WriteEnableForThreadsAt_CLIENTINPUTACTION
    {
        [DllImport("LIBWriteEnableForThreadsAtCLIENTINPUTACTION.dll", EntryPoint = "?Initialise_WriteEnable@Library_WriteEnableForThreadsAt_CLIENTINPUTACTION@Avril_FSD@@SAPAXXZ")]
        public static extern IntPtr Initialise_WriteEnable();

        [DllImport("LIBWriteEnableForThreadsAtCLIENTINPUTACTION.dll", EntryPoint = "?Write_End@Library_WriteEnableForThreadsAt_CLIENTINPUTACTION@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_CLIENTINPUTACTION_Framework@2@E@Z")]
        public static extern void Write_End(IntPtr obj, byte coreId);

        [DllImport("LIBWriteEnableForThreadsAtCLIENTINPUTACTION.dll", EntryPoint = "?Write_Start@Library_WriteEnableForThreadsAt_CLIENTINPUTACTION@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_CLIENTINPUTACTION_Framework@2@E@Z")]
        public static extern void Write_Start(IntPtr obj, byte coreId);
    }
}
````
#### IMPORT_LIB_WriteEnableForThreadsAt_CLIENTOUTPUTRECIEVE.cs
````
using System;
using System.Runtime.InteropServices;
using System.Security;

namespace Avril_FSD
{
    [SuppressUnmanagedCodeSecurity]
    public static class Library_For_WriteEnableForThreadsAt_CLIENTOUTPUTRECIEVE
    {
        [DllImport("LIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE.dll", EntryPoint = "?Initialise_WriteEnable@CLIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE@Avril_FSD@@SAPAXXZ")]
        public static extern IntPtr Initialise_WriteEnable();

        [DllImport("LIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE.dll", EntryPoint = "?Write_End@CLIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_STACK_Framework@2@E@Z")]
        public static extern void Write_End(IntPtr obj, byte coreId);

        [DllImport("LIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE.dll", EntryPoint = "?Write_Start@CLIBWriteEnableForThreadsAtCLIENTOUTPUTRECIEVE@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_STACK_Framework@2@E@Z")]
        public static extern void Write_Start(IntPtr obj, byte coreId);
    }
}
````
