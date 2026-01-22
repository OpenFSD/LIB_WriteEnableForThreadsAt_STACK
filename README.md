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
#### LIB_Server_IO_Concurrnecy.header
````
#ifdef LIBSERVERIOCONCURRNECY_EXPORTS
#define LIBSERVERIOCONCURRNECY_API __declspec(dllexport)
#else
#define LIBSERVERIOCONCURRNECY_API __declspec(dllimport)
#endif

namespace Avril_FSD
{
	// This class is exported from the dll
	class LIBSERVERIOCONCURRNECY_API CLIBServerIOConcurrnecy {
	public:
		CLIBServerIOConcurrnecy(void);
		// TODO: add your methods here.
		static void* Initialise_Server_Concurrency();
		static void Initalise_Programs(class Avril_FSD::Framework_Server* obj);
		static void Flip_InBufferToWrite(class Avril_FSD::Framework_Server* obj);
		static void Flip_OutBufferToWrite(class Avril_FSD::Framework_Server* obj);
		static bool Get_flag_isNewInputDataReady(class Avril_FSD::Framework_Server* obj);
		static bool Get_flag_isNewOutputDataReady(class Avril_FSD::Framework_Server* obj);
		static bool Get_flag_IsStackLoaded_Server_InputAction(class Avril_FSD::Framework_Server* obj);
		static bool Get_flag_IsStackLoaded_Server_OutputRecieve(class Avril_FSD::Framework_Server* obj);
		static bool Get_flag_IsInitialised_Avril_FSD_ServerConcurrency(class Avril_FSD::Framework_Server* obj);
		static void* Get_program_WriteEnableStack_ServerInputAction();
		static void* Get_program_WriteEnableStack_ServerOutputRecieve();
		static void Pop_Stack_Output(class Avril_FSD::Framework_Server* obj);
		static void Push_Stack_InputPraises(class Avril_FSD::Framework_Server* obj);
		static void Select_Set_Intput_Subset(class Avril_FSD::Framework_Server* obj, __int8 praiseEventId);
		static void Set_flag_IsNewInputDataReady(class Avril_FSD::Framework_Server* obj, bool value);
		static void Set_flag_IsNewOutputDataReady(class Avril_FSD::Framework_Server* obj, bool value);

		// Praise Event Id
		static __int8 Get_PraiseEventId(class Avril_FSD::Framework_Server* obj);
		static void Set_PraiseEventId(class Avril_FSD::Framework_Server* obj, __int8 value);
		// Praise 0 Data
		static bool Get_Praise0_Input_IsPingActive(class Avril_FSD::Framework_Server* obj);
		static void Set_Praise0_Input_IsPingActive(class Avril_FSD::Framework_Server* obj, bool value);
		static bool Get_Praise0_Output_IsPingActive(class Avril_FSD::Framework_Server* obj);
		static void Set_Praise0_Output_IsPingActive(class Avril_FSD::Framework_Server* obj, bool value);
		// Praise 1 Data
		static float Get_Praise1_Input_mouseDelta_X(class Avril_FSD::Framework_Server* obj);
		static float Get_Praise1_Input_mouseDelta_Y(class Avril_FSD::Framework_Server* obj);
		static void Set_Praise1_Input_mouseDelta_X(class Avril_FSD::Framework_Server* obj, float value);
		static void Set_Praise1_Input_mouseDelta_Y(class Avril_FSD::Framework_Server* obj, float value);
		static Eigen::Vector3d Get_Praise1_Output_Player_Fowards(class Avril_FSD::Framework_Server* obj);
		static Eigen::Vector3d Get_Praise1_Output_Player_Up(class Avril_FSD::Framework_Server* obj);
		static Eigen::Vector3d Get_Praise1_Output_Player_Right(class Avril_FSD::Framework_Server* obj);
		static void Set_Praise1_Output_Player_Fowards(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value);
		static void Set_Praise1_Output_Player_Up(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value);
		static void Set_Praise1_Output_Player_Right(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value);
		// Praise 0 Data

		// TODO: add your methods here.


	};
}
extern LIBSERVERIOCONCURRNECY_API int nLIBServerIOConcurrnecy;

LIBSERVERIOCONCURRNECY_API int fnLIBServerIOConcurrnecy(void);
````
##### LIB_Server_IO_Concurrnecy.cpp
````
#include "pch.h"
#include "framework.h"
#include "LIB_Server_IO_Concurrnecy.h"

class Avril_FSD::Framework_Server* _Server_Assembly;
void* programHandleId_WriteEnalbe_ServerInputAction;
void* programHandleId_WriteEnalbe_ServerOutputRecieve;

bool _flag_isNewInputDataReady;
bool _flag_isNewOutputDataReady;
bool _flag_IsStackLoaded_Server_InputAction;
bool _flag_IsStackLoaded_Server_OutputRecieve;
bool _flag_IsInitialised_Avril_FSD_ServerAssembly;

