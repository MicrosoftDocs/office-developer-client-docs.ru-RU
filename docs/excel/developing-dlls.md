---
title: ���������� ��������� DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dlls [excel 2007], creating,creating DLLs [Excel 2007]
localization_priority: Normal
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 030cdd4358d9a71841eca6acfcef6e71839e02a0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807169"
---
# <a name="developing-dlls"></a><span data-ttu-id="189a2-104">���������� ��������� DLL</span><span class="sxs-lookup"><span data-stu-id="189a2-104">Developing DLLs</span></span>

<span data-ttu-id="189a2-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="189a2-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="189a2-p101">���������� � ��� ���������������� ���, ������� ������������ ������� ������������ ���������� � ������������� ��� ������. ���������� ����� ���� ������� ���������� � �����������, ������ � ��� ���������� LIB � DLL ��������������. ����������� ���������� (��������, ���������� ������� ���������� C) ����������� � ����������� �� ����� ���������� � ���������� ������ ����������� ������������ �����. ���������� ��������� ���������� DLL, ����� ��� ���������� (������ ��� �������). ���� ���������� DLL ����� ��������� ������ ���������� DLL � ����������� ��������� �� ���.</span><span class="sxs-lookup"><span data-stu-id="189a2-p101">A library is a body of compiled code that provides some functionality and data to an executable application. Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively. Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable. The application loads a DLL when it is needed, usually when the application starts up. One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="189a2-111">Преимущества использования библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="189a2-111">Benefits of using DLLs</span></span>

<span data-ttu-id="189a2-112">���� ��������� �������� ������������ ��������� DLL.</span><span class="sxs-lookup"><span data-stu-id="189a2-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="189a2-113">��� ���������� ����� ������������ ���� ����� �� �����.</span><span class="sxs-lookup"><span data-stu-id="189a2-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="189a2-114">����������� ����� ���������� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="189a2-p102">����������� ��������� ������� �������. ������������ ���������� � ��������� DLL ������ ������ ����������� ��������� ��������������� ������. ���� ��������� �������������� � ���������� DLL.</span><span class="sxs-lookup"><span data-stu-id="189a2-p102">They enable large development projects to be broken down. Application and DLL developers only need agree an interface between their respective parts. This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="189a2-118">������������ DLL ����� ��������� ���������� DLL, ����� �������� �� ������������� ��� ��������� ������, �� �������� ��� ������������ �� ����������, ���� ���������������� ��������� ���������� DLL �� ����������.</span><span class="sxs-lookup"><span data-stu-id="189a2-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="189a2-119">� ������� DLL ����� ��������� ������� � ������� � Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="189a2-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="189a2-120">Ресурсы для создания библиотеки DLL</span><span class="sxs-lookup"><span data-stu-id="189a2-120">Resources for creating DLLs</span></span>

<span data-ttu-id="189a2-121">��� ��� �����, ����� ������� ���������� DLL:</span><span class="sxs-lookup"><span data-stu-id="189a2-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="189a2-122">�������� ��������� ����.</span><span class="sxs-lookup"><span data-stu-id="189a2-122">A source code editor.</span></span>
    
- <span data-ttu-id="189a2-123">���������� ��� �������������� ��������� ���� � ���������, ����������� � �������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="189a2-124">����������� ��� ���������� ���� �� ����������� ��������� � �������� ������������ DLL-�����.</span><span class="sxs-lookup"><span data-stu-id="189a2-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="189a2-p103">� ����������� ��������������� ������ ���������� (IDE), �������� Microsoft Visual Studio, ���� ��� ��� ����������, � ����� �����-���������, ����������� ��� ������� ���� � ���������� ����������� ���������, ������� �������� �������� � ������ ������ �����������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p103">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things. They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="189a2-p104">�� ������ ��������� ���������� DLL �� ���������� ������, �������� C/C++, Pascal � Visual Basic. ��� ��� �������� ��� API Excel � C � C++, � ���� ������������ ��������������� ������ ��� ��� �����.</span><span class="sxs-lookup"><span data-stu-id="189a2-p104">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic. Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="189a2-129">Экспорт команды и функции</span><span class="sxs-lookup"><span data-stu-id="189a2-129">Exporting functions and commands</span></span>

