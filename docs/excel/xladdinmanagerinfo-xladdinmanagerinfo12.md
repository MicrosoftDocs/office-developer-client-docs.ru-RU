---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- функция xladdinmanagerinfo [Excel 2007]
localization_priority: Normal
ms.assetid: 63a73cd2-6479-4233-ad68-93379f940717
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 66d2ac05b9603d6bb587a3898bde2545c1bb844a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407797"
---
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="c7d4f-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="c7d4f-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="c7d4f-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c7d4f-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c7d4f-106">Вызывается Microsoft Excel при первом вызове диспетчера надстройки в Excel сеансе.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="c7d4f-107">Эта функция используется для предоставления Add-In менеджеру сведений о вашей надстройки.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="c7d4f-108">Excel 2007 и более поздних версиях вызов **xlAddInManagerInfo12** в предпочтение **xlAddInManagerInfo,** если экспортируется XLL.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="c7d4f-109">Функция **xlAddInManagerInfo12** должна работать так же, как **xlAddInManagerInfo,** чтобы избежать различий в поведении XLL.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="c7d4f-110">Excel **xlAddInManagerInfo12** возвращает тип данных **XLOPER12,** в то время как **xlAddInManagerInfo** должен возвращать **XLOPER**.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="c7d4f-111">Функция **xlAddInManagerInfo12** не вызвана версиями Excel раньше Excel 2007 г., так как они не поддерживают **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="c7d4f-112">Excel XLL не требуется для реализации и экспорта этих функций.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="c7d4f-113">Parameters</span><span class="sxs-lookup"><span data-stu-id="c7d4f-113">Parameters</span></span>

 <span data-ttu-id="c7d4f-114">_pxAction:_ Указатель на числовые **XLOPER/XLOPER12** **(xltypeInt** или **xltypeNum).**</span><span class="sxs-lookup"><span data-stu-id="c7d4f-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="c7d4f-115">Сведения, которые Excel запрашивается.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c7d4f-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c7d4f-116">Property value/Return value</span></span>

<span data-ttu-id="c7d4f-117">Если  _pxAction_ является или может быть принужден к номеру 1, то при реализации этой функции должна быть возвращена строка, содержащая некоторые сведения о надстройке, как правило, ее имя и, возможно, номер версии.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="c7d4f-118">В противном случае он должен #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="c7d4f-119">Если строка не возвращается, Excel пытается преобразовать возвращенные значения в строку.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="c7d4f-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="c7d4f-120">Remarks</span></span>

<span data-ttu-id="c7d4f-121">Если возвращенная строка указывает на динамически выделенный буфер, необходимо убедиться, что этот буфер в конечном итоге будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="c7d4f-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="c7d4f-122">Если строка была выделена Excel, для этого необходимо установить **xlbitXLFree.**</span><span class="sxs-lookup"><span data-stu-id="c7d4f-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="c7d4f-123">Если строка была выделена DLL, для этого необходимо установить **xlbitDLLFree,** а также реализовать ее в [xlAutoFree](xlautofree-xlautofree12.md) (если вы возвращаете **XLOPER)** или **xlAutoFree12** (если вы возвращаете **XLOPER12).**</span><span class="sxs-lookup"><span data-stu-id="c7d4f-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="c7d4f-124">Пример</span><span class="sxs-lookup"><span data-stu-id="c7d4f-124">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c7d4f-125">См. также</span><span class="sxs-lookup"><span data-stu-id="c7d4f-125">See also</span></span>



[<span data-ttu-id="c7d4f-126">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="c7d4f-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

