---
title: TempMissing/TempMissing12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempMissing
- TempMissing12
keywords:
- Функция темпмиссинг [Excel 2007], функция TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310495"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** типа **кслтипемиссинг**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких параметров.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель на **кслтипемиссинг** **XLOPER**/ ****.
  
## <a name="example"></a>Пример

В этом примере используется **TempMissing12** для предоставления трех отсутствующих аргументов **кслкворкспаце** , за которыми следует **логическое** **значение false** , чтобы отменить отображение полос прокрутки листа. Первые три аргумента соответствуют другим параметрам рабочей области, которые не затрагиваются. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempMissingExample(void)
{
   XLOPER12 xBool;
   xBool.xltype = xltypeBool;
   xBool.val.xbool = 0;
   Excel12f(xlcWorkspace, 0, 4, TempMissing12(), TempMissing12(),
      TempMissing12(), (LPXLOPER12)&xBool);
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

