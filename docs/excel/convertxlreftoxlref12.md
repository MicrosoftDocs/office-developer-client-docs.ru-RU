---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- функция convertxlreftoxlref12 [excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807154"
---
# <a name="convertxlreftoxlref12"></a><span data-ttu-id="c6329-104">ConvertXLRefToXLRef12</span><span class="sxs-lookup"><span data-stu-id="c6329-104">ConvertXLRefToXLRef12</span></span>

<span data-ttu-id="c6329-105">**Относится к**: Excel 2013 | Office 2013 | Visual Studio</span><span class="sxs-lookup"><span data-stu-id="c6329-105">**Applies to**: Excel 2013 | Office 2013 | Visual Studio</span></span> 
  
<span data-ttu-id="c6329-106">Функция Framework, пытается выполнить преобразование **XLREF** в **XLREF12**.</span><span class="sxs-lookup"><span data-stu-id="c6329-106">Framework function that attempts to convert an **XLREF** into an **XLREF12**.</span></span>
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a><span data-ttu-id="c6329-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="c6329-107">Parameters</span></span>

 <span data-ttu-id="c6329-108">_pxRef_ (**LPXLREF**)</span><span class="sxs-lookup"><span data-stu-id="c6329-108">_pxRef_ (**LPXLREF**)</span></span>
  
<span data-ttu-id="c6329-109">Указатель на структуру источника ссылки.</span><span class="sxs-lookup"><span data-stu-id="c6329-109">Pointer to the source reference structure.</span></span>
  
 <span data-ttu-id="c6329-110">_pxRef12_ (**LPXLREF12**)</span><span class="sxs-lookup"><span data-stu-id="c6329-110">_pxRef12_ (**LPXLREF12**)</span></span>
  
<span data-ttu-id="c6329-111">Указатель на структуру ссылку конечного, в который преобразованное значение — для размещения.</span><span class="sxs-lookup"><span data-stu-id="c6329-111">Pointer to the target reference structure into which the converted value is to be placed.</span></span>
  
## <a name="property-valuereturn-value"></a><span data-ttu-id="c6329-112">Значение свойства или возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c6329-112">Property value/Return value</span></span>

 <span data-ttu-id="c6329-113">**Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае.</span><span class="sxs-lookup"><span data-stu-id="c6329-113">**TRUE** if the conversion succeeded, **FALSE** otherwise.</span></span> 
  
## <a name="remarks"></a><span data-ttu-id="c6329-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="c6329-114">Remarks</span></span>

<span data-ttu-id="c6329-115">При условии, что переданное **XLREF** является допустимым, эта операция всегда должна быть установлена.</span><span class="sxs-lookup"><span data-stu-id="c6329-115">Provided that the passed-in **XLREF** is valid, this operation should always be successful.</span></span> <span data-ttu-id="c6329-116">С другой стороны преобразования другим способом из **XLREF12** **XLREF**, выполненный [ConvertXLRef12ToXLRef](convertxlref12toxlref.md)не выполняется, если заданный ссылка на часть таблицу Excel 2007, который не поддерживается в более ранних версиях.</span><span class="sxs-lookup"><span data-stu-id="c6329-116">In contrast, conversion the other way from **XLREF12** to **XLREF**, performed by [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), fails if the supplied reference refers to part of an Excel 2007 worksheet that is not supported in earlier versions.</span></span>
  
## <a name="example"></a><span data-ttu-id="c6329-117">Пример</span><span class="sxs-lookup"><span data-stu-id="c6329-117">Example</span></span>

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

## <a name="see-also"></a><span data-ttu-id="c6329-118">См. также</span><span class="sxs-lookup"><span data-stu-id="c6329-118">See also</span></span>



[<span data-ttu-id="c6329-119">Функции в библиотеке платформы</span><span class="sxs-lookup"><span data-stu-id="c6329-119">Functions in the Framework Library</span></span>](functions-in-the-framework-library.md)

