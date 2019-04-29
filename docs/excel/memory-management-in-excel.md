---
title: ���������� ������� � Excel
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
keywords:
- xloper12 memory [excel 2007],managing memory in Excel,Excel stack,strings [Excel 2007], managing memory,memory management in Excel,XLOPER memory [Excel 2007],memory [Excel 2007], management guidelines
localization_priority: Normal
ms.assetid: 3bf5195b-6235-43cf-8795-0c7b0a63a095
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f129dac2971f01c8ada15f0028958132b1945746
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419543"
---
# <a name="memory-management-in-excel"></a><span data-ttu-id="a8dfe-104">Управление памятью в Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-104">Memory Management in Excel</span></span>

 <span data-ttu-id="a8dfe-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="a8dfe-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="a8dfe-p101">���� �� ������ ��������� ����������� � ���������� XLL-����������, ������� �������� ������� ���������� �������. ������������ ���������� ������� ����� �������� � ������ ���� ������� � Microsoft Excel � �� ��������������, ����� ��� ��������� ������ ������ ��� �� ������������� ������������� � �������������, �� ���������, ����� ��� �������������� Excel.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p101">Memory management is the most important concern if you want to create efficient and stable XLLs. Failure to manage memory well can lead to a range of problems in Microsoft Excel—from minor problems such as inefficient memory allocation and initialization and small memory leaks, to major problems such as the destabilization of Excel.</span></span>
  
<span data-ttu-id="a8dfe-p102">������������ ���������� ������� � �������� ���������������� ������� ��������� �������, ��������� � ������������. �������������, ���������� ������ ������ ��� ������� ������ ����������� � ���������������� ��������� ���������� �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p102">Mismanagement of memory is the most common source of serious add-in-related problems. Therefore, you should build your project with a consistent and well-thought-through strategy on memory management.</span></span> 
  
<span data-ttu-id="a8dfe-p103">� ���������� �������������� ��������� ���� � Microsoft Office Excel 2007 ��������� ������� ����� �������. ���� �� ������ ��������� � �������������� ���������������� ������� ������, ���������� ��������� ���������, ������� ����� ��������� ��� ����������� ���������� ������� �� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p103">Memory management became more complex in Microsoft Office Excel 2007 with the introduction of multithreaded workbook recalculation. If you want to create and export thread-safe worksheet functions, you must manage the resulting conflicts that can occur when multiple threads compete for access.</span></span>
  
<span data-ttu-id="a8dfe-112">���� ��������� ������������ ��� ��������� ���� ����� ��������� ������:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-112">There are memory considerations for the following three data structure types:</span></span>
  
- <span data-ttu-id="a8dfe-113">**XLOPER** � **XLOPER12**;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-113">**XLOPER**s and **XLOPER12**s</span></span>
    
- <span data-ttu-id="a8dfe-114">�����, ��������� ������� ���������� �� **XLOPER** ��� **XLOPER12**;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-114">Strings that are not in an **XLOPER** or **XLOPER12**</span></span>
    
- <span data-ttu-id="a8dfe-115">�������� **FP** � **FP12**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-115">**FP** and **FP12** arrays</span></span> 
    
## <a name="xloperxloper12-memory"></a><span data-ttu-id="a8dfe-116">Память XLOPER и XLOPER12</span><span class="sxs-lookup"><span data-stu-id="a8dfe-116">XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="a8dfe-117">Структура данных **XLOPER**/ **XLOPER12** содержит несколько подтипов, которые содержат указатели на блоки памяти, а именно строки (**кслтипестр**), массивы (**xltypeMulti**) и внешние ссылки (**кслтипереф**).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-117">The **XLOPER**/ **XLOPER12** data structure has a few sub-types that contain pointers to blocks of memory, namely strings (**xltypeStr**), arrays (**xltypeMulti**) and external references (**xltypeRef**).</span></span> <span data-ttu-id="a8dfe-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-118">Note also that **xltypeMulti** arrays can contain string **XLOPER**/ **XLOPER12s** that in turn point to other blocks of memory.</span></span> 
  
<span data-ttu-id="a8dfe-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-119">An **XLOPER**/ **XLOPER12** can be created in several ways:</span></span> 
  
- <span data-ttu-id="a8dfe-120">� Excel ��� ���������� ���������� ��� �������� � ������� XLL;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-120">By Excel when preparing arguments to be passed to an XLL function</span></span>
    
- <span data-ttu-id="a8dfe-121">� Excel ��� ����������� **XLOPER** ��� **XLOPER12** �� ����� ������ API C;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-121">By Excel when returning an **XLOPER** or **XLOPER12** in a C API call</span></span> 
    
- <span data-ttu-id="a8dfe-122">� DLL ��� �������� ���������� ��� �������� �� ����� ������ API C;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-122">By your DLL when creating arguments to be passed to a C API call</span></span>
    
- <span data-ttu-id="a8dfe-123">в DLL при создании возвращаемого значения функции XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-123">By your DLL when creating an XLL function return value</span></span>
    
<span data-ttu-id="a8dfe-124">Блок памяти, принадлежащий к типу указателей на память, можно выделить под что-то несколькими способами:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-124">A block of memory within one of the memory-pointing types can be allocated in several ways:</span></span>
  
- <span data-ttu-id="a8dfe-125">как статический блок в библиотеке DLL за пределами кода функции (в этом случае необязательно выделять или освобождать память);</span><span class="sxs-lookup"><span data-stu-id="a8dfe-125">It can be a static block within your DLL outside any function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="a8dfe-126">��� ����������� ���� � ���������� DLL, �������� � ��� ������� (� ���� ������ ������������� �������� ��� ����������� ������);</span><span class="sxs-lookup"><span data-stu-id="a8dfe-126">It can be a static block within your DLL within some function code, in which case you do not have to allocate or free the memory.</span></span>
    
- <span data-ttu-id="a8dfe-127">� ������� ������������� ��������� � ������������ � ���������� DLL ( **malloc** � **free**, **new** � **delete** � �. �.);</span><span class="sxs-lookup"><span data-stu-id="a8dfe-127">It can be dynamically allocated and freed by your DLL in several possible ways: **malloc** and **free**, **new** and **delete**, and so on.</span></span>
    
- <span data-ttu-id="a8dfe-128">� ������� ������������� ��������� � Excel.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-128">It can be dynamically allocated by Excel.</span></span>
    
<span data-ttu-id="a8dfe-p105">�������� ����� ��������� ���������� ������ **XLOPER**/ **XLOPER12** � ���������� ��������, � ������� ���������� ������ **XLOPER**/ **XLOPER12** ���������� ��� ������, �������������, ��� ��� ���� ����� ���� ����� �������. ��� �� �����, ���� ��������� ���������� �������� � �������������, �� ����� ����������� ���������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p105">Given the number of possible origins for **XLOPER**/ **XLOPER12** memory and the number of situations in which the **XLOPER**/ **XLOPER12** might have had that memory assigned, it is not surprising that this subject can seem very difficult. However, the complexity can be greatly reduced if you follow several rules and guidelines.</span></span> 
  
### <a name="rules-for-working-with-xloperxloper12"></a><span data-ttu-id="a8dfe-131">Правила работы с XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="a8dfe-131">Rules for Working with XLOPER/XLOPER12</span></span>

