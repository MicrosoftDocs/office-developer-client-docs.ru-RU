---
title: xlAddInManagerInfo/xlAddInManagerInfo12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlAddInManagerInfo
keywords:
- Функция xladdinmanagerinfo [excel 2007]
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
# <a name="xladdinmanagerinfoxladdinmanagerinfo12"></a><span data-ttu-id="b1cd4-104">xlAddInManagerInfo/xlAddInManagerInfo12</span><span class="sxs-lookup"><span data-stu-id="b1cd4-104">xlAddInManagerInfo/xlAddInManagerInfo12</span></span>

 <span data-ttu-id="b1cd4-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="b1cd4-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="b1cd4-106">Вызывается Microsoft Excel при первом вызове диспетчера надстройки в сеансе Excel.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-106">Called by Microsoft Excel when the Add-in Manager is invoked for the first time in an Excel session.</span></span> <span data-ttu-id="b1cd4-107">Эта функция используется для предоставления диспетчеру Add-In сведений о надстройки.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-107">This function is used to provide the Add-In Manager with information about your add-in.</span></span>
  
<span data-ttu-id="b1cd4-108">Excel 2007 и более поздних версий вызов **xlAddInManagerInfo12** в предпочтение **xlAddInManagerInfo,** если экспортируется с помощью XLL.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-108">Excel 2007 and later versions call **xlAddInManagerInfo12** in preference to **xlAddInManagerInfo** if exported by the XLL.</span></span> <span data-ttu-id="b1cd4-109">Функция **xlAddInManagerInfo12** должна работать так же, как **и xlAddInManagerInfo,** чтобы избежать различий в поведении XLL для конкретных версий.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-109">The **xlAddInManagerInfo12** function should work in the same way as **xlAddInManagerInfo** to avoid version-specific differences in the behavior of the XLL.</span></span> <span data-ttu-id="b1cd4-110">Excel ожидает, **что xlAddInManagerInfo12** возвратит тип данных **XLOPER12,** тогда как **xlAddInManagerInfo** должен возвращать **XLOPER.**</span><span class="sxs-lookup"><span data-stu-id="b1cd4-110">Excel expects **xlAddInManagerInfo12** to return an **XLOPER12** data type, whereas **xlAddInManagerInfo** should return an **XLOPER**.</span></span>
  
<span data-ttu-id="b1cd4-111">Функция **xlAddInManagerInfo12** не вызвана версиями Excel более ранних версий, чем Excel 2007, так как они не поддерживают **XLOPER12**.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-111">The **xlAddInManagerInfo12** function is not called by versions of Excel earlier than Excel 2007, as these do not support the **XLOPER12**.</span></span>
  
<span data-ttu-id="b1cd4-112">Excel не требует XLL для реализации и экспорта этих функций.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-112">Excel does not require an XLL to implement and export either of these functions.</span></span>
  
```cs
LPXLOPER WINAPI xlAddInManagerInfo(LPXLOPER pxAction);
LPXLOPER12 WINAPI xlAddInManagerInfo12(LPXLOPER12 pxAction);
```

## <a name="parameters"></a><span data-ttu-id="b1cd4-113">Параметры</span><span class="sxs-lookup"><span data-stu-id="b1cd4-113">Parameters</span></span>

 <span data-ttu-id="b1cd4-114">_pxAction:_ Указатель на числовые **XLOPER/XLOPER12** (**xltypeInt** или **xltypeNum).**</span><span class="sxs-lookup"><span data-stu-id="b1cd4-114">_pxAction:_ A pointer to a numeric **XLOPER/XLOPER12** (**xltypeInt** or **xltypeNum**).</span></span>
  
<span data-ttu-id="b1cd4-115">Запрашиваемая в Excel информация.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-115">The information that Excel is asking for.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="b1cd4-116">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="b1cd4-116">Property value/Return value</span></span>

<span data-ttu-id="b1cd4-117">Если  _pxAction_ имеет номер 1 или может быть принудичен к этому номеру, реализация этой функции должна возвращать строку, содержащую некоторые сведения о надстройке, как правило, ее имя и, возможно, номер версии.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-117">If  _pxAction_ is, or can be coerced to, the number 1, then your implementation of this function should return a string containing some information about the add-in, typically its name and perhaps a version number.</span></span> <span data-ttu-id="b1cd4-118">В противном случае он должен возвращать #VALUE!.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-118">Otherwise it should return #VALUE!.</span></span> 
  
<span data-ttu-id="b1cd4-119">Если строка не возвращается, Excel пытается преобразовать возвращенные значения в строку.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-119">If you do not return a string, Excel tries to convert the returned value to a string.</span></span>
  
## <a name="remarks"></a><span data-ttu-id="b1cd4-120">Примечания</span><span class="sxs-lookup"><span data-stu-id="b1cd4-120">Remarks</span></span>

<span data-ttu-id="b1cd4-121">Если возвращенная строка указывает на динамически выделенный буфер, необходимо убедиться, что в конечном итоге этот буфер будет освобожден.</span><span class="sxs-lookup"><span data-stu-id="b1cd4-121">If the returned string points to dynamically allocated buffer, you must make sure that this buffer is eventually freed.</span></span> <span data-ttu-id="b1cd4-122">Если строка была выделена Excel, для этого необходимо установить **параметр xlbitXLFree.**</span><span class="sxs-lookup"><span data-stu-id="b1cd4-122">If the string was allocated by Excel, you do this by setting **xlbitXLFree**.</span></span> <span data-ttu-id="b1cd4-123">Если строка была выделена DLL, для этого необходимо установить **xlbitDLLFree,** а также реализовать ее в [xlAutoFree](xlautofree-xlautofree12.md) (если возвращается **XLOPER)** или **xlAutoFree12** (если возвращается **XLOPER12).**</span><span class="sxs-lookup"><span data-stu-id="b1cd4-123">If the string was allocated by the DLL, you do this by setting **xlbitDLLFree**, and you must also implement in [xlAutoFree](xlautofree-xlautofree12.md) (if you are returning an **XLOPER**) or **xlAutoFree12** (if you are returning an **XLOPER12**).</span></span>
  
## <a name="example"></a><span data-ttu-id="b1cd4-124">Пример</span><span class="sxs-lookup"><span data-stu-id="b1cd4-124">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="b1cd4-125">См. также</span><span class="sxs-lookup"><span data-stu-id="b1cd4-125">See also</span></span>



[<span data-ttu-id="b1cd4-126">Функции диспетчера надстроек и интерфейса XLL</span><span class="sxs-lookup"><span data-stu-id="b1cd4-126">Add-in Manager and XLL Interface Functions</span></span>](add-in-manager-and-xll-interface-functions.md)

