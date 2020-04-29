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
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0a12052a93d030088feb548449955129ff5bdc0f
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432655"
---
# <a name="convertxlref12toxlref"></a>ConvertXLRef12ToXLRef

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пытается преобразовать **XLREF12** в **кслреф**.
  
```cs
BOOL ConvertXLRefToXLRef12(LPXLREF12 pxRef12, LPXLREF pxRef);
```

## <a name="parameters"></a>Параметры

 _pxRef12_ (**LPXLREF12**)
  
Указатель на исходную ссылочную структуру.
  
 _пксреф_ (**лпкслреф**)
  
Указатель на целевую ссылочную структуру, в которую будет включено преобразованное значение.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

 **Значение true** , если преобразование выполнено успешно, в противном случае — **значение false** . 
  
## <a name="remarks"></a>Примечания

Преобразование из **XLREF12** в **кслреф** завершается с ошибкой, если предоставленная ссылка относится к части листа Excel 2007, которая не поддерживается в более ранних версиях. 
  
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



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

