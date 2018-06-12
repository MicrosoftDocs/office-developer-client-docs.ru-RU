---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- функция xladdinmanagerinfo [excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e42cca809c4426ddf9a98b3b275d08490d31c8db
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807327"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="2e744-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="2e744-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="2e744-105">**Применимо к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="2e744-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="2e744-106">Именем с Microsoft Excel, когда диспетчер надстроек вызывается в первый раз в сеансе Excel.</span><span class="sxs-lookup"><span data-stu-id="2e744-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="2e744-107">Эта функция используется для предоставления сведений о надстройке Диспетчер надстроек.</span><span class="sxs-lookup"><span data-stu-id="2e744-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="2e744-108">Excel 2007 и более поздних версий вызовите **xlAddInManagerInfo12** вместо **xlAddInManagerInfo** при экспорте с XLL.</span><span class="sxs-lookup"><span data-stu-id="2e744-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="2e744-109">Функция **xlAddInManagerInfo12** должны работать в так же, как **xlAddInManagerInfo** во избежание разных версий различия в поведении XLL.</span><span class="sxs-lookup"><span data-stu-id="2e744-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="2e744-110">Предполагается, что **xlAddInManagerInfo12** возвращает тип данных **XLOPER12** , тогда как **xlAddInManagerInfo** должен возвращать **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="2e744-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="2e744-111">Функция **xlAddInManagerInfo12** не вызывается с версии Excel, предшествующие Excel 2007, как они не поддерживают **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="2e744-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="2e744-112">Excel не требуется XLL внедрение и экспортировать любой из этих функций.</span><span class="sxs-lookup"><span data-stu-id="2e744-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="2e744-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="2e744-113">Parameters</span></span>

 <span data-ttu-id="2e744-114">_pxAction:_ Указатель на числовой **XLOPER и XLOPER12** (**xltypeInt** или **xltypeNum**).</span><span class="sxs-lookup"><span data-stu-id="2e744-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="2e744-115">Сведения о, запрашивает Excel.</span><span class="sxs-lookup"><span data-stu-id="2e744-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="2e744-116">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2e744-116">Property value/Return value</span></span>

<span data-ttu-id="2e744-117">Если _pxAction_ является или могут быть приведены к номер 1, реализация этой функции должен возвращать строку, содержащую сведения о надстройки, обычно его имя и может быть номер версии.</span><span class="sxs-lookup"><span data-stu-id="2e744-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="2e744-118">В противном случае возвращается #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="2e744-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="2e744-119">Если строка не возвращают, Excel пытается преобразовать возвращаемое значение в строку.</span><span class="sxs-lookup"><span data-stu-id="2e744-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="2e744-120">Замечания</span><span class="sxs-lookup"><span data-stu-id="2e744-120">Remarks</span></span>

<span data-ttu-id="2e744-121">Если Возвращенная строка указывает динамически выделенный буфер, необходимо убедиться, что в конечном счете освобождается этот буфер.</span><span class="sxs-lookup"><span data-stu-id="2e744-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="2e744-122">Если строка выделена в Excel, это можно сделать, задав **xlbitXLFree**.</span><span class="sxs-lookup"><span data-stu-id="2e744-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="2e744-123">Если строка была выделена библиотеки DLL, для этого параметра **xlbitDLLFree**и также необходимо реализовать в [xlAutoFree](xlautofree-xlautofree12.md) (если, возвращают **XLOPER**) или **xlAutoFree12** (если, возвращают **XLOPER12**).</span><span class="sxs-lookup"><span data-stu-id="2e744-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="2e744-124">Пример</span><span class="sxs-lookup"><span data-stu-id="2e744-124">Example</span></span>

 `\SAMPLES\GENERIC\GENERIC.C`
  
```cs
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 xAction)
{
    static XLOPER12 xInfo, xIntAction;
/*
** This code coerces the passed-in value to an integer. This is how the
** code determines what is being requested. If it receives a 1, it returns a
** string representing the long name. If it receives anything else, it
** returns a #VALUE! error.
*/
    Excel12f(xlCoerce, &xIntAction, 2, xAction, TempInt12(xltypeInt));
    if(xIntAction.val.w == 1) 
    {
        xInfo.xltype = xltypeStr;
        xInfo.val.str = L"\026Example Standalone DLL";
    }
    else 
    {
        xInfo.xltype = xltypeErr;
        xInfo.val.err = xlerrValue;
    }
// Word of caution - returning static XLOPERs/XLOPER12s is not thread safe
// for UDFs declared as thread safe. Use alternate memory allocation mechanisms.
    return (LPXLOPER12)&xInfo;
} 

```

## <a name="see-also"></a><span data-ttu-id="2e744-125">См. также</span><span class="sxs-lookup"><span data-stu-id="2e744-125">See also</span></span>



[<span data-ttu-id="2e744-126">Диспетчер надстроек и функции XLL интерфейса</span><span class="sxs-lookup"><span data-stu-id="2e744-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

