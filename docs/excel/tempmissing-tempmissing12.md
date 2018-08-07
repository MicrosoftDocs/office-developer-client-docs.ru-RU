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
- функция tempmissing [excel 2007], функция TempMissing12 [Excel 2007]
localization_priority: Normal
ms.assetid: d9cb6afc-1fbb-45d6-88e5-84eba3af3c60
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: a6db2e1f2917ecd9361043577f4bf203b3267a5c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807330"
---
# <a name="tempmissingtempmissing12"></a>TempMissing/TempMissing12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** тип **xltypeMissing**.
  
```cs
LPXLOPER TempMissing(void);
LPXLOPER12 TempMissing12(void);
```

## <a name="parameters"></a>Параметры

Эта функция не получает никаких параметров.
  
## <a name="return-value"></a>������������ ��������

Возвращает указатель на **xltypeMissing** **XLOPER**/ **XLOPER12**.
  
## <a name="example"></a>Пример

В этом примере использует **TempMissing12** для предоставления трех отсутствующие аргументы, которые нужно **xlcWorkspace** , а затем **логическое** **значение FALSE,** чтобы отображать полосы прокрутки листа. Другие параметры рабочей области, которые не влияет на соответствуют первым трем аргументов. 
  
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

