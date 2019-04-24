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
- Функция темпбул [Excel 2007], функция TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: c8c917f0004fe091413ea670f1cc562f1d701fa0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310355"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** , содержащую **логическое** **значение true** или **false**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Параметры

 _b_ (**int**)
  
Чтобы возвращать **значение false**, используйте значение 0; Используйте любое другое значение, чтобы возвратить **значение true**.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает объект **** **Boolean** кслтипебул, содержащий логическое значение, переданное в параметре. 
  
## <a name="example"></a>Пример

В примере ниже показано, как очистить строку состояния с помощью функции **TempBool12** . Временная память освобождается при вызове функции [Excel/Excel12f](excel-excel12f.md) . 
  
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