- <span data-ttu-id="a8dfe-p106">�� ��������� ���������� ������ ��� ������������ ��������� ������ **XLOPERs**/ **XLOPER12**, ������� ���������� ��� ��������� � ������� XLL. ��� ��������� ������������� ������ ��� ������. �������������� �������� ��. � ������� "����������� **XLOPER** ��� **XLOPER12** � ������� ��������� ���������� �� �����" ������ [��������� ��������, ����������� ��� ���������� XLL ��� Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p106">Do not try to free memory or overwrite **XLOPERs**/ **XLOPER12**s that are passed as arguments to your XLL function. You should treat such arguments as read-only. For more information, see "Returning **XLOPER** or **XLOPER12** by Modifying Arguments in Place" in [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
    
- <span data-ttu-id="a8dfe-135">���� ���������� Excel �������� ������ ��������� ������ **XLOPER**/ **XLOPER12**, ������������ � DLL �� ����� ������ API C:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-135">If Excel has allocated memory for an **XLOPER**/ **XLOPER12** returned to your DLL in a call to the C API:</span></span> 
    
  - <span data-ttu-id="a8dfe-p107">���������� ���������� ������, ����� ��� ������ �� ��������� **XLOPER**/ **XLOPER12**, � ������� ������ [xlFree](xlfree.md). �� ����������� ��� ����� ������ �����, �������� free ��� delete.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p107">You must free the memory when you no longer need the **XLOPER**/ **XLOPER12** using a call to [xlFree](xlfree.md). Do not use any other method, such as free or delete, to release the memory.</span></span>
    
  - <span data-ttu-id="a8dfe-138">���� ������������ ��� � **xltypeMulti**, �� ��������������� **XLOPER**/ **XLOPER12** � �������, �������� ���� ��� �������� ������ ��� �� �������� ��������� ���������� � ������� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-138">If the returned type is **xltypeMulti**, do not overwrite any **XLOPER**/ **XLOPER12**s within the array, especially if they contain strings, and especially not where you are trying to overwrite with a string.</span></span>
    
  - <span data-ttu-id="a8dfe-139">����� ���������� � Excel **XLOPER**/ **XLOPER12** ��� ������������ �������� ������� DLL, ���������� �������� Excel � ������, ������� ���������� ���������� ����� ���������� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-139">If you want to return the **XLOPER**/ **XLOPER12** to Excel as your DLL function's return value, you must tell Excel that there is memory that Excel must release when done.</span></span> 
    
- <span data-ttu-id="a8dfe-140">������� **xlFree** ���������� �������� ������ ��� ��������� ������ **XLOPER**/ **XLOPER12**, ��������� � �������� ������������� �������� ��� ������ API C.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-140">You must only call **xlFree** on an **XLOPER**/ **XLOPER12** that was created as the return value to a C API call.</span></span> 
    
- <span data-ttu-id="a8dfe-141">���� ���������� DLL �������� ������ ��������� ������ **XLOPER**/ **XLOPER12**, ������� ����� ���������� � Excel � �������� ������������� �������� ������� DLL, ���������� �������� Excel � ������, ������� ���������� DLL ������ ����������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-141">If your DLL has allocated memory for an **XLOPER**/ **XLOPER12** that you want to return to Excel as your DLL function's return value, you must tell Excel that there is memory that the DLL must release.</span></span> 
    
### <a name="guidelines-for-memory-management"></a><span data-ttu-id="a8dfe-142">Рекомендации по управлению памятью</span><span class="sxs-lookup"><span data-stu-id="a8dfe-142">Guidelines for Memory Management</span></span>

- <span data-ttu-id="a8dfe-p108">Используйте определенный метод для выделения и освобождения памяти в библиотеке DLL. Не смешивайте методы. Рекомендуем использовать нужный метод как структуру или класс памяти, где его можно изменять, не изменяя код в других местах.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p108">Be consistent in your DLL in the method that you use to allocate and release memory. Avoid mixing methods. A good approach is to wrap the method that you are using up in a memory class or structure, within which you can change the method used without altering your code in many places.</span></span>
    
- <span data-ttu-id="a8dfe-p109">��� �������� �������� **xltypeMulti** � ���������� DLL ��������� ������ ��� ����� ������������ ��������: ������ ��������� ������ ����������� ��� ������ ����������� ����������� ������. � ���� ������, ���������� ������, �� ������ �����, ��� ���������� ������ ����������� ������ ��� ������� ����� �� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p109">When you create **xltypeMulti** arrays within your DLL, be consistent in the way that you allocate memory for strings: always dynamically allocate the memory for them or always use static memory. If you do this, when you are freeing the memory, you will know that you must either always or never free the strings.</span></span> 
    
- <span data-ttu-id="a8dfe-148">���������� �������� ����� ���������� Excel ������ ��� ����������� ��������� � ������� Excel ��������� ������ **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-148">Make deep copies of Excel-allocated memory when you are copying an Excel-created **XLOPER**/ **XLOPER12**.</span></span>
    
- <span data-ttu-id="a8dfe-p110">�� ��������� ���������� Excel ������ **XLOPER**/ **XLOPER12** � ������� **xltypeMulti**. ���������� �������� ����� ����� � ������� ��������� �� ��� ����� � �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p110">Do not put Excel-allocated string **XLOPER**/ **XLOPER12**s within **xltypeMulti** arrays. Make deep copies of the strings and store pointers to the copies in the array.</span></span> 
    
## <a name="freeing-excel-allocated-xloperxloper12-memory"></a><span data-ttu-id="a8dfe-151">Освобождение выделенной Excel памяти XLOPER/XLOPER12</span><span class="sxs-lookup"><span data-stu-id="a8dfe-151">Freeing Excel-Allocated XLOPER/XLOPER12 Memory</span></span>

<span data-ttu-id="a8dfe-152">� ��������� ������� XLL ������������ ������� **xlGetName** ��� ��������� ������, ���������� ��� DLL-����� � ���� � ����, � ������� **xlcAlert** ��� �� ����������� � ���������� ���� ����������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-152">Consider the following XLL command, which uses **xlGetName** to obtain a string containing the path and file name of the DLL and displays it in an alert dialog box using **xlcAlert**.</span></span>
  
```cs
int WINAPI show_DLL_name(void)
{
    XLOPER12 xDllName;
    if(Excel12(xlfGetName, &xDllName, 0) == xlretSuccess)
    {
        // Display the name.
        Excel12(xlcAlert, 0, 1, &xDllName);
        // Free the memory that Excel allocated for the string.
        Excel12(xlFree, 0, 1, &xDllName);
    }
    return 1;
}

```

<span data-ttu-id="a8dfe-153">����� ������� ������ �� ����� ������, �� ������� ��������� **xDllName**, ��� ����� ���������� ��, ��������� ����� [������� xlFree](xlfree.md), ����� �� ������� API C ������ ��� ��������� DLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-153">When the function no longer needs the memory pointed to by **xDllName**, it can free it using a call to the [xlFree function](xlfree.md), one of the DLL-only C API functions.</span></span> 
  
<span data-ttu-id="a8dfe-154">������� **xlFree** �������� ������� � ����������� �� �������� (��. ������ [������� ���������� API ��� C, ������� ����� ���������� ������ �� DLL ��� XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), �� �������� �������� �� ���������:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-154">The **xlFree** function is fully documented in the function reference section (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), but be aware of the following:</span></span>
  
- <span data-ttu-id="a8dfe-155">�� ������ ���������� ��������� ���������� ���������� ������ **XLOPER**/ **XLOPER12** �� ����� ������ ������ ������� **xlFree**. ������������ ����������� ��� ���� � ���������� ���������� �������, ������� �������������� � ������������ ������ Excel (30 � Excel 2003, 255 � Excel�2007 � ����� ������� ������).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-155">You can pass pointers to more than one **XLOPER**/ **XLOPER12**s in a single call to **xlFree**, limited only by the number of function arguments supported in the running version of Excel (30 in Excel 2003, 255 starting in Excel 2007).</span></span>
    
- <span data-ttu-id="a8dfe-p111">������� **xlFree** ������������� ��� ������������� ��������� �������� **NULL**, ����� ���������� ������������ ��� ������� ������������ ��� ������������� ��������� ������ **XLOPER**/ **XLOPER12**. **xlFree** � ��� ������������ ������� API C, ������� �������� ���� ���������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p111">**xlFree** sets the contained pointer to **NULL** to ensure that an attempt to free an **XLOPER**/ **XLOPER12** that has already been freed is safe. **xlFree** is the only C API function that modifies its arguments.</span></span> 
    
- <span data-ttu-id="a8dfe-158">�� ������ ��������� �������� **xlFree** ��� ����� ��������� ������ **XLOPER**/ **XLOPER12**, ������� ������������ ��� ��������� ������������� �������� ��� ������ API C, ���������� �� ������� � ��� ��������� �� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-158">You can safely call **xlFree** on any **XLOPER**/ **XLOPER12** used for the return value of a call to the C API, regardless of whether it contains a pointer to memory.</span></span> 
    
## <a name="returning-xloperxloper12s-to-be-freed-by-excel"></a><span data-ttu-id="a8dfe-159">Возвращение структур данных XLOPER или XLOPER12 для освобождения в Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-159">Returning XLOPER/XLOPER12s to be freed by Excel</span></span>

<span data-ttu-id="a8dfe-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p112">Suppose you wanted to modify the example command in the previous section and change it to a worksheet function that returns the DLL path and file name when passed a **Boolean** **true** argument, and **#N/A** otherwise. Clearly you cannot call **xlFree** to release the string memory before returning it to Excel. However, if it is not freed at some point, the add-in will leak memory every time the function is called. To work around this problem, you can set a bit in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitXLFree** in xlcall.h. Setting this tells Excel that it must free the returned memory when it has finished copying the value out.</span></span> 
  
### <a name="example"></a><span data-ttu-id="a8dfe-165">Пример</span><span class="sxs-lookup"><span data-stu-id="a8dfe-165">Example</span></span>

<span data-ttu-id="a8dfe-166">В следующем примере кода показано преобразование команды XLL из предыдущего раздела в функцию листа XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-166">The following code example shows the XLL command in the previous section converted into an XLL worksheet function.</span></span>
  
```cs
LPXLOPER12 WINAPI get_DLL_name(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype == xltypeStr)
    {
// Tell Excel to free the string memory after
// it has copied out the return value.
        xRtnValue.xltype |= xlbitXLFree;
    }
    return &xRtnValue;
}
```

<span data-ttu-id="a8dfe-p113">������� XLL, ������� ���������� **XLOPER**/ **XLOPER12**, ���������� �������� ��� �����, ������� ��������� � ���������� ��������� �� **XLOPER**/ **XLOPER12**. ������������� � ���� ������� ����������� ������ **XLOPER12** � ������� �� ���������������. �� ������ ����������� ���������������� ��� ������� ��� ����������������, �� ���������� ���� ���������� �������� **xRtnValue** ����� ������� �� ���������� ������ � ��� ������� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p113">XLL functions that use **XLOPER**/ **XLOPER12**s must be declared as taking and returning pointers to **XLOPER**/ **XLOPER12**s. The use in this example of a static **XLOPER12** within the function is not thread safe. You could incorrectly register this function as thread safe, but you would risk **xRtnValue** being overwritten by one thread before another thread had finished with it.</span></span> 
  
<span data-ttu-id="a8dfe-p114">�������� **xlbitXLFree** ���������� �������� ����� ������ ������� ��������� ������ Excel, ������� ��� ��������. ���� ������ ��� �� �����, ��� ����� ������������ � �� ���� ������� �������. ���� �� ������ ������������ ��� �������� � �������� ��������� �� ����� ������ ������ ������� API C �� ��� ����������� �� ����, ��� �������� ������� �������� ����� ������ ������. � ��������� ������ �� ����������� �������, ������� �� ��������� ��� �������� �� �������� ���� **XLOPER**/ **XLLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p114">You must set **xlbitXLFree** after the call to the Excel callback that allocates it. If you set it before this, it is overwritten and does not have the effect that you want. If you intend to use the value as an argument in a call to another C API function before returning it to the worksheet, you should set this bit after any such call. Otherwise, you will confuse functions that do not mask this bit before checking the **XLOPER**/ **XLLOPER12** type.</span></span> 
  
## <a name="returning-xloperxloper12s-to-be-freed-by-the-dll"></a><span data-ttu-id="a8dfe-174">Возвращение структур данных XLOPER или XLOPER12 для освобождения в библиотеке DLL</span><span class="sxs-lookup"><span data-stu-id="a8dfe-174">Returning XLOPER/XLOPER12s to be freed by the DLL</span></span>

<span data-ttu-id="a8dfe-p115">����������� �������� ���������, ����� ���������� XLL �������� ������ **XLOPER**/ **XLOPER12** � ����� ���������� �� � Excel. Excel ���������� ��� ���� ��������, ������� ����� ������ � ���� **xltype** ��������� ������ **XLOPER**/ **XLOPER12**, � **xlbitDLLFree** � xlcall.h.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p115">A similar problem to this occurs when your XLL has allocated memory for an **XLOPER**/ **XLOPER12** and wants to return it to Excel. Excel recognizes another bit that can be set in the **xltype** field of the **XLOPER**/ **XLOPER12**, defined as **xlbitDLLFree** in xlcall.h.</span></span> 
  
<span data-ttu-id="a8dfe-p116">������� **an XLOPER**/ **XLOPER12** � ���� ���������, Excel �������� ������� ������� [xlAutoFree](xlautofree-xlautofree12.md) (��� **XLOPER**) ��� **xlAutoFree12** (��� **XLOPER12**), ������� ������ �������������� ���������� XLL. ��� ������� ����� �������� ������� � ����������� �� �������� (��. ������ [��������� ��������� � ������� XLL ����������](add-in-manager-and-xll-interface-functions.md)), �� ������ ����������� ���������� �������� �����. ��� ������������� ��� ������������ ������ **XLOPER**/ **XLOPER12** ��� �� ��������, ������� ��� ���������� ��������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p116">When Excel receives **an XLOPER**/ **XLOPER12** with this bit set, it tries to call a function that should be exported by the XLL called [xlAutoFree](xlautofree-xlautofree12.md) (for **XLOPER**s) or **xlAutoFree12** (for **XLOPER12**s). This function is described more fully in the function reference (see [Add-in Manager and XLL Interface Functions](add-in-manager-and-xll-interface-functions.md)), but an example minimal implementation is given here. Its purpose is to free the **XLOPER**/ **XLOPER12** memory in a way that is consistent with how it was originally allocated.</span></span> 
  
### <a name="examples"></a><span data-ttu-id="a8dfe-180">Примеры</span><span class="sxs-lookup"><span data-stu-id="a8dfe-180">Examples</span></span>

<span data-ttu-id="a8dfe-181">�������� ������� � ��������� ������� ���������� �������� ���������� ������� (�� ����������� ����, ��� ��� �������� ����� "The full pathname for this DLL is" ����� ������ DLL).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-181">The following example function does the same as the previous function except that it includes the text "The full pathname for this DLL is " before the DLL name.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_2(int calculation_trigger)
{
    static XLOPER12 xRtnValue; // Not thread-safe
    Excel12(xlfGetName, &xRtnValue, 0);
// If xlfGetName failed, xRtnValue will be #VALUE!
    if(xRtnValue.xltype != xltypeStr)
        return &xRtnValue;
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = xRtnValue.val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, xRtnValue.val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, &xRtnValue);
// Now reuse the XLOPER12 for the new string.
    xRtnValue.val.str = msg_text;
// Tell Excel to call back into the DLL to free the string
// memory after it has copied out the return value.
    xRtnValue.xltype     = xltypeStr | xlbitDLLFree;
    return &xRtnValue;
}
```

<span data-ttu-id="a8dfe-182">����������� ���������� ������� **xlAutoFree12** � ���������� XLL, ���������������� ���������� �������, �������� ��������� �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-182">A minimally sufficient implementation of **xlAutoFree12** in the XLL that exported the previous function would be as follows.</span></span> 
  
```cs
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
}
```

<span data-ttu-id="a8dfe-p117">���� ���������� ����������, ������ ���� ���������� XLL ���������� ������ **XLOPER12** � ��� ���������� � ������� ������� **malloc**. �������� ��������, ��� � ���� ������ ����</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p117">This implementation is only sufficient if the XLL only returns **XLOPER12** strings, and those strings are only allocated using **malloc**. Note that the test</span></span> 
  
 ` if(p_oper->xltype == xltypeStr) `
  
<span data-ttu-id="a8dfe-185">���� ����, ��� ��� ������ �������� **xlbitDLLFree**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-185">would fail in this case because **xlbitDLLFree** is set.</span></span> 
  
<span data-ttu-id="a8dfe-186">� �����, ������� **xlAutoFree** � **xlAutoFree12** ���������� ����������� ���, ����� ��� ����������� ������, ��������� � ���������� ��� ������ XLL ��������� **xltypeMulti** � �������� �������� **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-186">In general, **xlAutoFree** and **xlAutoFree12** should be implemented so that they free memory associated with XLL-created **xltypeMulti** arrays and **xltypeRef** external references.</span></span> 
  
<span data-ttu-id="a8dfe-p118">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p118">You might decide to implement your XLL functions so that they ALL return dynamically allocated **XLOPER**s and **XLOPER12**s. In this case, you would need to set **xlbitDLLFree** on all such **XLOPER**s and **XLOPER12**s regardless of the sub-type. You would also need to implement **xlAutoFree** and **xlAutoFree12** so that this memory was freed and also any memory pointed to within the **XLOPER**/ **XLOPER12**. This approach is one way to make the return value thread safe. For example, the previous function could be rewritten as follows.</span></span>
  
```cs
#include <string.h>
LPXLOPER12 WINAPI get_DLL_name_3(int calculation_trigger)
{
// Thread-safe
    LPXLOPER12 pxRtnValue = (LPXLOPER12)malloc(sizeof(XLOPER12));
    Excel12(xlfGetName, pxRtnValue, 0);
// If xlfGetName failed, pxRtnValue will be #VALUE!
    if(pxRtnValue->xltype != xltypeStr)
    {
// Even though an error type does not point to memory,
// Excel needs to pass this oper to xlAutoFree12 to
// free pxRtnValue itself.
        pxRtnValue->xltype |= xlbitDLLFree;
        return pxRtnValue;
    }
// Make a copy of the DLL path and file name.
    wchar_t *leader = L"The full pathname for this DLL is ";
    size_t leader_len = wcslen(leader);
    size_t dllname_len = pxRtnValue->val.str[0];
    size_t msg_len = leader_len + dllname_len;
    wchar_t *msg_text = (wchar_t *)malloc(msg_len + 1);
    wcsncpy_s(msg_text + 1, leader, leader_len);
    wcsncpy_s(msg_text + 1 + leader_len, pxRtnValue->val.str + 1,
        dllname_len);
    msg_text[0] = msg_len;
// Now the original string has been copied Excel can free it.
    Excel12(xlFree, 0, 1, pxRtnValue);
// Now reuse the XLOPER12 for the new string.
    pxRtnValue->val.str = msg_text;
    pxRtnValue->xltype = xltypeStr | xlbitDLLFree;
    return pxRtnValue;
}
void WINAPI xlAutoFree12(LPXLOPER12 p_oper)
{
    if(p_oper->xltype == (xltypeStr | xlbitDLLFree))
        free(p_oper->val.str);
    free(p_oper);
}
```

<span data-ttu-id="a8dfe-192">�������������� �������� � **xlAutoFree** � **xlAutoFree12** ��. � ������ [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-192">For more information about **xlAutoFree** and **xlAutoFree12**, see [xlAutoFree/xlAutoFree12](xlautofree-xlautofree12.md).</span></span>
  
## <a name="returning-modify-in-place-arguments"></a><span data-ttu-id="a8dfe-193">Возвращение аргументов, изменяемых на месте</span><span class="sxs-lookup"><span data-stu-id="a8dfe-193">Returning Modify-in-Place Arguments</span></span>

<span data-ttu-id="a8dfe-p119">В Excel функция XLL может возвращать значение, изменяя аргумент на месте. Это возможно, только если аргумент передается в виде указателя. Для этого функцию необходимо зарегистрировать так, чтобы указать Excel, какой аргумент будет изменяться.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p119">Excel allows an XLL function to return a value by modifying an argument in place. You can only do this with an argument passed in as a pointer. To work like this, the function must be registered in a way that tells Excel which argument will be modified.</span></span> 
  
<span data-ttu-id="a8dfe-197">���� ����� ��� ����������� �������� �������������� ��� ���� ����� ������, ������� ����� ���������� � ������� ���������, �� �������� ������� ��� ��������� �����:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-197">This method of returning a value is supported for all data types that can be passed by pointer but is especially useful for the following types:</span></span>
  
- <span data-ttu-id="a8dfe-198">������ ������ ASCII, ��� ������� ������������ ������� ����� � ������� ������������ �����;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-198">Length-counted and null-terminated ASCII byte strings</span></span>
    
- <span data-ttu-id="a8dfe-199">������ ����������� �������� �������, ��� ������� ������������ ������� ����� � ������� ������������ ����� (� Excel�2007 � ����� ������� ������);</span><span class="sxs-lookup"><span data-stu-id="a8dfe-199">Length-counted and null-terminated Unicode wide character strings (starting in Excel 2007)</span></span>
    
- <span data-ttu-id="a8dfe-200">������� **FP** � ��������� �������;</span><span class="sxs-lookup"><span data-stu-id="a8dfe-200">**FP** floating-point arrays</span></span> 
    
- <span data-ttu-id="a8dfe-201">������� � ��������� ������� **FP12** (� Excel�2007 � ����� ������� ������).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-201">**FP12** floating-point arrays (starting in Excel 2007)</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a8dfe-p120">[!����������] �� ������� �������� ���������� ����� ������� **XLOPER** ��� **XLOPER12**. �������������� �������� ��. � ������ [��������� ��������, ����������� ��� ���������� XLL ��� Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p120">You should not try to return **XLOPER**s or **XLOPER12**s in this manner. For more information, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span> 
  
<span data-ttu-id="a8dfe-p121">������������ ����� ������� ��� �������������� ��������� ����������� ����������� � ���, ��� Excel �������� ������ ��� ������������ ��������. �������� ������ ������������ ������, Excel ����������� ������. ��� ����������� ������� XLL �� ���������� �������. ���� ������ ���������������: ����� ������� � Excel ���������� ������������ � ��������� �������, ��� ������� ������ ������ ������������ ���� �����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p121">The advantage of using this technique, instead of just using the return statement, is that Excel allocates the memory for the return values. Once Excel has finished reading the returned data, it releases the memory. This takes the memory management tasks away from the XLL function. This technique is thread safe: If called concurrently by Excel on different threads, each function call on each thread has its own buffer.</span></span>
  
<span data-ttu-id="a8dfe-p122">��� ������ ��� ������������� ����������� ���� ����� ������, ������ ��� �������� ��������� ������ DLL ��� ������������ ������ ����� �����������, ������� ���������� ��� **XLOPER**/ **XLOPER12**, �� ���������� ��� ������� ����� � �������� **FP**/ **FP12**. �������������, ��� ����������� ��������� � ������� DLL ������ ��� ������� � ��������� ������� � ��� ���� ����������� ���� ��������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p122">It is useful for the previously listed data types in particular because the mechanism for calling back into the DLL to free memory post-return that exists for **XLOPER**/ **XLOPER12**s does not exist for simple strings and **FP**/ **FP12** arrays. Therefore, when returning a DLL-created string or floating-point array, you have the following choices:</span></span> 
  
- <span data-ttu-id="a8dfe-p123">���������� ���������� ��������� ��� ����������� ����������� ������, ���������� ���������. �� ����� ���������� ������ ������� (1) ���������, ��� �������� ��������� � �� ����, (2) ���������� �������, ���������� �� ����� ����������� ������, � �������� �������� ���������, (3) �������� ����������� ��������� ��� ������ ����������� ����� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p123">Set a persistent pointer to a dynamically allocated buffer, return the pointer. On the next call to the function (1) check that the pointer is not null, (2) free the resources allocated on the previous call and reset the pointer to null, (3) reuse the pointer for a newly allocated block of memory.</span></span>
    
- <span data-ttu-id="a8dfe-212">�������� ������ � ������� � ����������� ������, ������� �� ����� �����������, � ���������� ��������� � ����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-212">Create your strings and arrays in a static buffer that does not need to be freed, and return a pointer to that.</span></span>
    
- <span data-ttu-id="a8dfe-213">�������� ��������� �� �����, ������� ������ ��� ������ ��������������� � ������������, ���������� ����������� Excel.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-213">Modify an argument in place, writing your string or array directly into the space set aside by Excel.</span></span>
    
<span data-ttu-id="a8dfe-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-214">Otherwise, you must create an **XLOPER**/ **XLOPER12**, and use **xlbitDLLFree** and **xlAutoFree**/ **xlAutoFree12** to release the resources.</span></span> 
  
<span data-ttu-id="a8dfe-p124">��������� ������� ����� ���� ����� ������� ��� �������� ��������� ���� �� ����, ��� � ������������ ��������. �������� ��������, ��� ������� ������ ���������� � ��� �� ������� ����������� (��� ����� ������� ���� Excel). ������� ������ ��� ����� � �������� **FP**/ **FP12** ��������� ����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p124">The last option might be the simplest in those cases in which you are being passed an argument of the same type as the return value. The key point to remember is that the buffer sizes are limited and you must be very careful not to overrun them. Getting this wrong could crash Excel. Buffer sizes for strings and **FP**/ **FP12** arrays are discussed next.</span></span> 
  
## <a name="strings"></a><span data-ttu-id="a8dfe-219">Строки</span><span class="sxs-lookup"><span data-stu-id="a8dfe-219">Strings</span></span>

<span data-ttu-id="a8dfe-220">Проблемы с управлением памятью строк — наиболее распространенная причина нестабильной работы приложений и надстроек. Это понятно, учитывая множество различных типов строк и способов обработки. Есть строки, которые оканчиваются нулем или для которых используется счетчик длины (а еще строки, для которых выполняются оба эти условия); статические или динамические буферы; строки фиксированной длины или практически неограниченной длины; память, управляемая операционной системой (например, OLE Bstr), или неуправляемые строки, а также другие варианты.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-220">Problems with the management of string memory are arguably the most common cause of instability in applications and add-ins. It is understandable perhaps, given the variety of ways in which strings are handled: null-terminated or length-counted (or both); static or dynamic buffers; fixed length or almost unlimited length; operating-system managed memory (for example, OLE Bstr) or unmanaged strings; and so on.</span></span>
  
<span data-ttu-id="a8dfe-p125">������������ C/C++ ���� ����� ���������� ������, �������������� �����. ����������� ���������� C ������������� ��� ������ � ������ ��������. ����������� ��������� �������� � ���� ������������� � ������, �������������� �����. ����� ����, Excel �������� �� �������� �� ��������� �����, ������� ������ �� ������������ �����. ��������� ���� ������ ������� ������� � ����������������� ������� � ��������� ����� � ������ ����� � DLL � XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p125">C/C++ programmers are most familiar with null-terminated strings. The standard C library is designed to work with such strings. Static string literals in code are compiled into null-terminated strings. Alternatively, Excel works with length-counted strings that are not in general null-terminated. The combination of these facts requires a clear and consistent approach within your DLL/XLL regarding how you handle strings and string memory.</span></span>
  
<span data-ttu-id="a8dfe-226">���� ��������� �������� ���������������� ��������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-226">The most common problems are as follows:</span></span>
  
- <span data-ttu-id="a8dfe-227">�������� ������� ��� ������������� ��������� � �������, ������� ������� ���������� ��������� � �� ��������� ��� �� ����� ��������� ��� ������������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-227">The passing of a null or invalid pointer to a function that expects a valid pointer and does not or cannot check the pointer's validity itself.</span></span>
    
- <span data-ttu-id="a8dfe-228">������������ ������ ������ ��������, ������� �� ������������ ��� �� ����� ����������� ������ ������ � ����� ������������ ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-228">The overrunning of the bounds of a string buffer by a function that does not or cannot check the length of the buffer against the length of the string being written.</span></span>
    
- <span data-ttu-id="a8dfe-229">Попытка освободить память буфера строки, если он статический или уже освобожденный, а также если способы освобождения и выделения не совпадают.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-229">Trying to free string buffer memory that is either static, or has been freed already, or was not allocated in a way that is consistent with how it is being freed.</span></span>
    
- <span data-ttu-id="a8dfe-230">Утечки памяти в результате выделения без последующего освобождения строк (обычно в часто вызываемой функции).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-230">Memory leaks that result from strings being allocated and then not freed, usually in a frequently called function.</span></span>
    
### <a name="rules-for-strings"></a><span data-ttu-id="a8dfe-231">Правила для строк</span><span class="sxs-lookup"><span data-stu-id="a8dfe-231">Rules for Strings</span></span>

<span data-ttu-id="a8dfe-p126">��� � ��� **XLOPER**/ **XLOPER**, ��� ����� ���������� ������� � ������������, ������� ���������� ���������. ������������ �� ���������� �� ����������� � ���������� �������. �������������� ������� ��� ����� ��������� ����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p126">As with **XLOPER**/ **XLOPER**s, there are rules and guidelines you should follow. The guidelines are the same as given in the previous section. The rules here are an extension of the rules specifically for strings.</span></span>
  
 <span data-ttu-id="a8dfe-235">**�������:**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-235">**Rules:**</span></span>
  
- <span data-ttu-id="a8dfe-p127">�� ��������� ���������� ������ ��� ������������ ������ **XLOPER**/ **XLOPER12**, � ����� ������� ������ �� ��������� ����� ��� ������, �������������� �����, ������� ���������� ��� ��������� � ������� XLL. ����� ��������� ������������� ������ ��� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p127">Do not try to free memory or overwrite string **XLOPER**/ **XLOPER12**s or simple length-counted or null-terminated strings passed as arguments to your XLL function. You should treat such arguments as read-only.</span></span>
    
- <span data-ttu-id="a8dfe-238">���� Excel �������� ������ ������ **XLOPER**/ **XLOPER12** ��� ��������� ������������� �������� ������� ��������� ������ API C, ���������� �� � ������� ������� **xlFree** ��� ������� �������� **xlbitXLFree** ��� �� ����������� � Excel �� ������� XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-238">Where Excel allocates memory for a string **XLOPER**/ **XLOPER12** for the return value of a C API callback function, use **xlFree** to free it, or set **xlbitXLFree** if returning it to Excel from an XLL function.</span></span> 
    
- <span data-ttu-id="a8dfe-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-239">Where your DLL dynamically allocates a string buffer for an **XLOPER**/ **XLOPER12**, free it in a way consistent with how you allocated it when done, or set **xlbitDLLFree** if returning it to Excel from an XLL function and then free it in **xlAutoFree**/ **xlAutoFree12**.</span></span>
    
- <span data-ttu-id="a8dfe-p128">���� Excel �������� ������ ������� **xltypeMulti**, ������������� � ���������� DLL �� ����� ������ API C, �� ��������������� ������ **XLOPER**/ **XLOPER12** � �������. ��� ������������ ���� �������� ���������� ������������ ������ ������� **xlFree** ��� �������� **xlbitXLFree** ��� ����������� �� ������� XLL.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p128">If Excel has allocated memory for an **xltypeMulti** array returned to your DLL in a call to the C API, do not overwrite any string **XLOPER**/ **XLOPER12**s within the array. Such arrays must only be freed using **xlFree**, or, if being returned by an XLL function, by setting **xlbitXLFree**.</span></span>
    
### <a name="string-types-supported"></a><span data-ttu-id="a8dfe-242">Поддерживаемые типы строк</span><span class="sxs-lookup"><span data-stu-id="a8dfe-242">String Types Supported</span></span>

<span data-ttu-id="a8dfe-243">**������ XLOPER/XLOPER12 xltypeStr API C**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-243">**C API xltypeStr XLOPER/XLOPER12s**</span></span>

|<span data-ttu-id="a8dfe-244">\*\*������ ������: \*\*XLOPER\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a8dfe-244">\*\*Byte strings: \*\*XLOPER\*\*\*\*</span></span>|<span data-ttu-id="a8dfe-245">\*\*������ ����������� ��������: \*\*XLOPER12\*\*\*\*</span><span class="sxs-lookup"><span data-stu-id="a8dfe-245">\*\*Wide character strings: \*\*XLOPER12\*\*\*\*</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8dfe-246">��� ������ Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-246">All versions of Excel</span></span>  <br/> |<span data-ttu-id="a8dfe-247">Excel�2007 � ����� ������� ������</span><span class="sxs-lookup"><span data-stu-id="a8dfe-247">Starting in Excel 2007</span></span>  <br/> |
|<span data-ttu-id="a8dfe-248">������������ �����: 255 ������ ������������ ���� ASCII</span><span class="sxs-lookup"><span data-stu-id="a8dfe-248">Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="a8dfe-249">Максимальная длина: 32 767 символов Юникода</span><span class="sxs-lookup"><span data-stu-id="a8dfe-249">Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="a8dfe-250">Первый байт (без знака) = длина</span><span class="sxs-lookup"><span data-stu-id="a8dfe-250">First (unsigned) byte = length</span></span>  <br/> |<span data-ttu-id="a8dfe-251">������ ������ ������� = �����</span><span class="sxs-lookup"><span data-stu-id="a8dfe-251">First Unicode character = length</span></span>  <br/> |
   
> [!IMPORTANT]
> <span data-ttu-id="a8dfe-252">[!�����!] ������ **XLOPER** ��� **XLOPER12** �� ������ ������������ �����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-252">Do not assume null termination of **XLOPER** or **XLOPER12** strings.</span></span> 
  
<span data-ttu-id="a8dfe-253">**������ C/C++**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-253">**C/C++ strings**</span></span>

|<span data-ttu-id="a8dfe-254">**������ ������**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-254">**Byte strings**</span></span>|<span data-ttu-id="a8dfe-255">**������ ����������� ��������**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-255">**Wide character strings**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a8dfe-256">Оканчивающиеся нулем (**char** \*), тип "C", максимальная длина составляет 255 байтов расширенного кода ASCII</span><span class="sxs-lookup"><span data-stu-id="a8dfe-256">Null-terminated (**char** \*) "C" Max length: 255 extended ASCII bytes</span></span>  <br/> |<span data-ttu-id="a8dfe-257">Оканчивающиеся нулем (**wchar_t** \*), тип "C%", максимальная длина составляет 32 767 символов Юникода</span><span class="sxs-lookup"><span data-stu-id="a8dfe-257">Null-terminated (**wchar_t** \*) "C%" Maximum length 32,767 Unicode chars</span></span>  <br/> |
|<span data-ttu-id="a8dfe-258">Со счетчиком длины (**unsigned char** \*), тип "D"</span><span class="sxs-lookup"><span data-stu-id="a8dfe-258">Length-counted (**unsigned char** \*) "D"</span></span>  <br/> |<span data-ttu-id="a8dfe-259">Со счетчиком длины (**wchar_t** \*), тип "D%"</span><span class="sxs-lookup"><span data-stu-id="a8dfe-259">Length-counted (**wchar_t** \*) "D%"</span></span>  <br/> |
   
### <a name="strings-in-xltypemulti-xloperxloper12-arrays"></a><span data-ttu-id="a8dfe-260">Строки в массивах XLOPER/XLOPER12 xltypeMulti</span><span class="sxs-lookup"><span data-stu-id="a8dfe-260">Strings in xltypeMulti XLOPER/XLOPER12 Arrays</span></span>

<span data-ttu-id="a8dfe-p129">� ��������� ������� Excel ������� ������ **xltypeMulti** ��� ������������� � ����������� DLL � XLL. ��������� �������������� ������� XLM ���������� ����� �������. ��������, ������� API C **xlfGetWorkspace** ��� �������� �� ���������  *44*  ���������� ������, ���������� ������, ������� ��������� ��� ������������������ ��������� DLL. ������� API C **xlfDialogBox** ���������� ���������� ����� ��������� �������, ���������� �������� ����� �����. ��������, ���� ����� ���������� XLL ������������ ������ **xltypeMulti** ��� ��� �������� � �������� ��������� � ������� XLL ��� �������������� � ���� ��� �� ���� ������ �� ��������. � ����� ������� Excel ������� �������� ����� ����� � �������� ������� � ��������� �� ��� � �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p129">In several cases, Excel creates an **xltypeMulti** array for use in your DLL/XLL. Several of the XLM information functions return such arrays. For example, the C API function **xlfGetWorkspace**, when passed the argument  *44*  , returns an array containing strings that describe all the currently registered DLL procedures. The C API function **xlfDialogBox** returns a modified copy of its array argument, containing deep copies of the strings. Perhaps the most common way an XLL encounters an **xltypeMulti** array is where it has been passed as an argument to an XLL function, or it has been coerced to this type from a range reference. In these latter cases, Excel creates deep copies of the strings in the source cells and points to these within the array.</span></span> 
  
<span data-ttu-id="a8dfe-p130">���� �� ������ �������� ��� ������ � ���������� DLL, ������� ������� ����������� �������� �����. ��� �������� ����������� �������� **xltypeMulti** �� ������� �������� � ��� ���������� Excel ������ **XLOPER**/ **XLOPER12**. ���������� ���� �� ���������� �� ��������� ��� �� ���������� ������. ����� ����, ������� ��������� �������� ����� ����� � ������� ��������� �� ����� � �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p130">Where you want to modify these strings in your DLL, you should make your own deep copies. When you are creating your own **xltypeMulti** arrays, you should not place Excel-allocated string **XLOPER**/ **XLOPER12**s within them. This risks you not freeing them correctly later, or not freeing them at all. Again, you should make deep copies of the strings and store pointers to the copies in the array.</span></span>
  
 <span data-ttu-id="a8dfe-271">**�������**</span><span class="sxs-lookup"><span data-stu-id="a8dfe-271">**Examples**</span></span>
  
<span data-ttu-id="a8dfe-p131">� ��������� ������� ������� ������� ����������� ���������� ����� ������ ������� �� ��������� �����. �������� ��������, ��� ���������� ������� � �������� ����� ������ ���������� ������, ���������� � ���� �������, � ������� ��������� **delete**[], � �������� ������ �� ������ ������������ �����. ������ ����� ���������, ���� ��� ���������� ��� ������������, � �� ������������ �����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p131">The following example function creates a dynamically allocated copy of a length-counted Unicode string. Note that the caller must ultimately free the memory allocated in this example using **delete**[], and that the source string is not assumed to be null terminated. The copy string is truncated if necessary for safety, and is not null terminated.</span></span>
  
```cs
#include <string.h>
#define MAX_V12_STRBUFFLEN    32678
    