<span data-ttu-id="189a2-p105">��� ���������� ������� DLL ���������� � ����������� ������ �����, ����� ������� ��������������, ����� ������������ � ��� ������ � ����������. � ���� ������� ������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p105">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application. This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="189a2-p106">��� ���������� ��������� ���� ����������� ������ �������� ����� �������. ��� ����� ��� ������ ��������� ������� � ������ ��� ����� �����. ���� ������� ���������� ������������� �����. ���������� ���������, ��� ����������, ����������� ���������� DLL, ����� ���������� ��� �������������� �������. ��� ����� ����� ������������� ���� �������� ������������ ����������� ����������� ��� � ����� ������� ������ ��������. ��� ����� ���� ��� �� ��������� ���� ��� ������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p106">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code. They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration. You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL. This can mean telling the linker to associate the decorated name with a simpler export name. The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="189a2-p107">������ ������������� ����� ������� �� ����� � ������� ������ �������, ����������� ������������, �. �. ���������� � �������. ����������� ������������� ���������� � ������� ��� Windows, ������������ � ����������� DLL, � ��� WinAPI. � ������ ���������� Windows ��� ���������� ��� **WINAPI** � ������� ����������� Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="189a2-p107">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention. The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention. It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="189a2-p108">�������, �������������� � DLL-���� ��� Excel (������� �����, �������, ������������� ����� ��������, ��� ���������������� �������) ������ ������ ������������ ���������� � ������� **WINAPI** / **__stdcall**. � ����������� ������� ���������� ���� �������� ��������� **WINAPI**, ��� ��� �� ��������� � ������������ Win32 ������������ ���������� � ������� **__cdecl**, ����� ������������ ��� **WINAPIV**.</span><span class="sxs-lookup"><span data-stu-id="189a2-p108">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention. It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="189a2-142">�� ������ �������� ������������ � ������������� �������� �������, � ����� �� ������� ��� ����������� ���������:</span><span class="sxs-lookup"><span data-stu-id="189a2-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="189a2-143">��������� ������� � DEF-���� ����� ��������� ����� **EXPORTS** � �������� ������ �� ���� ���� � �������� ������� DLL �� ����� ����������.</span><span class="sxs-lookup"><span data-stu-id="189a2-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="189a2-144">����������� ���������� **__declspec(dllexport)** � ����������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="189a2-145">����������� ��������� ������������� **#pragma** ��� �������� ��������� ������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="189a2-146">� ������� ����� ������������ ��� ��� �������, ��� �������������� � ������������, � �������������, �� �� ������� �������������� ���� ������� ����� ��� ����� ��������.</span><span class="sxs-lookup"><span data-stu-id="189a2-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="189a2-147">Например, предположим, что библиотеки DLL содержит два исходного кода модулей, один C и C++ один, содержащие две функции для экспорта, **Мои\_C\_Экспорт** и **Мои\_Cpp\_Экспорт** соответственно.</span><span class="sxs-lookup"><span data-stu-id="189a2-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="189a2-148">��� �������� �����������, ��� ������� ��������� ���� �������� �������� ������� �������� � ���������� ������ ���� �� ����.</span><span class="sxs-lookup"><span data-stu-id="189a2-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="189a2-149">Альтернативы для экспорта каждой функции с помощью каждого из этих методов описанные в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="189a2-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="189a2-150">С помощью DEF-файла</span><span class="sxs-lookup"><span data-stu-id="189a2-150">Using a DEF file</span></span>

```C
double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

```cpp
double WINAPI my_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<br/>

