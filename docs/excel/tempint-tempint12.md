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
- функция tempint12 [Excel 2007], функция TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 16a2222dbc51ad9480dbd5941ca2ed13f65b55e2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33438752"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, которая создает временную **XLOPER** /  **XLOPER12** с набором. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Parameters

 _i_
  
Предназначенное значение в несколько раз. Обратите внимание, что integer **XLOPER** — это подписанный 16-битный (короткий int), в то время как integer **XLOPER12** — это подписанный 32-bit integer ([long] int). 
  
## <a name="return-value"></a>Возвращаемое значение

Возвращает **integer xltypeInt,** содержащий переданные значения. 
  
## <a name="example"></a>Пример

В этом примере используется **функция TempInt12,** чтобы передать аргумент **в xlfGetWorkspace.**
  
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

