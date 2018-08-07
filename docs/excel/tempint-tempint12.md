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
- функция tempint12 [excel 2007], функция TempInt [Excel 2007]
localization_priority: Normal
ms.assetid: 86d690b8-caca-450d-93f7-69ca4cd1a6e0
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: eb1dd9be0c0b20e533d9cd8202f8878c43b997be
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807329"
---
# <a name="tempinttempint12"></a>TempInt/TempInt12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащее целое число. 
  
```cs
LPXLOPER TempInt(short int i);
LPXLOPER12 TempInt12(int i);
```

## <a name="parameters"></a>Параметры

 _я_
  
Предполагаемая целое значение. Обратите внимание, что целое число **XLOPER** 16-разрядного целого числа со знаком (короткий int), тогда как **XLOPER12** целое число — 32-разрядная версия целого числа со знаком (int [длинный]). 
  
## <a name="return-value"></a>������������ ��������

Возвращает **xltypeInt** целое значение, переданное в. 
  
## <a name="example"></a>Пример

В этом примере используется функция **TempInt12** для передачи аргумента **xlfGetWorkspace**.
  
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

