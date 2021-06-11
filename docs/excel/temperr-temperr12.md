---
title: TempErr/TempErr12
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- TempErr
- TempErr12
keywords:
- функция темпера [Excel 2007], функция TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 68a0addc36ecf1b4491ab1e4f5b10f359bbc59c3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33410611"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки framework, которая создает временную **XLOPER** /  **XLOPER12,** содержащую ошибку Microsoft Excel таблицы. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Parameters

 _err_
  
Желаемый код ошибки или его литеральный числовый эквивалент, как показано в следующей таблице.
  
|**Ошибка**|**Код ошибки, определенный в XLCALL. H**|**Десятичной эквивалент**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#ДЕЛ/0!  <br/> |**xlerrDiv0** <br/> |7   <br/> |
|#ЗНАЧ!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#ССЫЛКА!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#ИМЯ?  <br/> |**xlerrName** <br/> |29  <br/> |
|#ЧИСЛО!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#Н/Д  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Возвращает **xltypeBool,** содержащий переданный код ошибки. 
  
## <a name="example"></a>Пример

В этом примере **используется функция TempErr12** для возврата #VALUE! ошибка Excel. 
  
> [!NOTE]
> Функция библиотеки Framework **TempErr12** выделяет память из внутреннего буфера, который обычно освобожден при назвав функцию **Framework Excel12f.** Если эта функция в примере называется несколько раз без призыва **Excel12f,** происходит утечка памяти. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