// Praise Event Id
__int8 _PraiseEventId;

// Praise 0 Data
bool _Praise0_Input_IsPingActive;
bool _Praise0_Output_IsPingActive;

// Praise 1 Data
float _Praise1_Input_mouseDelta_X;
float _Praise1_Input_mouseDelta_Y;
Eigen::Vector3d _praise1_Output_Player_Camera_Fowards;
Eigen::Vector3d _praise1_Output_Player_Camera_Up;
Eigen::Vector3d _praise1_Output_Player_Camera_Right;

// This is an example of an exported variable
LIBSERVERIOCONCURRNECY_API int nLIBServerIOConcurrnecy=0;

// This is an example of an exported function.
LIBSERVERIOCONCURRNECY_API int fnLIBServerIOConcurrnecy(void)
{
    return 0;
}
void* Avril_FSD::CLIBServerIOConcurrnecy::Initialise_Server_Concurrency()
{
    _Server_Assembly = new class Avril_FSD::Framework_Server();
    while (_Server_Assembly == NULL) {}
    return (void*)_Server_Assembly;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Initalise_Programs(Avril_FSD::Framework_Server* obj)
{
    obj->Initialise_Program(obj);
}
void Avril_FSD::CLIBServerIOConcurrnecy::Flip_InBufferToWrite(Avril_FSD::Framework_Server* obj)
{
    obj->Get_Server_Assembly()->Get_Data()->Flip_Input_DoubleBuffer();
}

void Avril_FSD::CLIBServerIOConcurrnecy::Flip_OutBufferToWrite(Avril_FSD::Framework_Server* obj)
{
    obj->Get_Server_Assembly()->Get_Data()->Flip_Output_DoubleBuffer();
}

bool Avril_FSD::CLIBServerIOConcurrnecy::Get_flag_isNewInputDataReady(Avril_FSD::Framework_Server* obj)
{
    _flag_isNewInputDataReady = obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Get_flag_IsNewInputDataReady();
    return _flag_isNewInputDataReady; 
}

bool Avril_FSD::CLIBServerIOConcurrnecy::Get_flag_isNewOutputDataReady(Avril_FSD::Framework_Server* obj)
{
    _flag_isNewOutputDataReady = obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Get_flag_IsNewOutputDataReady();
    return _flag_isNewOutputDataReady;
}

bool Avril_FSD::CLIBServerIOConcurrnecy::Get_flag_IsStackLoaded_Server_InputAction(class Avril_FSD::Framework_Server* obj)
{
    _flag_IsStackLoaded_Server_InputAction = obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Get_flag_IsStackLoaded_Server_InputAction();
    return _flag_IsStackLoaded_Server_InputAction;
}
bool Avril_FSD::CLIBServerIOConcurrnecy::Get_flag_IsStackLoaded_Server_OutputRecieve(class Avril_FSD::Framework_Server* obj)
{
    _flag_IsStackLoaded_Server_OutputRecieve = obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Get_flag_IsStackLoaded_Server_OutputRecieve();
    return _flag_IsStackLoaded_Server_OutputRecieve;
}
bool Avril_FSD::CLIBServerIOConcurrnecy::Get_flag_IsInitialised_Avril_FSD_ServerConcurrency(class Avril_FSD::Framework_Server* obj)
{
    _flag_IsInitialised_Avril_FSD_ServerAssembly = obj->Get_Server_Assembly()->Get_Execute()->Get_Control_Of_Execute()->GetFlag_SystemInitialised(obj);
    return _flag_IsInitialised_Avril_FSD_ServerAssembly;
}
void* Avril_FSD::CLIBServerIOConcurrnecy::Get_program_WriteEnableStack_ServerInputAction()
{
    return (void*)programHandleId_WriteEnalbe_ServerInputAction;
}
void* Avril_FSD::CLIBServerIOConcurrnecy::Get_program_WriteEnableStack_ServerOutputRecieve()
{
    return (void*)programHandleId_WriteEnalbe_ServerOutputRecieve;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Pop_Stack_Output(class Avril_FSD::Framework_Server* obj)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Pop_Stack_Output(obj);
}
void Avril_FSD::CLIBServerIOConcurrnecy::Push_Stack_InputPraises(class Avril_FSD::Framework_Server* obj)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Push_Stack_InputPraises(obj);
}

void Avril_FSD::CLIBServerIOConcurrnecy::Select_Set_Intput_Subset(class Avril_FSD::Framework_Server* obj, __int8 praiseEventId)
{
    obj->Get_Server_Assembly()->Get_Data()->GetBuffer_InputFrontDouble()->Get_Input_Control()->SelectSet_Input_Subset(obj, praiseEventId);
}

