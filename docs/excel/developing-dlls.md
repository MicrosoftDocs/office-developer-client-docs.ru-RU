---
title: ���������� ��������� DLL
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
keywords:
- dlls [excel 2007], creating,creating DLLs [Excel 2007]
ms.assetid: 5d69d06d-a126-4c47-82ad-17112674c8a3
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
localization_priority: Priority
ms.openlocfilehash: 89dd7b65ad94ba2fc7e1cf3f99ee163d3003d0fe
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310922"
---
# <a name="developing-dlls"></a><span data-ttu-id="e1314-104">Разработка библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="e1314-104">Developing DLLs</span></span>

<span data-ttu-id="e1314-105">**Область применения**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="e1314-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="e1314-p101">Библиотека — это скомпилированный код, который обеспечивает функции исполняемого приложения и предоставляет ему данные. Библиотеки могут быть связаны статически и динамически, обычно у них расширение LIB и DLL соответственно. Статические библиотеки (например, библиотека времени выполнения C) связываются с приложением во время компиляции и становятся частью полученного исполняемого файла. Приложение загружает библиотеку DLL, когда она необходима (обычно при запуске). Одна библиотека DLL может загружать другую библиотеку DLL и динамически ссылаться на нее.</span><span class="sxs-lookup"><span data-stu-id="e1314-p101">A library is a body of compiled code that provides some functionality and data to an executable application. Libraries can be either statically linked or dynamically linked, and they conventionally have the file name extensions .lib and .dll respectively. Static libraries (such as the C run-time library) are linked to the application at compilation and so become part of the resulting executable. The application loads a DLL when it is needed, usually when the application starts up. One DLL can load and dynamically link to another DLL.</span></span>
  
## <a name="benefits-of-using-dlls"></a><span data-ttu-id="e1314-111">Преимущества библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="e1314-111">Benefits of using DLLs</span></span>

<span data-ttu-id="e1314-112">Ниже приведены основные преимущества библиотек DLL.</span><span class="sxs-lookup"><span data-stu-id="e1314-112">The main benefits of DLLs are as follows:</span></span>
  
- <span data-ttu-id="e1314-113">Все приложения могут использовать одну копию на диске.</span><span class="sxs-lookup"><span data-stu-id="e1314-113">All applications can share a single copy on disk.</span></span>
    
- <span data-ttu-id="e1314-114">����������� ����� ���������� �������� �������.</span><span class="sxs-lookup"><span data-stu-id="e1314-114">Applications' executable files are kept smaller.</span></span>
    
- <span data-ttu-id="e1314-p102">Возможность разбивать большие проекты. Разработчики приложений и библиотек DLL должны только согласовать интерфейс соответствующих частей. Этот интерфейс экспортируется в библиотеке DLL.</span><span class="sxs-lookup"><span data-stu-id="e1314-p102">They enable large development projects to be broken down. Application and DLL developers only need agree an interface between their respective parts. This interface is exported by the DLL.</span></span>
    
- <span data-ttu-id="e1314-118">Разработчики DLL могут обновлять библиотеки DLL, чтобы повысить их эффективность или исправить ошибку, не обновляя все использующие их приложения, если экспортированный интерфейс библиотеки DLL не изменяется.</span><span class="sxs-lookup"><span data-stu-id="e1314-118">DLL developers can update DLLs—perhaps to make them more efficient or to fix a bug—without having to update all the applications that use it, provided that the exported interface of the DLL does not change.</span></span>
    
<span data-ttu-id="e1314-119">С помощью DLL можно добавлять функции и команды в Microsoft Excel.</span><span class="sxs-lookup"><span data-stu-id="e1314-119">You can use DLLs to add worksheet functions and commands in Microsoft Excel.</span></span>
  
## <a name="resources-for-creating-dlls"></a><span data-ttu-id="e1314-120">Ресурсы для создания библиотек DLL</span><span class="sxs-lookup"><span data-stu-id="e1314-120">Resources for creating DLLs</span></span>

<span data-ttu-id="e1314-121">Вот что нужно, чтобы создать библиотеку DLL:</span><span class="sxs-lookup"><span data-stu-id="e1314-121">To create a DLL, you need the following:</span></span>
  
- <span data-ttu-id="e1314-122">Редактор исходного кода.</span><span class="sxs-lookup"><span data-stu-id="e1314-122">A source code editor.</span></span>
    
