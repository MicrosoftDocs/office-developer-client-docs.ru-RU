---
title: TempBool/TempBool12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempBool
- TempBool12
keywords:
- функция tempbool [Excel 2007], функция TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433719"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную **XLOPER** /  **XLOPER12, содержащую** **Boolean** **TRUE** или **FALSE.**
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parameters

 _b_ **(int)**
  
Использование 0 для возврата **FALSE;** используйте любое другое значение для возврата **TRUE.**
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает **xltypeBool** **Boolean,** содержащее логическое значение, переданного в. 
  
## <a name="example"></a>Пример

В следующем примере для очистки панели состояния используется функция **TempBool12.** Временная память будет освобождена [при Excel/Excel12f.](excel-excel12f.md) 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

