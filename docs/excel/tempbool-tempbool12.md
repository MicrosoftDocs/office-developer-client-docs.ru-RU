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
- функция tempbool [excel 2007], функция TempBool12 [Excel 2007]
localization_priority: Normal
ms.assetid: 0cf1fa58-416f-4692-a2e3-422473c19492
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 30874e7b918d8cd780bef60b4b02de1319f0f9ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807323"
---
# <a name="tempbooltempbool12"></a>TempBool/TempBool12

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий **логическое** **значение TRUE** или **FALSE**.
  
```cs
LPXLOPER TempBool(int b);
LPXLOPER12 TempBool12(int b);
```

## <a name="parameters"></a>Parameters

 _b_ (**int**)
  
Используйте 0, чтобы возвратить **значение FALSE**; Используйте другое значение возвращало **значение TRUE**.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает **xltypeBool** **логическое** содержащий логическое значение, переданное в. 
  
## <a name="example"></a>Пример

В следующем примере функция **TempBool12** снимите флажок в строке состояния. Временные память освобождается при вызове функции [Excel/Excel12f](excel-excel12f.md) . 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short int WINAPI TempBoolExample(void)
{
    Excel12f(xlcMessage, 0, 1, TempBool12(0));
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке Framework](functions-in-the-framework-library.md)