- <span data-ttu-id="e1314-123">Компилятор для преобразования исходного кода в объектный, совместимый с оборудованием.</span><span class="sxs-lookup"><span data-stu-id="e1314-123">A compiler to turn source code into object code that is compatible with your hardware.</span></span>
    
- <span data-ttu-id="e1314-124">Компоновщик для добавления кода из статических библиотек и создания исполняемого DLL-файла.</span><span class="sxs-lookup"><span data-stu-id="e1314-124">A linker to add code from static libraries, where used, and to create the executable DLL file.</span></span>
    
<span data-ttu-id="e1314-p103">В современных интегрированных средах разработки (IDE), например Microsoft Visual Studio, есть все эти компоненты, а также смарт-редакторы, инструменты для отладки кода и управления несколькими проектами, мастера создания проектов и другие важные инструменты.</span><span class="sxs-lookup"><span data-stu-id="e1314-p103">Modern integrated development environments (IDEs), such as Microsoft Visual Studio, provide all of these things. They also provide a great deal more: smart editors, tools to debug your code, tools to manage multiple projects, new project wizards, and many other important tools.</span></span>
  
<span data-ttu-id="e1314-p104">Вы можете создавать библиотеки DLL на нескольких языках, например C/C++, Pascal и Visual Basic. Так как исходный код API Excel — C и C++, в этой документации рассматриваются только эти два языка.</span><span class="sxs-lookup"><span data-stu-id="e1314-p104">You can create DLLs in several languages, for example, C/C++, Pascal and Visual Basic. Given that the API source code provided with Excel is C and C++, only these two languages are considered in this documentation.</span></span>
  
## <a name="exporting-functions-and-commands"></a><span data-ttu-id="e1314-129">Экспорт функций и команд</span><span class="sxs-lookup"><span data-stu-id="e1314-129">Exporting functions and commands</span></span>

<span data-ttu-id="e1314-p105">При компиляции проекта DLL компилятор и компоновщик должны знать, какие функции экспортировать, чтобы предоставить к ним доступ в приложении. В этом разделе описаны возможные способы.</span><span class="sxs-lookup"><span data-stu-id="e1314-p105">When compiling a DLL project, the compiler and linker need to know what functions are to be exported so that they can make them available to the application. This section describes the ways this can be done.</span></span>
  
<span data-ttu-id="e1314-p106">��� ���������� ��������� ���� ����������� ������ �������� ����� �������. ��� ����� ��� ������ ��������� ������� � ������ ��� ����� �����. ���� ������� ���������� ������������� �����. ���������� ���������, ��� ����������, ����������� ���������� DLL, ����� ���������� ��� �������������� �������. ��� ����� ����� ������������� ���� �������� ������������ ����������� ����������� ��� � ����� ������� ������ ��������. ��� ����� ���� ��� �� ��������� ���� ��� ������.</span><span class="sxs-lookup"><span data-stu-id="e1314-p106">When compilers compile source code, in general, they change the names of the functions from their appearance in the source code. They usually do this by adding to the beginning and/or end of the name, in a process known as name decoration. You need to make sure that the function is exported with a name that is recognizable to the application loading the DLL. This can mean telling the linker to associate the decorated name with a simpler export name. The export name can be the name as it originally appeared in the source code, or something else.</span></span>
  
<span data-ttu-id="e1314-p107">������ ������������� ����� ������� �� ����� � ������� ������ �������, ����������� ������������, �. �. ���������� � �������. ����������� ������������� ���������� � ������� ��� Windows, ������������ � ����������� DLL, � ��� WinAPI. � ������ ���������� Windows ��� ���������� ��� **WINAPI** � ������� ����������� Win32 **__stdcall**.</span><span class="sxs-lookup"><span data-stu-id="e1314-p107">The way the name is decorated depends on the language and how the compiler is instructed to make the function available, that is, the calling convention. The standard inter-process calling convention for Windows used by DLLs is known as the WinAPI convention. It is defined in Windows header files as **WINAPI**, which is in turn defined using the Win32 declarator **__stdcall**.</span></span>
  
