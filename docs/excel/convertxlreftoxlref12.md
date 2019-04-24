---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- Функция convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310992"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="c53f6-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="c53f6-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="c53f6-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c53f6-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c53f6-106">Функция Framework, которая пытается преобразовать **кслреф** в **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="c53f6-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="c53f6-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c53f6-107">Parameters</span></span>

 <span data-ttu-id="c53f6-108">_пксреф_ (**Лпкслреф**)</span><span class="sxs-lookup"><span data-stu-id="c53f6-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="c53f6-109">Указатель на исходную ссылочную структуру.</span><span class="sxs-lookup"><span data-stu-id="c53f6-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="c53f6-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="c53f6-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="c53f6-111">Указатель на целевую ссылочную структуру, в которую будет включено преобразованное значение.</span><span class="sxs-lookup"><span data-stu-id="c53f6-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c53f6-112">Значение свойства и возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c53f6-112">Property value/Return value</span></span>

 <span data-ttu-id="c53f6-113">**Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** .</span><span class="sxs-lookup"><span data-stu-id="c53f6-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c53f6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c53f6-114">Remarks</span></span>

<span data-ttu-id="c53f6-115">При условии, что переданный **кслреф** является допустимым, эта операция всегда должна быть успешной.</span><span class="sxs-lookup"><span data-stu-id="c53f6-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="c53f6-116">В отличие от этого, преобразование других способов из **XLREF12** в **кслреф**, выполняемое [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), завершается неудачей, если предоставленная ссылка относится к части листа Excel 2007, которая не поддерживается в более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="c53f6-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="c53f6-117">Пример</span><span class="sxs-lookup"><span data-stu-id="c53f6-117">Example</span></span>

 `\SAMPLES\FRAMEWRK\FRAMEWRK.C`
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxref, LPXLREF12 pxref12)
{
   if (pxref->rwLast >= pxref->rwFirst && pxref->colLast >= pxref->colFirst)
   {
      if (pxref->rwFirst >= 0 && pxref->colFirst >= 0)
      {
         pxref12->rwFirst = pxref->rwFirst;
         pxref12->rwLast = pxref->rwLast;
         pxref12->colFirst = pxref->colFirst;
         pxref12->colLast = pxref->colLast;
         return TRUE;
      }
   }
   return FALSE;
}
```

## <a name="see-also"></a><span data-ttu-id="c53f6-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c53f6-118">See also</span></span>



[<span data-ttu-id="c53f6-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="c53f6-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

