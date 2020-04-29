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
  
Функция Framework, которая пытается преобразовать **кслреф** в **XLREF12**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF pxRef, LPXLREF12 pxRef12);
```

## <a name="parameters"></a>Параметры

 _пксреф_ (**лпкслреф**)
  
Указатель на исходную ссылочную структуру.
  
 _pxRef12_ (**LPXLREF12**)
  
Указатель на целевую ссылочную структуру, в которую будет включено преобразованное значение.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** . 
  
## <a name="remarks"></a>Примечания

При условии, что переданный **кслреф** является допустимым, эта операция всегда должна быть успешной. В отличие от этого, преобразование других способов из **XLREF12** в **кслреф**, выполняемое [ConvertXLRef12ToXLRef](convertxlref12toxlref.md), завершается неудачей, если предоставленная ссылка относится к части листа Excel 2007, которая не поддерживается в более ранних версиях.
  
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

