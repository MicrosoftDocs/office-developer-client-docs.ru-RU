---
title: xlFree
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlFree
keywords:
- функция xlFree [excel 2007]
localization_priority: Normal
ms.assetid: 8ce2eef2-0138-495d-b6cb-bbb727a3cda4
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 2dd61ee5cd0e2e671cc47425689287b8a437732f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807361"
---
# <a name="xlfree"></a><span data-ttu-id="42b1b-104">xlFree</span><span class="sxs-lookup"><span data-stu-id="42b1b-104">xlFree</span></span>

 <span data-ttu-id="42b1b-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="42b1b-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="42b1b-106">Используется, чтобы освободить память, ресурсы, выделенные Microsoft Excel при создании возвращаемое значение **XLOPER**/ **XLOPER12** к вызову [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md)или [Excel12v](excel4v-excel12v.md).</span><span class="sxs-lookup"><span data-stu-id="42b1b-106">Used to free memory resources allocated by Microsoft Excel when creating the return value **XLOPER**/ **XLOPER12** in a call to [Excel4](excel4-excel12.md), [Excel4v](excel4v-excel12v.md), [Excel12](excel4-excel12.md), or [Excel12v](excel4v-excel12v.md).</span></span> <span data-ttu-id="42b1b-107">Функция **xlFree** освобождает память, дополнительный и сбрасывает указатель на **значение NULL** , но не уничтожает другим частям **XLOPER**/ **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="42b1b-107">The **xlFree** function frees the auxiliary memory and resets the pointer to **NULL** but does not destroy other parts of the **XLOPER**/ **XLOPER12**.</span></span>
  
```cs
Excel4(xlFree, 0, n, LPXLOPER px_1, ..., LPXLOPER px_n);
Excel12(xlFree, 0, n, LPXLOPER12 px_1, ..., LPXLOPER12 px_n);
```

## <a name="parameters"></a><span data-ttu-id="42b1b-108">Parameters</span><span class="sxs-lookup"><span data-stu-id="42b1b-108">Parameters</span></span>

 <span data-ttu-id="42b1b-109">_px_1,..., px_n_</span><span class="sxs-lookup"><span data-stu-id="42b1b-109">_px_1, ..., px_n_</span></span>
  
<span data-ttu-id="42b1b-110">Один или несколько **XLOPER**/ **XLOPER12**s, чтобы освободить.</span><span class="sxs-lookup"><span data-stu-id="42b1b-110">One or more **XLOPER**/ **XLOPER12**s to be freed.</span></span> <span data-ttu-id="42b1b-111">В версиях Excel до 2003 максимальное число указателей, может быть передан: 30.</span><span class="sxs-lookup"><span data-stu-id="42b1b-111">In Excel versions up to 2003, the maximum number of pointers that can be passed is 30.</span></span> <span data-ttu-id="42b1b-112">Начиная с версии Excel 2007, это увеличивается до 255.</span><span class="sxs-lookup"><span data-stu-id="42b1b-112">Starting in Excel 2007, this is increased to 255.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="42b1b-113">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="42b1b-113">Property value/Return value</span></span>

<span data-ttu-id="42b1b-114">Эта функция не возвращает значение.</span><span class="sxs-lookup"><span data-stu-id="42b1b-114">This function does not return a value.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="42b1b-115">Замечания</span><span class="sxs-lookup"><span data-stu-id="42b1b-115">Remarks</span></span>

<span data-ttu-id="42b1b-116">Необходимо освободить каждые **XLOPER** , получаемые как возвращаемое значение из **Excel4** или **Excel4v** и каждые **XLOPER12** , который можно получить как возвращаемое значение от **Excel12** или **Excel12v** если они находятся на один из следующих типов: **xltypeStr **, **xltypeMulti**или **xltypeRef**.</span><span class="sxs-lookup"><span data-stu-id="42b1b-116">You must free every **XLOPER** that you get as a return value from **Excel4** or **Excel4v** and every **XLOPER12** that you get as a return value from **Excel12** or **Excel12v** if they are one of the following types: **xltypeStr**, **xltypeMulti**, or **xltypeRef**.</span></span> <span data-ttu-id="42b1b-117">Всегда безопасно Бесплатная загрузка других типов даже в том случае, если не используют дополнительный объем памяти до тех пор, пока полученный в **Excel4** или **Excel12**.</span><span class="sxs-lookup"><span data-stu-id="42b1b-117">It is always safe to free other types even if they do not use auxiliary memory, as long as you got them from **Excel4** or **Excel12**.</span></span>
  
<span data-ttu-id="42b1b-118">Где возвращается в Excel указатель **XLOPER**/ **XLOPER12** , по-прежнему содержит памяти Excel, выделенный для освобождения, необходимо установить **xlbitXLFree** для обеспечения выпуски Excel объем памяти.</span><span class="sxs-lookup"><span data-stu-id="42b1b-118">Where you are returning to Excel a pointer to an **XLOPER**/ **XLOPER12** that still contains Excel-allocated memory to be freed, you must set the **xlbitXLFree** to ensure Excel releases the memory.</span></span> 
  
## <a name="example"></a><span data-ttu-id="42b1b-119">Пример</span><span class="sxs-lookup"><span data-stu-id="42b1b-119">Example</span></span>

<span data-ttu-id="42b1b-120">В этом примере вызывается **ПОЛУЧИТЕ. WORKSPACE(1)** для возврата платформу, на какие Excel — в настоящее время работает в виде строки.</span><span class="sxs-lookup"><span data-stu-id="42b1b-120">This example calls **GET.WORKSPACE(1)** to return the platform on which Excel is currently running as a string.</span></span> <span data-ttu-id="42b1b-121">Код копирует этот возвращенный строки в буфер для дальнейшего использования.</span><span class="sxs-lookup"><span data-stu-id="42b1b-121">The code copies this returned string into a buffer for later use.</span></span> <span data-ttu-id="42b1b-122">Код помещает буфера обратно в **XLOPER12** для дальнейшего использования с помощью функции Excel.</span><span class="sxs-lookup"><span data-stu-id="42b1b-122">The code places the buffer back into the **XLOPER12** for later use with the Excel function.</span></span> <span data-ttu-id="42b1b-123">И, наконец код отображает строку сообщение об ошибке.</span><span class="sxs-lookup"><span data-stu-id="42b1b-123">Finally, the code displays the string in an alert box.</span></span> 
  
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

## <a name="see-also"></a><span data-ttu-id="42b1b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="42b1b-124">See also</span></span>

- [<span data-ttu-id="42b1b-125">Функции интерфейса API для C, которые могут вызываться только из DLL или XLL</span><span class="sxs-lookup"><span data-stu-id="42b1b-125">C API Functions That Can Be Called Only from a DLL or XLL</span></span>](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

