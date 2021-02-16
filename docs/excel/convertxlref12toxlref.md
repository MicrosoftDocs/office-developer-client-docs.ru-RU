---
title: ConvertXLRef12ToXLRef
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRef12ToXLRef
keywords:
- функция convertxlref12toxlref [excel 2007]
localization_priority: Normal
ms.assetid: b620ed21-73ef-489b-9c00-7be12bb41214
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432655"
---
# <a name="convertxlref12toxlref"></a><span data-ttu-id="af34a-104">ConvertXLRef12ToXLRef</span><span class="sxs-lookup"><span data-stu-id="af34a-104">ConvertXLRef12ToXLRef</span></span>

<span data-ttu-id="af34a-105">**Область применения:** Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="af34a-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="af34a-106">Пытается преобразовать **XLREF12 в** **XLREF.**</span><span class="sxs-lookup"><span data-stu-id="af34a-106">Tries to convert an **XLREF12** into an **XLREF**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a><span data-ttu-id="af34a-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="af34a-107">Parameters</span></span>

 <span data-ttu-id="af34a-108">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="af34a-108">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="af34a-109">Указатель на структуру ссылок на источник.</span><span class="sxs-lookup"><span data-stu-id="af34a-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="af34a-110">_pxRef_ (**LPXLREF)**</span><span class="sxs-lookup"><span data-stu-id="af34a-110">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="af34a-111">Указатель на целевую эталонную структуру, в которую необходимо поместить преобразованные значения.</span><span class="sxs-lookup"><span data-stu-id="af34a-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="af34a-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="af34a-112">Property value/Return value</span></span>

 <span data-ttu-id="af34a-113">**TRUE,** если преобразование успешно, в противном случае **FALSE.**</span><span class="sxs-lookup"><span data-stu-id="af34a-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="af34a-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="af34a-114">Remarks</span></span>

<span data-ttu-id="af34a-115">Преобразование **из XLREF12** в **XLREF** не происходит, если предоставленная ссылка ссылается на часть листа Excel 2007, который не поддерживается в предыдущих версиях.</span><span class="sxs-lookup"><span data-stu-id="af34a-115">The conversion from **XLREF12** to **XLREF** fails if the supplied reference refers to part of a Excel 2007 worksheet that is not supported in earlier versions.</span></span> 
  
## <a name="example"></a><span data-ttu-id="af34a-116">Пример</span><span class="sxs-lookup"><span data-stu-id="af34a-116">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="af34a-117">См. также</span><span class="sxs-lookup"><span data-stu-id="af34a-117">See also</span></span>



[<span data-ttu-id="af34a-118">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="af34a-118">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

