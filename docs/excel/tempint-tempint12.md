---
title: TempInt/TempInt12
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempInt
- TempInt12
keywords:
- Функция tempint12 [Excel 2007], функция Темпинт [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310481"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** , содержащую целое число. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Параметры

 _i_
  
Предполагаемое целое значение. Обратите внимание, что значение **XLOPER** — это 16-разрядное целое число со знаком (short int), а значение **XLOPER12** — это 32-разрядное целое число ([Long] int). 
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает целое число **кслтипеинт** , содержащее переданное значение. 
  
## <a name="example"></a>Пример

В этом примере функция **TempInt12** используется для передачи аргумента в **кслфжетворкспаце**.
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI TempIntExample(void)
{
    XLOPER12 xRes;
    Excel12f(xlfGetWorkspace, (LPXLOPER12)&xRes, 1, TempInt12(44));
    Excel12f(xlFree, 0, 1, (LPXLOPER12)&xRes);
    return 1;
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