<span data-ttu-id="e1314-p108">�������, �������������� � DLL-���� ��� Excel (������� �����, �������, ������������� ����� ��������, ��� ���������������� �������) ������ ������ ������������ ���������� � ������� **WINAPI** / **__stdcall**. � ����������� ������� ���������� ���� �������� ��������� **WINAPI**, ��� ��� �� ��������� � ������������ Win32 ������������ ���������� � ������� **__cdecl**, ����� ������������ ��� **WINAPIV**.</span><span class="sxs-lookup"><span data-stu-id="e1314-p108">A DLL-export function for use with Excel (whether it is a worksheet function, macro-sheet equivalent function, or user-defined command) should always use the **WINAPI** / **__stdcall** calling convention. It is necessary to include the **WINAPI** specifier explicitly in the function's definition as the default in Win32 compilers is to use the **__cdecl** calling convention, also defined as **WINAPIV**, if none is specified.</span></span>
  
<span data-ttu-id="e1314-142">Вы можете сообщить компоновщику о необходимости экспорта функции, а также ее внешнее имя несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="e1314-142">You can tell the linker that a function is to be exported, and the name it is to be known by externally in one of several ways:</span></span>
  
- <span data-ttu-id="e1314-143">��������� ������� � DEF-���� ����� ��������� ����� **EXPORTS** � �������� ������ �� ���� ���� � �������� ������� DLL �� ����� ����������.</span><span class="sxs-lookup"><span data-stu-id="e1314-143">Place the function in a DEF file after the **EXPORTS** keyword, and set your DLL project setting to reference this file when linking.</span></span> 
    
- <span data-ttu-id="e1314-144">����������� ���������� **__declspec(dllexport)** � ����������� �������.</span><span class="sxs-lookup"><span data-stu-id="e1314-144">Use the **__declspec(dllexport)** declarator in the function's definition.</span></span> 
    
- <span data-ttu-id="e1314-145">����������� ��������� ������������� **#pragma** ��� �������� ��������� ������������.</span><span class="sxs-lookup"><span data-stu-id="e1314-145">Use a **#pragma** preprocessor directive to send a message to the linker.</span></span> 
    
<span data-ttu-id="e1314-146">В проекте можно использовать все три способа, они поддерживаются и компилятором, и компоновщиком, но не следует экспортировать одну функцию более чем одним способом.</span><span class="sxs-lookup"><span data-stu-id="e1314-146">Although your project can use all three methods and your compiler and linker support them, you should not try to export one function in more than one of these ways.</span></span> <span data-ttu-id="e1314-147">Например, предположим, что библиотека DLL содержит два модуля исходного кода, C и C++, которые содержат две функции для экспорта — **my\_C\_export** и **my\_Cpp\_export** соответственно.</span><span class="sxs-lookup"><span data-stu-id="e1314-147">For example, suppose that a DLL contains two source code modules, one C and one C++, which contain two functions to be exported, **my\_C\_export** and **my\_Cpp\_export** respectively.</span></span> <span data-ttu-id="e1314-148">Для простоты предположим, что функции принимают один числовой аргумент двойной точности и возвращают данные того же типа.</span><span class="sxs-lookup"><span data-stu-id="e1314-148">For simplicity, suppose that each function takes a single double-precision numerical argument and returns the same data type.</span></span> <span data-ttu-id="e1314-149">В следующих разделах описываются варианты экспорта функций с помощью каждого из этих методов.</span><span class="sxs-lookup"><span data-stu-id="e1314-149">The alternatives for exporting each function by using each of these methods are outlined in the following sections.</span></span> 
  
### <a name="using-a-def-file"></a><span data-ttu-id="e1314-150">С помощью DEF-файла</span><span class="sxs-lookup"><span data-stu-id="e1314-150">Using a DEF file</span></span>

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

<span data-ttu-id="e1314-151">DEF-файл должен содержать следующие строки.</span><span class="sxs-lookup"><span data-stu-id="e1314-151">The DEF file would then need to contain these lines.</span></span>
  
`EXPORTS my_C_export = _my_C_export@8  my_Cpp_export`

<br/>

<span data-ttu-id="e1314-152">���� �������� ����� ��������� ������, ��������� �� ���������� **EXPORTS**.</span><span class="sxs-lookup"><span data-stu-id="e1314-152">The general syntax of a line that follows an **EXPORTS** statement is as follows.</span></span> 
  
`entryname[=internalname] [@ordinal[NONAME]] [DATA] [PRIVATE]`

