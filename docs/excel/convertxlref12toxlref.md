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
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 826428edb57eba9e17d601164aa8b4b797fc8929
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807147"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пытается преобразовать **XLREF12** в **XLREF**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Parameters

 _pxRef12_ (**LPXLREF12**)
  
Указатель на структуру источника ссылки.
  
 _pxRef_ (**LPXLREF**)
  
Указатель на структуру ссылку конечного, в который преобразованное значение — для размещения.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

 **Значение TRUE,** Если преобразование выполнено успешно, **значение FALSE** в противном случае. 
  
## <a name="remarks"></a>Замечания

Преобразование из **XLREF12** в **XLREF** не выполняется, если заданный ссылка на части листа Excel 2007, не поддерживаются в более ранних версиях. 
  
## <a name="example"></a>Пример

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

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