void Avril_FSD::CLIBServerIOConcurrnecy::Set_flag_IsNewInputDataReady(Avril_FSD::Framework_Server* obj, bool value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Set_flag_IsNewInputDataReady(value);
}

void Avril_FSD::CLIBServerIOConcurrnecy::Set_flag_IsNewOutputDataReady(Avril_FSD::Framework_Server* obj, bool value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_Data_Control()->Set_flag_IsNewOutputDataReady(value);
}

__int8 Avril_FSD::CLIBServerIOConcurrnecy::Get_PraiseEventId(class Avril_FSD::Framework_Server* obj)
{
    _PraiseEventId = obj->Get_Server_Assembly()->Get_Data()->GetBuffer_OutputBackDouble()->Get_out_praiseEventId();
    return _PraiseEventId;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_PraiseEventId(class Avril_FSD::Framework_Server* obj, __int8 value)
{
    obj->Get_Server_Assembly()->Get_Data()->GetBuffer_InputBackDouble()->Set_in_praiseEventId(value);
}
//
bool Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise0_Input_IsPingActive(class Avril_FSD::Framework_Server* obj)
{
    _Praise0_Input_IsPingActive = obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise0_Input()->Get_ping_Active();
    return _Praise0_Input_IsPingActive;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise0_Input_IsPingActive(class Avril_FSD::Framework_Server* obj, bool value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise0_Input()->Set_ping_Active(value);
}
bool Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise0_Output_IsPingActive(class Avril_FSD::Framework_Server* obj)
{
    _Praise0_Output_IsPingActive = obj->Get_Server_Assembly()->Get_Data()->Get_User_O()->Get_Praise0_Output()->Get_ping_Active();
    return _Praise0_Output_IsPingActive;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise0_Output_IsPingActive(class Avril_FSD::Framework_Server* obj, bool value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_O()->Get_Praise0_Output()->Set_ping_Active(value);
}
//
float Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise1_Input_mouseDelta_X(class Avril_FSD::Framework_Server* obj)
{
    _Praise1_Input_mouseDelta_X = obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise1_Input()->Get_mouse_X();
    return _Praise1_Input_mouseDelta_X;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise1_Input_mouseDelta_X(class Avril_FSD::Framework_Server* obj, float value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise1_Input()->Set_mouse_X(value);
}
float Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise1_Input_mouseDelta_Y(class Avril_FSD::Framework_Server* obj)
{
    _Praise1_Input_mouseDelta_Y = obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise1_Input()->Get_mouse_Y();
    return _Praise1_Input_mouseDelta_Y;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise1_Input_mouseDelta_Y(class Avril_FSD::Framework_Server* obj, float value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_I()->Get_Praise1_Input()->Set_mouse_Y(value);
}

Eigen::Vector3d Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise1_Output_Player_Fowards(class Avril_FSD::Framework_Server* obj)
{
    Avril_FSD::Praise1_Output* outputSebset = (Avril_FSD::Praise1_Output*)obj->Get_Server_Assembly()->Get_Data()->GetBuffer_OutputFrontDouble()->Get_praiseOutputBuffer_Subset();
    _praise1_Output_Player_Camera_Fowards = outputSebset->GetFowards();
    return _praise1_Output_Player_Camera_Fowards;
}
Eigen::Vector3d Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise1_Output_Player_Up(class Avril_FSD::Framework_Server* obj)
{
    Avril_FSD::Praise1_Output* outputSebset = (Avril_FSD::Praise1_Output*)obj->Get_Server_Assembly()->Get_Data()->GetBuffer_OutputFrontDouble()->Get_praiseOutputBuffer_Subset();
    _praise1_Output_Player_Camera_Up = outputSebset->GetUp();
    return _praise1_Output_Player_Camera_Up;
}
Eigen::Vector3d Avril_FSD::CLIBServerIOConcurrnecy::Get_Praise1_Output_Player_Right(class Avril_FSD::Framework_Server* obj)
{
    Avril_FSD::Praise1_Output* outputSebset = (Avril_FSD::Praise1_Output*)obj->Get_Server_Assembly()->Get_Data()->GetBuffer_OutputFrontDouble()->Get_praiseOutputBuffer_Subset();
    _praise1_Output_Player_Camera_Right = outputSebset->GetRight();
    return _praise1_Output_Player_Camera_Right;
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise1_Output_Player_Fowards(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_O()->Get_Praise1_Output()->SetFowards(value);
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise1_Output_Player_Up(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_O()->Get_Praise1_Output()->SetUp(value);
}
void Avril_FSD::CLIBServerIOConcurrnecy::Set_Praise1_Output_Player_Right(class Avril_FSD::Framework_Server* obj, Eigen::Vector3d value)
{
    obj->Get_Server_Assembly()->Get_Data()->Get_User_O()->Get_Praise1_Output()->SetUp(value);
}
````
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