<span data-ttu-id="e1314-p110">Обратите внимание, что функция C декорирована, но в DEF-файле компоновщику явно дано указание предоставлять эту функцию, используя имя из исходного кода (в данном примере). Компоновщик неявно экспортирует функцию C++, используя имя исходного кода, так что в DEF-файл необязательно включать расширенное имя.</span><span class="sxs-lookup"><span data-stu-id="e1314-p110">Note that the C function has been decorated, but the DEF file explicitly forces the linker to expose the function using the original source code name (in this example). The linker implicitly exports the C++ function using the original code name, so that it is not necessary to include the decorated name in the DEF file.</span></span>
  
<span data-ttu-id="e1314-155">���������� ��� ������� ������� API 32-��������� Windows ��������������� ��������� ������������� ������� C: **function_name** ���������� _ **function_name@** _n_, ���  _n_ � ���������� ������, ���������� � ���� ����������� �����, ������������ ����� �����������, ��� ���� ���������� ������ ��� ������� ����������� �� ���������� �����, �������� �������.</span><span class="sxs-lookup"><span data-stu-id="e1314-155">For 32-bit Windows API function calls, the convention for the decoration of C-compiled functions is as follows: **function_name** becomes _ **function_name@** _n_ where  _n_ is the number of bytes expressed as a decimal taken up by all the arguments, with the bytes for each rounded up to the nearest multiple of four.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e1314-p111">Размер всех указателей в Win32 — четыре байта. Тип возвращаемого значения не влияет на декорирование имени.</span><span class="sxs-lookup"><span data-stu-id="e1314-p111">All pointers are four bytes wide in Win32. The return type has no impact on name decoration.</span></span> 
  
<span data-ttu-id="e1314-p112">����� ���������� C++ ������������ �������, ��������� ������������� �����, ��������� ������� � �� ��������� �� ������� ���� "C" {�}, ��� �������� � ����������� ���� �������. (�������� ������ **{}** ����� �������, ��� ��� ���������� ��������� ������ � ����� ���� �������, �������������� ��������������� �� ���.)</span><span class="sxs-lookup"><span data-stu-id="e1314-p112">It is possible to force the C++ compiler to expose undecorated names for C++ functions by enclosing the function, and any function prototypes, within an extern "C" {…} block, as shown in this example. (The braces **{}** are omitted here because the declaration only refers to the function code block that immediately follows it).</span></span> 
  
```cpp
extern "C"
double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}

```

<span data-ttu-id="e1314-161">При размещении прототипов функции C в файлах заголовков, которые могут быть включены в исходные файлы C или C++, необходимо включить следующую директиву препроцессора.</span><span class="sxs-lookup"><span data-stu-id="e1314-161">When you are placing C function prototypes in header files that could be included in C or C++ source files, you should include the following pre-processor directive.</span></span>
  
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

### <a name="using-the-declspecdllexport-declarator"></a><span data-ttu-id="e1314-162">С помощью декларатора __declspec(dllexport)</span><span class="sxs-lookup"><span data-stu-id="e1314-162">Using the __declspec(dllexport) declarator</span></span>

<span data-ttu-id="e1314-163">Ключевое слово **__declspec(dllexport)** можно использовать в объявлении функции указанным ниже образом.</span><span class="sxs-lookup"><span data-stu-id="e1314-163">The **__declspec(dllexport)** keyword can be used in the declaration of the function as follows.</span></span> 
  