<span data-ttu-id="189a2-151">DEF-���� ������ ��������� ��������� ������.</span><span class="sxs-lookup"><span data-stu-id="189a2-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="189a2-152">���� �������� ����� ��������� ������, ��������� �� ���������� **EXPORTS**.</span><span class="sxs-lookup"><span data-stu-id="189a2-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="189a2-p110">�������� ��������, ��� ������� C ������������, �� � DEF-����� ������������ ���� ���� �������� ������������� ��� �������, ��������� ��� �� ��������� ���� (� ������ �������). ����������� ������ ������������ ������� C++, ��������� ��� ��������� ����, ��� ��� � DEF-���� ������������� �������� ����������� ���.</span><span class="sxs-lookup"><span data-stu-id="189a2-p110">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example). The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="189a2-155">���������� ��� ������� ������� API 32-��������� Windows ��������������� ��������� ������������� ������� C: **function_name** ���������� _ **function_name@** _n_, ���  _n_ � ���������� ������, ���������� � ���� ����������� �����, ������������ ����� �����������, ��� ���� ���������� ������ ��� ������� ����������� �� ���������� �����, �������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="189a2-p111">[!����������] ������ ���� ���������� � Win32 � ������ �����. ��� ������������� �������� �� ������ �� ������������� �����.</span><span class="sxs-lookup"><span data-stu-id="189a2-p111">All pointers are four bytes wide in Win32. The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="189a2-p112">����� ���������� C++ ������������ �������, ��������� ������������� �����, ��������� ������� � �� ��������� �� ������� ���� "C" {�}, ��� �������� � ����������� ���� �������. (�������� ������ **{}** ����� �������, ��� ��� ���������� ��������� ������ � ����� ���� �������, �������������� ��������������� �� ���.)</span><span class="sxs-lookup"><span data-stu-id="189a2-p112">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…} block, as shown in this example. (The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="189a2-161">��� ���������� ���������� ������� C � ������ ����������, ������� ����� ���� �������� � �������� ����� C ��� C++, ���������� �������� ��������� ��������� �������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
```cpp
#ifdef __cplusplus
extern "C" {
#endif
double WINAPI my_C_export(double x);
double WINAPI my_Cdecorated_Cpp_export(double x);
#ifdef __cplusplus
}
#endif
```

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="189a2-162">С помощью оператора объявления __declspec(dllexport)</span><span class="sxs-lookup"><span data-stu-id="189a2-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="189a2-163">�������� ����� **__declspec(dllexport)** ����� ������������ � ���������� ������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="189a2-p113">�������� ����� **__declspec(dllexport)** ���������� �������� � ������� ����� ����� ����������. ������������ ����� �������: ������� �� ����� ��������� � DEF-�����, � ��������� �������� ����������� ������ � ������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p113">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration. The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="189a2-166">���� �� �� ������ ������������ ��� ������� C++, ���������� �������� ������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="189a2-167">����������� ������� ������� ��������� ��� ������ my_undecorated_Cpp_export, �� ���� ������ �� ��������� ����, ��� �������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="189a2-168">С помощью директивы препроцессору компоновщика #pragma</span><span class="sxs-lookup"><span data-stu-id="189a2-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="189a2-p114">��������� ������ Microsoft Visual Studio ������������ ��� ���������������� �������, ������� ��� ������������� � ���������� **#pragma** ��������� ������ �������� ������������ �������������� ������� ��������������� � ���� �������. ������� __FUNCTION__ � __FUNCDNAME__ (�������� �������� �� ��� ������� ������������� � ������ �������) ������������ � ����������������� � ��������������� ������� ������� ��������������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p114">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code. The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="189a2-171">��������, ��� ������������� Microsoft Visual Studio ��� ������ ����� �������� � ����� ���� ���������, ��� �������� ����.</span><span class="sxs-lookup"><span data-stu-id="189a2-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="189a2-172">���� ����� ��������� ������� � �������� �����, ��� �������, ����������� � �������� �������, ����� �������������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="189a2-173">��� C:</span><span class="sxs-lookup"><span data-stu-id="189a2-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="189a2-174">��� C++:</span><span class="sxs-lookup"><span data-stu-id="189a2-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="189a2-p115">�������� ��������, ��� ��������� ���������� ��������� � ��� �������. �� ����� ����������, ������ ���� ��������� **/EP** � **/P** ����������� �� ������. ��� ������������� ����� ������� �������� ������������� � DEF-����� � ���������� **__declspec(dllexport)**, � ������������ ��������� �������� ����������� � ���� �������.</span><span class="sxs-lookup"><span data-stu-id="189a2-p115">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set. This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="189a2-177">��. �����</span><span class="sxs-lookup"><span data-stu-id="189a2-177">See also</span></span>

- [<span data-ttu-id="189a2-178">Доступа к библиотекам DLL в Excel</span><span class="sxs-lookup"><span data-stu-id="189a2-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="189a2-179">����� � Excel �� DLL ��� XLL</span><span class="sxs-lookup"><span data-stu-id="189a2-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="189a2-180">�������� ���������������� � Excel</span><span class="sxs-lookup"><span data-stu-id="189a2-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="189a2-181">���������� XLL-������� ��� Excel 2013</span><span class="sxs-lookup"><span data-stu-id="189a2-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

