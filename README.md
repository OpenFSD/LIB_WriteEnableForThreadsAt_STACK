# Avril - LIBRARY Template for Write Enable For Threads At Stack.
# Request, Wait, Write for Thread access to Stack Control.

## Similar Repository
 - https://github.com/cameron314/readerwriterqueue

# Request, Wait, Write for Threads at Stack Control, Dynamic Link Library.

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

### C#
#### IMPORT_LIB_WriteEnableForThreadsAt_CLIENTINPUTACTION
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
#### IMPORT_LIB_WriteEnableForThreadsAt_SERVERINPUTACTION
````
﻿using System.Runtime.InteropServices;
using System.Security;

namespace Avril_FSD
{
    [SuppressUnmanagedCodeSecurity]
    public static class Library_For_WriteEnableForThreadsAt_SERVERINPUTACTION
    {
        [DllImport("LIBWriteEnableForThreadsAtSERVERINPUTACTION.dll", EntryPoint = "?Initialise_WriteEnable@Library_WriteEnableForThreadsAt_SERVERINPUTACTION@Avril_FSD@@SAPAXXZ")]
        public static extern IntPtr Initialise_WriteEnable();

        [DllImport("LIBWriteEnableForThreadsAtSERVERINPUTACTION.dll", EntryPoint = "?Write_End@Library_WriteEnableForThreadsAt_SERVERINPUTACTION@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_SERVERINPUTACTION_Framework@2@E@Z")]
        public static extern void Write_End(IntPtr obj, byte coreId);

        [DllImport("LIBWriteEnableForThreadsAtSERVERINPUTACTION.dll", EntryPoint = "?Write_Start@Library_WriteEnableForThreadsAt_SERVERINPUTACTION@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_SERVERINPUTACTION_Framework@2@E@Z")]
        public static extern void Write_Start(IntPtr obj, byte coreId);
    }
}
````
#### IMPORT_LIB_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE
````
﻿using System.Runtime.InteropServices;
using System.Security;

namespace Avril_FSD
{
    [SuppressUnmanagedCodeSecurity]
    public static class Library_For_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE
    {
        [DllImport("LIBWriteEnableForThreadsAtSERVEROUTPUTRECIEVE.dll", EntryPoint = "?Initialise_WriteEnable@Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE@Avril_FSD@@SAPAXXZ")]
        public static extern IntPtr Initialise_WriteEnable();

        [DllImport("LIBWriteEnableForThreadsAtSERVEROUTPUTRECIEVE.dll", EntryPoint = "?Write_End@Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework@2@E@Z")]
        public static extern void Write_End(IntPtr obj, byte coreId);

        [DllImport("LIBWriteEnableForThreadsAtSERVEROUTPUTRECIEVE.dll", EntryPoint = "?Write_Start@Library_WriteEnableForThreadsAt_SERVEROUTPUTRECIEVE@Avril_FSD@@SAXPAVWriteEnableForThreadsAt_SERVEROUTPUTRECIEVE_Framework@2@E@Z")]
        public static extern void Write_Start(IntPtr obj, byte coreId);
    }
}
````
#### IMPORT_LIB_WriteEnableForThreadsAt_CLIENTOUTPUTRECIEVE
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
