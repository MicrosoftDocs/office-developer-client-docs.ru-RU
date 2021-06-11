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
- функция tempmissing [Excel 2007], функция TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 37c127b2252f18643b34dfc72fd9929885a68d01
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435959"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки framework, которая создает временную **XLOPER** /  **XLOPER12** типа **xltypeMissing.**
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Parameters

Эта функция не получает никаких параметров.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает указатель **xltypeMissing** **XLOPER** /  **XLOPER12.**
  
## <a name="example"></a>Пример

В этом примере **tempMissing12** предоставляет **xlcWorkspace** три отсутствующих аргумента, за которыми следует false **Boolean**  для подавления отображения столбцов прокрутки таблицы. Первые три аргумента соответствуют другим параметрам рабочего пространства, которые не имеют изменений. 
  
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