wchar_t * deep_copy_wcs(const wchar_t *p_source)
{
    if(!p_source)
        return NULL;
    size_t source_len = p_source[0];
    bool truncated = false;
    if(source_len >= MAX_V12_STRBUFFLEN)
    {
        source_len = MAX_V12_STRBUFFLEN - 1; // Truncate the copy
        truncated = true;
    }
    wchar_t *p_copy = new wchar_t[source_len + 1];
    wcsncpy_s(p_copy, p_source, source_len + 1);
    if(truncated)
        p_copy[0] = source_len;
    return p_copy;
}
```

<span data-ttu-id="a8dfe-p132">����� � ������� ���� ������� ����� ��������� ���������� **XLOPER12**, ��� �������� �� ������� ��������� �������������� ������� XLL, ������������ ����� ���������, ���� ��� ������. ��� ������ ���� ������������ ��� ������ ������. �������� ��������, ��� ��������� �� �������������� � ������� ���������� **#VALUE!**. ��� ������� ���������� ���������������� ��� �����, ������� ��������� �������� ���� "U", ��� �������� ������ � ���� ��������. ��� ������������ ���������� ������� **T()** ����� (�� ����������� ����, ��� **AsText** ����� ����������� ������ � ������ ������). � ���� ������� ���� ��������������, ��� **xlAutoFree12** ����������� ���������� ���������, � ����� ��� ����������, � ������� ��������� **delete**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p132">This function can then be safely used to copy an **XLOPER12**, as shown in the following exportable XLL function that returns a copy of its argument if it is a string. All other types are returned as a zero-length string. Note that ranges are not handled—the function returns **#VALUE!**. The function must be registered as taking a type U argument so that references are passed in as values. This is equivalent to the built-in worksheet function **T()** except that **AsText** also converts errors to zero-length strings. This code example assumes that **xlAutoFree12** frees the passed-in pointer, and also its contents, using **delete**.</span></span>
  
```cs
LPXLOPER12 WINAPI AsText(LPXLOPER12 pArg)
{
    LPXLOPER12 pRtnVal = new XLOPER12;
// If the input was an array, only operate on the top-left element.
    LPXLOPER *pTemp;
    if(pArg->xltype == xltypeMulti)
        pTemp = pArg->val.array.lparray;
    else
        pTemp = pArg;
    switch(pTemp->xltype)
    {
        case xltypeErr:
        case xltypeNum:
        case xltypeMissing:
        case xltypeNil:
        case xltypeBool:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(L"\000");
            return pRtnVal;
        case xltypeStr:
            pRtnVal->xltype = xltypeStr | xlbitDLLFree;
            pRtnVal->val.str = deep_copy_wcs(pTemp->val.str);
            return pRtnVal;
        
        default: // xltypeSRef, xltypeRef, xltypeFlow, xltypeInt
            pRtnVal->xltype = xltypeErr | xlbitDLLFree;
            pRtnVal->val.err = xlerrValue;
            return pRtnVal;
    }
}
```

### <a name="returning-modify-in-place-string-arguments"></a><span data-ttu-id="a8dfe-281">Возвращение строковых аргументов, изменяемых на месте</span><span class="sxs-lookup"><span data-stu-id="a8dfe-281">Returning Modify-in-Place String Arguments</span></span>

<span data-ttu-id="a8dfe-p133">���������, ������������������ ��� ��������� ����� **F**, **G**, **F%** � **G%**, ����� �������� �� �����. ������������� ��������� ��������� ��� ���� �����, Excel ������� ����� ������������� �������. ����� Excel �������� � ���� ������ ���������, ���� ���� ��� ����������� ������. ��� ��������� ������� XLL ���������� ������������ �������� ��������������� � �� �� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p133">Arguments registered as types **F**, **G**, **F%**, and **G%** can be modified in place. When Excel is preparing string arguments for these types, it creates a maximum length buffer. Then it copies the argument string into that, even if this string is very much shorter. This enables the XLL function to write its return value directly into the same memory.</span></span> 
  
<span data-ttu-id="a8dfe-286">���� ��������� ������� ������, ������������� ��� ���� �����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-286">Buffer sizes set apart for these types are as follows:</span></span>
  
- <span data-ttu-id="a8dfe-287">**Строки байтов:** 256 байтов, включая счетчик длины (тип "G") или завершающий символ нуля (тип "F").</span><span class="sxs-lookup"><span data-stu-id="a8dfe-287">**Byte strings:** 256 bytes including the length counter (type G) or null-termination (type F).</span></span> 
    
- <span data-ttu-id="a8dfe-288">**Строки в кодировке Юникод:** 32 768 расширенных символов (65 536 байтов), включая счетчик длины (тип "G%") или завершающий символ нуля (тип "F%").</span><span class="sxs-lookup"><span data-stu-id="a8dfe-288">**Unicode strings:** 32,768 wide characters (65,536 bytes) including the length counter (type G%) or null-termination (type F%).</span></span> 
    
> [!NOTE]
> <span data-ttu-id="a8dfe-p134">[!����������] ��� ������� ���������� ������� ��������������� �� Visual Basic ��� ���������� (VBA), ��� ��� �� �� ������ ������������� ��������� ������ ���������� �������� �������. ��������� ��� ������� ����� ������� ������ �� ������ ���������� DLL, ���� �� ���� �������� ���������� ������� �����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p134">You cannot call such a function directly from Visual Basic for Applications (VBA) because you cannot ensure that a sufficiently large buffer has been allocated. You can only call such a function from another DLL safely if you have explicitly passed a big enough buffer.</span></span> 
  
<span data-ttu-id="a8dfe-p135">���� �������� ������ ������� XLL, ������� �������� �� �������� ������������������ ����������� �������� � ���������� ������, �������������� �����, ��������� ����������� ������� ���������� **wcsrev**. �������� � ���� ������ ����� ��������������� ��� �������� ���� **F%**.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p135">Here is an example of an XLL function that reverses a passed-in null-terminated wide character string using the standard library function **wcsrev**. The argument in this case would be registered as type **F%**.</span></span>
  
```cs
void WINAPI reverse_text_xl12(wchar_t *text)
{
    _wcsrev(text);
}
```

## <a name="persistent-storage-binary-names"></a><span data-ttu-id="a8dfe-293">Постоянное хранилище (двоичные имена)</span><span class="sxs-lookup"><span data-stu-id="a8dfe-293">Persistent Storage (Binary Names)</span></span>

<span data-ttu-id="a8dfe-294">Двоичные имена определяются и связываются с блоками двоичных объектов, то есть с неструктурированными данными, хранящимися вместе с книгой.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-294">Binary names are defined and associated with blocks of binary, that is, unstructured, data that is stored together with the workbook.</span></span> <span data-ttu-id="a8dfe-295">Они создаются с помощью функции [кслдефинебинаринаме](xldefinebinaryname.md), а данные извлекаются с помощью функции [кслжетбинаринаме](xlgetbinaryname.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-295">They are created using the function [xlDefineBinaryName](xldefinebinaryname.md), and the data is retrieved using the function [xlGetBinaryName](xlgetbinaryname.md).</span></span> <span data-ttu-id="a8dfe-296">Обе функции описаны более подробно в справочнике по функциям (см. [функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), и в обоих случаях используется структура **кслтипебигдата** **XLOPER**/ \*\*\*\*.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-296">Both functions are described in more detail in the function reference (see [C API Functions That Can Be Called Only from a DLL or XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)), and both use the **xltypeBigData** **XLOPER**/ **XLOPER12**.</span></span> 
  
<span data-ttu-id="a8dfe-297">�������� �� ��������� ���������, ������� ������������ ������������ ���������� �������� ����, ��. � ������ [��������� ��������, ����������� ��� ���������� XLL ��� Excel](known-issues-in-excel-xll-development.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-297">For information about known issues that limit the practical applications of binary names, see [Known Issues in Excel XLL Development](known-issues-in-excel-xll-development.md).</span></span>
  
## <a name="excel-stack"></a><span data-ttu-id="a8dfe-298">Стек Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-298">Excel Stack</span></span>

<span data-ttu-id="a8dfe-p137">Excel использует стек вместе со всеми загруженными библиотеками DLL. Места в стеке обычно более чем достаточно для обычного использования. О нем не нужно беспокоиться, если вы выполняете следующие рекомендации:</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p137">Excel shares its stack space with all the DLLs it has loaded. Stack space is usually more than adequate for ordinary use, and you do not need to be concerned about it as long as you follow a few guidelines:</span></span> 
  
- <span data-ttu-id="a8dfe-p138">�� ����������� ����� ������� ��������� � �������� ���������� ������� � ���� �������� � �����. ����������� ��������� ��� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p138">Do not pass very large structures as arguments to functions by value on the stack. Pass pointers or references instead.</span></span>
    
- <span data-ttu-id="a8dfe-p139">�� ����������� ������� ��������� � �����. ����������� ��������� �� ����������� ��� ����������� ���������� ������ ��� ����������� ���������, ������������ � �������������� ������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p139">Do not return large structures on the stack. Return pointers to static or dynamically allocated memory, or use arguments passed by reference.</span></span>
    
- <span data-ttu-id="a8dfe-p140">�� ���������� ����� ������� ��������� �������������� ���������� � ���� �������. ���� ����������, �������� �� ��� �����������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p140">Do not declare very large automatic variable structures in the function code. If you need them, declare them as static.</span></span>
    
- <span data-ttu-id="a8dfe-p141">�� ��������� ������� ����������, ���� �� �������, ��� �������� ������ ����� ��������. ������ ����� ����������� ����.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p141">Do not call functions recursively unless you are sure the depth of recursion will always be shallow. Try using a loop instead.</span></span>
    
<span data-ttu-id="a8dfe-p142">������� �������� ����� �� ���������� DLL � ������� API C, Excel ������� ���������, ���������� �� ����� � ����� ��� ������ ������� ��������. ���� Excel ���������, ��� ���������� ����� ����� ���� ������������, �� ���������� ����� ��� ������������, ���� ���� �� ����� ���� ����� ����������. � ���� ������ ��� �������� ������ ������������ ��� **xlretFailed**. ��� ������� ������������� API C � ����� ���� ������ API C ���� �� ���������� �� ���� �������.</span><span class="sxs-lookup"><span data-stu-id="a8dfe-p142">When a DLL calls back into Excel using the C API, Excel first checks whether there is enough space on the stack for the worst-case usage call that could be made. If it thinks there might be insufficient room, it will fail the call to be safe, even though there might actually have been enough space for that particular call. In this case, the callbacks return the code **xlretFailed**. For ordinary use of the C API and the stack, this is an unlikely cause of the failure of a C API call.</span></span>
  
<span data-ttu-id="a8dfe-313">���� �� ������ ��������� ���������� ����� � ����� �� ��������� ������ ����, ������� ����� �����, ������ ������� [xlStack](xlstack.md).</span><span class="sxs-lookup"><span data-stu-id="a8dfe-313">If you are concerned, or just curious, or you want to eliminate lack of stack space as a reason for an unexplained failure, you can find out how much stack space there is with a call to the [xlStack](xlstack.md) function.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a8dfe-314">См. также</span><span class="sxs-lookup"><span data-stu-id="a8dfe-314">See also</span></span>



[<span data-ttu-id="a8dfe-315">Многопоточный пересчет в Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-315">Multithreaded Recalculation in Excel</span></span>](multithreaded-recalculation-in-excel.md)
  
[<span data-ttu-id="a8dfe-316">��������������� � ��������� ������ � Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-316">Multithreading and Memory Contention in Excel</span></span>](multithreading-and-memory-contention-in-excel.md)
  
[<span data-ttu-id="a8dfe-317">Разработка XLL-файлов для Excel</span><span class="sxs-lookup"><span data-stu-id="a8dfe-317">Developing Excel XLLs</span></span>](developing-excel-xlls.md)