```cpp
__declspec(dllexport) double WINAPI my_C_export(double x)
{
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="e1314-p113">�������� ����� **__declspec(dllexport)** ���������� �������� � ������� ����� ����� ����������. ������������ ����� �������: ������� �� ����� ��������� � DEF-�����, � ��������� �������� ����������� ������ � ������������.</span><span class="sxs-lookup"><span data-stu-id="e1314-p113">The **__declspec(dllexport)** keyword must be added at the extreme left of the declaration. The advantages of this approach are that the function does not need to be listed in a DEF file, and that the export status is right with the definition.</span></span> 
  
<span data-ttu-id="e1314-166">Если вы не хотите декорировать имя функции C++, необходимо объявить функцию следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e1314-166">If you want to avoid a C++ function being made available with the C++ name decoration, you must declare the function as follows.</span></span>
  
```cpp
extern "C"
__declspec(dllexport) double WINAPI my_undecorated_Cpp_export(double x)
{
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="e1314-167">Компоновщик сделает функцию доступной под именем my_undecorated_Cpp_export, то есть именем из исходного кода, без декорирования.</span><span class="sxs-lookup"><span data-stu-id="e1314-167">The linker will make the function available as my_undecorated_Cpp_export, that is, the name as it appears in the source code with no decoration.</span></span>
  
### <a name="using-a-pragma-preprocessor-linker-directive"></a><span data-ttu-id="e1314-168">С помощью директивы компоновщика препроцессора #pragma</span><span class="sxs-lookup"><span data-stu-id="e1314-168">Using a #pragma preprocessor linker directive</span></span>

<span data-ttu-id="e1314-p114">Последние версии Microsoft Visual Studio поддерживают два предопределенных макроса, которые при использовании с директивой **#pragma** позволяют давать указание компоновщику экспортировать функции непосредственно в коде функции. Макросы __FUNCTION__ и __FUNCDNAME__ (обратите внимание на два символа подчеркивания с каждой стороны) используются с недекорированными и декорированными именами функций соответственно.</span><span class="sxs-lookup"><span data-stu-id="e1314-p114">Recent versions of Microsoft Visual Studio support two predefined macros that, when used in conjunction with a **#pragma** directive, enable you to instruct the linker to export the function directly from within the function code. The macros are __FUNCTION__ and __FUNCDNAME__ (note the double underline at each end) which are expanded to the undecorated and decorated function names respectively.</span></span> 
  
<span data-ttu-id="e1314-171">Например, при использовании Microsoft Visual Studio эти строки можно включить в общий файл заголовка, как показано ниже.</span><span class="sxs-lookup"><span data-stu-id="e1314-171">For example, when you are using Microsoft Visual Studio, these lines can be incorporated into a common header file as follows.</span></span>
  
```cpp
#if _MSC_VER > 1200 // Later than Visual Studio 6.0
#define EXPORT comment(linker, "/EXPORT:"__FUNCTION__"="__FUNCDNAME__)
#else // Cannot use this way of exporting functions.
#define EXPORT
#endif // else need to use DEF file or __declspec(dllexport)

```

<span data-ttu-id="e1314-172">Если такой заголовок включен в исходные файлы, две функции, приведенные в качестве примера, можно экспортировать следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e1314-172">If this header is included in the source files, the two example functions can then be exported as follows.</span></span>
  
<span data-ttu-id="e1314-173">Код C:</span><span class="sxs-lookup"><span data-stu-id="e1314-173">C code:</span></span>
  
```C
double WINAPI my_C_export(double x)
{
#pragma EXPORT
/* Modify x and return it. */
    return x * 2.0;
}
```

<span data-ttu-id="e1314-174">Код C++:</span><span class="sxs-lookup"><span data-stu-id="e1314-174">C++ code:</span></span>
  
```cpp
double WINAPI my_Cpp_export(double x)
{
#pragma EXPORT
// Modify x and return it.
    return x * 2.0;
}
```

<span data-ttu-id="e1314-p115">Обратите внимание, что директиву необходимо поместить в код функции. Ее можно развернуть, только если параметры **/EP** и **/P** компилятора не заданы. При использовании этого способа исчезает необходимость в DEF-файле и объявлении **__declspec(dllexport)**, а спецификация состояния экспорта указывается в коде функции.</span><span class="sxs-lookup"><span data-stu-id="e1314-p115">Note that the directive must be placed within the body of the function and is only expanded when neither of the compiler options **/EP** or **/P** is set. This technique removes the need for a DEF file, or **__declspec(dllexport)** declaration, and keeps the specification of its export status with the function code.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e1314-177">См. также</span><span class="sxs-lookup"><span data-stu-id="e1314-177">See also</span></span>

- [<span data-ttu-id="e1314-178">Доступ к библиотекам DLL в Excel</span><span class="sxs-lookup"><span data-stu-id="e1314-178">Access DLLs in Excel</span></span>](how-to-access-dlls-in-excel.md)
- [<span data-ttu-id="e1314-179">Вызов Excel из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="e1314-179">Calling into Excel from the DLL or XLL</span></span>](calling-into-excel-from-the-dll-or-xll.md)
- [<span data-ttu-id="e1314-180">Понятия, связанные с программированием, для Excel</span><span class="sxs-lookup"><span data-stu-id="e1314-180">Excel Programming Concepts</span></span>](excel-programming-concepts.md)
- [<span data-ttu-id="e1314-181">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="e1314-181">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

