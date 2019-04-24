---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- Функция ConvertXLRef12ToXLRef [Excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32311055"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="f9393-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="f9393-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="f9393-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="f9393-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="f9393-106">Пытается преобразовать **XLREF12** в **кслреф**.</span><span class="sxs-lookup"><span data-stu-id="f9393-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="f9393-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9393-107">Parameters</span></span>

 <span data-ttu-id="f9393-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="f9393-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="f9393-109">Указатель на исходную ссылочную структуру.</span><span class="sxs-lookup"><span data-stu-id="f9393-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="f9393-110">_пксреф_ (**Лпкслреф**)</span><span class="sxs-lookup"><span data-stu-id="f9393-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="f9393-111">Указатель на целевую ссылочную структуру, в которую будет включено преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="f9393-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="f9393-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="f9393-112">Property value/Return value</span></span>

 <span data-ttu-id="f9393-113">**Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="f9393-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="f9393-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9393-114">Remarks</span></span>

<span data-ttu-id="f9393-115">Преобразование из **XLREF12** в **кслреф** завершается с ошибкой, если предоставленная ссылка относится к части листа Excel 2007, которая не поддерживается в более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="f9393-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="f9393-116">Пример</span><span class="sxs-lookup"><span data-stu-id="f9393-116">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRef12ToXLRef(LPXLREF12 pxref12, LPXLREF pxref)
{
   if (pxref12->rwLast >= pxref12->rwFirst && pxref12->colLast >= pxref12->colFirst)
   {
      if (pxref12->rwFirst >=0 && pxref12->colFirst >= 0)
      {
         if (pxref12->rwLast < rwMaxO8 && pxref12->colLast < colMaxO8)
         {
            pxref->rwFirst = (WORD)pxref12->rwFirst;
            pxref->rwLast = (WORD)pxref12->rwLast;
            pxref->colFirst = (BYTE)pxref12->colFirst;
            pxref->colLast = (BYTE)pxref12->colLast;
            return TRUE;
         }
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="f9393-117">См. также</span><span class="sxs-lookup"><span data-stu-id="f9393-117">See also</span></span>



[<span data-ttu-id="f9393-118">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="f9393-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

