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
#### LIB_LaunchEnableForConcurrentThreadsAt_SERVER.h
````
#ifdef LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_EXPORTS
#define LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_API __declspec(dllexport)
#else
#define LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_API __declspec(dllimport)
#endif

namespace Avril_FSD
{
	// This class is exported from the dll
	class LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_API CLIBLaunchEnableForConcurrentThreadsAtSERVER {
		public:
			CLIBLaunchEnableForConcurrentThreadsAtSERVER(void);
			// TODO: add your methods here.
			static void* Initialise_LaunchEnableForConcurrentThreadsAt();

			static void Request_Wait_Launch(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId);
			static void Thread_End(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework*, unsigned char concurrent_CoreId);

			static __int8 Get_coreId_To_Launch(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj);
			static bool Get_Flag_Active(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj);
			static bool Get_Flag_ConcurrentCoreState(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId);
			static bool Get_Flag_Idle(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj);
			static bool Get_State_LaunchBit(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj);
			static void Set_state_ConcurrentCore(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId, bool value);

		private:
			static class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* Get_LaunchEnableForConcurrentThreadsAt_SERVER_Framework();
			static void Set_LaunchEnableForConcurrentThreadsAt_SERVER_Framework(class LaunchEnableForConcurrentThreadsAt_SERVER_Framework* framework);
	};
}
````
#### LIB_LaunchEnableForConcurrentThreadsAt_SERVER.cpp
````
#include "pch.h"
#include "framework.h"
#include "LIB_LaunchEnableForConcurrentThreadsAt_SERVER.h"

class Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* ptr_LaunchEnableForConcurrentThreadsAt_SERVER_Framework = NULL;

// This is an example of an exported variable
LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_API int nLIBLaunchEnableForConcurrentThreadsAtSERVER=0;

// This is an example of an exported function.
LIBLAUNCHENABLEFORCONCURRENTTHREADSATSERVER_API int fnLIBLaunchEnableForConcurrentThreadsAtSERVER(void)
{
    return 0;
}

// This is the constructor of a class that has been exported.
Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::CLIBLaunchEnableForConcurrentThreadsAtSERVER()
{
    return;
}

// This is an example of an exported function.
void* Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Initialise_LaunchEnableForConcurrentThreadsAt()
{
    Set_LaunchEnableForConcurrentThreadsAt_SERVER_Framework(new class Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework());
    while (Get_LaunchEnableForConcurrentThreadsAt_SERVER_Framework() == NULL) {}
    return (void*)Get_LaunchEnableForConcurrentThreadsAt_SERVER_Framework();
}

void Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Request_Wait_Launch(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId)
{
    obj->Get_LaunchEnableForConcurrentThread()->Thread_Start(obj, concurrent_CoreId);
}

void Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Thread_End(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId)
{
    obj->Get_LaunchEnableForConcurrentThread()->Thread_End(obj, concurrent_CoreId);
}

__int8 Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_coreId_To_Launch(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj)
{
    return obj->Get_LaunchEnableForConcurrentThread()->Get_Control_Of_LaunchConcurrency()->Get_que_CoreToLaunch(0);
}

bool Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_Flag_Active(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj)
{
    return obj->Get_LaunchEnableForConcurrentThread()->Get_LaunchConcurrency_Global()->Get_flag_core_ACTIVE();
}

bool Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_Flag_ConcurrentCoreState(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId)
{
    return obj->Get_LaunchEnableForConcurrentThread()->Get_Control_Of_LaunchConcurrency()->Get_state_ConcurrentCore(concurrent_CoreId);
}

bool Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_Flag_Idle(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj)
{
    return obj->Get_LaunchEnableForConcurrentThread()->Get_LaunchConcurrency_Global()->Get_flag_core_IDLE();
}

bool Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_State_LaunchBit(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj)
{
    return obj->Get_LaunchEnableForConcurrentThread()->Get_Control_Of_LaunchConcurrency()->Get_state_ConcurrentCore(0);
}

void Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Set_state_ConcurrentCore(Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* obj, unsigned char concurrent_CoreId, bool value)
{
    obj->Get_LaunchEnableForConcurrentThread()->Get_Control_Of_LaunchConcurrency()->Set_state_ConcurrentCore(concurrent_CoreId, value);
}

Avril_FSD::LaunchEnableForConcurrentThreadsAt_SERVER_Framework* Avril_FSD::CLIBLaunchEnableForConcurrentThreadsAtSERVER::Get_LaunchEnableForConcurrentThreadsAt_SERVER_Framework()
{
    return ptr_LaunchEnableForConcurrentThreadsAt_SERVER_Framework;
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
#### IMPORT_LIB_LaunchEnableForConcurrentThreadsAt_CLIENT.cs
````
using System;
using System.Runtime.InteropServices;
using System.Security;

namespace Avril_FSD
{
    [SuppressUnmanagedCodeSecurity]
    public static class Library_For_LaunchEnableForConcurrentThreadsAt_CLIENT
	{
        [DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Initialise_LaunchEnableForConcurrentThreadsAt@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SAPAXXZ")]
        public static extern IntPtr Initialise_LaunchEnableForConcurrentThreadsAt();

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Request_Wait_Launch@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SAXPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@E@Z")]
		public static extern void Request_Wait_Launch(IntPtr obj, byte concurrent_CoreId);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Thread_End@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SAXPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@E@Z")]
		public static extern void Thread_End(IntPtr obj, byte concurrent_CoreId);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Get_coreId_To_Launch@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SADPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@@Z")]
		public static extern byte Get_coreId_To_Launch(IntPtr obj);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Get_Flag_Active@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SA_NPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@@Z")]
		public static extern bool Get_Flag_Active(IntPtr obj);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Get_Flag_ConcurrentCoreState@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SA_NPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@E@Z")]
		public static extern bool Get_Flag_ConcurrentCoreState(IntPtr obj, byte concurrent_CoreId);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Get_Flag_Idle@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SA_NPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@@Z")]
		public static extern bool Get_Flag_Idle(IntPtr obj);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Get_State_LaunchBit@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SA_NPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@@Z")]
		public static extern bool Get_State_LaunchBit(IntPtr obj);

		[DllImport("LIBLaunchEnableForConcurrentThreadsAtCLIENT.dll", EntryPoint = "?Set_state_ConcurrentCore@CLIBLaunchEnableForConcurrentThreadsAtCLIENT@Avril_FSD@@SAXPAVLaunchEnableForConcurrentThreadsAt_CLIENT_Framework@2@E_N@Z")]
		public static extern void Set_State_ConcurrentCoreState(IntPtr obj, byte concurrent_CoreId, bool value);
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
