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
- Функция tempnum12 [Excel 2007], функция Темпнум [Excel 2007]
localization_priority: Normal
ms.assetid: 5b74d618-db3a-4d84-bd17-4fee7ae3b51e
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: cabd44ab828a2cfe22253e9aaf12abf7b7709d69
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33426634"
---
# <a name="tempnumtempnum12"></a>TempNum/TempNum12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** , содержащую номер листа Microsoft Excel (значение Double 8 байт). 
  
```cs
LPXLOPER TempNum(double d);
LPXLOPER12 TempNum12(double d);
```

## <a name="parameters"></a>Параметры

 _d_ (**двойной**)
  
Предполагаемое значение. Обратите внимание, что в настоящее время в настоящее время не поддерживаются и округляются значения IEEE, которые округляются до нуля. Поддерживается отрицательная бесконечность.
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает числовое значение **кслтипенум** , которое содержит переданное значение или ноль, если переданное значение было вложенным в обычный. 
  
## <a name="example"></a>Пример

В этом примере функция **TempNum12** используется для передачи аргумента в **кслфжетворкспаце**.
  
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

