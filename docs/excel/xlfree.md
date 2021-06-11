---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- функция xlfree [Excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: de1c75ad65acacd44644e9bfb111b30abd0a578e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424716"
---
# <a name="xlfree"></a><span data-ttu-id="7e6dc-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="7e6dc-104">xlFree</span></span>

 <span data-ttu-id="7e6dc-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="7e6dc-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="7e6dc-106">Используется для бесплатного использования ресурсов памяти, выделенных Microsoft Excel при создании возвращаемой стоимости **XLOPER XLOPER12** в вызове в /   [Excel4,](excel4-excel12.md) [Excel4v,](excel4v-excel12v.md) [Excel12](excel4-excel12.md)или [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="7e6dc-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="7e6dc-107">Функция **xlFree** освободит вспомогательную память и сбросит указатель в **NULL,** но не уничтожает другие части **XLOPER XLOPER12.** /  </span><span class="sxs-lookup"><span data-stu-id="7e6dc-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="7e6dc-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="7e6dc-108">Parameters</span></span>

 <span data-ttu-id="7e6dc-109">_px_1, ..., px_n_</span><span class="sxs-lookup"><span data-stu-id="7e6dc-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="7e6dc-110">Один или несколько /  **XLOPER XLOPER12** s, которые будут освобождены.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-110">One or more **XLOPER**/ **XLOPER12** s to be freed.</span></span> <span data-ttu-id="7e6dc-111">В Excel версии до 2003 года максимальное количество указателей, которые можно передать, — 30.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="7e6dc-112">Начиная с Excel 2007 г. это число увеличивается до 255.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="7e6dc-113">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="7e6dc-113">Property value/Return value</span></span>

<span data-ttu-id="7e6dc-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="7e6dc-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="7e6dc-115">Remarks</span></span>

<span data-ttu-id="7e6dc-116">Вы должны освободить каждый **XLOPER,** который вы получаете в качестве возвращаемого значения от **Excel4** или **Excel4v,** и каждый **XLOPER12,** который вы получаете в качестве возвращаемого значения от **Excel12** или **Excel12v,** если они являются одним из следующих типов: **xltypeStr**, **xltypeMulti** или **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="7e6dc-117">Всегда безопасно освободить другие типы, даже если они не используют вспомогательную память, если вы получили их из **Excel4** или **Excel12.**</span><span class="sxs-lookup"><span data-stu-id="7e6dc-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="7e6dc-118">При возвращении в Excel указатель **XLOPER XLOPER12,** который по-прежнему содержит Excel выделенную память, необходимо установить /   **xlbitXLFree,** чтобы Excel высвободить память.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="7e6dc-119">Пример</span><span class="sxs-lookup"><span data-stu-id="7e6dc-119">Example</span></span>

<span data-ttu-id="7e6dc-120">В этом примере **вызываетСЯ GET. WORKSPACE (1)** для возврата платформы, на Excel которой в настоящее время запущена строка.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="7e6dc-121">Код копирует возвращенную строку в буфер для более позднего использования.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="7e6dc-122">Код возвращает буфер в **XLOPER12** для более позднего использования с Excel функцией.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="7e6dc-123">Наконец, код отображает строку в поле оповещений.</span><span class="sxs-lookup"><span data-stu-id="7e6dc-123">Finally, the code displays the string in an alert box.</span></span> 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlFreeExample(void)
{
   XLOPER12 xRes, xInt;
   XCHAR buffer[cchMaxStz];
   int i,len;
   // Create an XLOPER12 for the argument to Getworkspace.
   xInt.xltype = xltypeInt;
   xInt.val.w = 1;
   // Call GetWorkspace.
   Excel12f(xlfGetWorkspace, &xRes, 1, (LPXLOPER12)&xInt);
   
   // Get the length of the returned string
   len = (int)xRes.val.str[0];
   //Take into account 1st char, which contains the length
   //and the null terminator. Truncate if necessary to fit
   //buffer.
   if (len > cchMaxStz - 2)
      len = cchMaxStz - 2;
   // Copy to buffer.
   for(i = 1; i <= len; i++)
      buffer[i] = xRes.val.str[i];
   // Null terminate, Not necessary but a good idea.
   buffer[len] = '\0';
   buffer[0] = len;
   // Free the string returned from Excel.
   Excel12f(xlFree, 0, 1, &xRes);
   // Create a new string XLOPER12 for the alert.
   xRes.xltype = xltypeStr;
   xRes.val.str = buffer;
   // Show the alert.
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a><span data-ttu-id="7e6dc-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7e6dc-124">See also</span></span>

- [<span data-ttu-id="7e6dc-125">Функции API C, которые можно вызывать только из библиотеки DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="7e6dc-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

