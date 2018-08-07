---
title: TempNum/TempNum12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempNum
- TempNum12
keywords:
- функция tempnum12 [excel 2007], функция TempNum [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 5ebe58dba32c2cf0382bf0811713eaa0a5471dda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807326"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащее число лист Microsoft Excel (IEEE double 8 байтов). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Параметры

 _d_ (**double**)
  
Целевое значение. Обратите внимание, что IEEE вложенных обычных чисел в настоящее время не поддерживается округляются до нуля. Отрицательное infinity поддерживается.
  
## <a name="return-value"></a>������������ ��������

Возвращает числовое **xltypeNum** , содержащая значение переданного или ноль, если переданное значение было вложенных обычный. 
  
## <a name="example"></a>Пример

В этом примере используется функция **TempNum12** для передачи аргумента **xlfGetWorkspace**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempNumExample(void)
{
   XLOPER12 xRes;
   Excel12f(xlfGetWorkspace, &xRes, 1, TempNum12(44));
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

