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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: f2830633482e5329d285907b610386b708c406a4
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807154"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция Framework, пытается выполнить преобразование **XLREF** в **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameters

 _pxRef_ (**LPXLREF**)
  
Указатель на структуру источника ссылки.
  
 _pxRef12_ (**LPXLREF12**)
  
Указатель на структуру ссылку конечного, в который преобразованное значение — для размещения.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

 **Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае. 
  
## <a name="remarks"></a>Замечания

При условии, что переданное **XLREF** является допустимым, эта операция всегда должна быть установлена. С другой стороны преобразования другим способом из **XLREF12** **XLREF**, выполненный [ConvertXLRef12ToXLRef](convertxlref12toxlref.md)не выполняется, если заданный ссылка на часть таблицу Excel 2007, который не поддерживается в более ранних версиях.
  
## <a name="example"></a>Пример

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

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

