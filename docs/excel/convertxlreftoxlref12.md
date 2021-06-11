---
title: ConvertXLRefToXLRef12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- ConvertXLRefToXLRef12
keywords:
- функция convertxlreftoxlref12 [Excel 2007]
localization_priority: Normal
ms.assetid: 94580044-9497-425f-a31e-53bb4d94dc30
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 530cb9cce5b0023318ff6b8a0ff73472f8250aa3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432032"
---
# <a name="convertxlreftoxlref12"></a>ConvertXLRefToXLRef12

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция Framework, которая пытается преобразовать **XLREF** в **XLREF12.**
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Parameters

 _pxRef_ **(LPXLREF)**
  
Указатель на структуру исходных ссылок.
  
 _pxRef12_ **(LPXLREF12)**
  
Указатель на целевую справочную структуру, в которую должно быть помещено преобразовано значение.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **TRUE,** если преобразование удалось, **FALSE** в противном случае. 
  
## <a name="remarks"></a>Примечания

При условии, что переданный **XLREF** является допустимым, эта операция всегда должна быть успешной. Напротив, преобразование в **XLREF12** в **XLREF,** выполненное [ConvertXLRef12ToXLRef,](convertxlref12toxlref.md)не выполняется, если предоставленная ссылка относится к части таблицы Excel 2007 г., которая не поддерживается в предыдущих версиях.
  
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



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

