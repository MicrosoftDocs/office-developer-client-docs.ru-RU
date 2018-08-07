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
- функция temperr [excel 2007], функция TempErr12 [Excel 2007]
localization_priority: Normal
ms.assetid: cf8c26b2-ca2b-4dda-a02d-0ccbeac19106
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 22c0ff1b8259fc0e5ee70edb06bb3db53781ff8c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807320"
---
# <a name="temperrtemperr12"></a>TempErr/TempErr12

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Функция библиотеки Framework, который создает временные **XLOPER**/ **XLOPER12** , содержащий ошибку лист Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Параметры

 _err_
  
Код ошибки желаемую или его литерала числовой эквивалент, как показано в следующей таблице.
  
|**Error**|**Код ошибки, определенных в XLCALL. H**|**Десятичный эквивалент**|
|:-----|:-----|:-----|
|#NULL  <br/> |**xlerrNull** <br/> |0  <br/> |
|#DIV/0!  <br/> |**xlerrDiv0** <br/> |7  <br/> |
|#VALUE!  <br/> |**xlerrValue** <br/> |15  <br/> |
|#REF!  <br/> |**xlerrRef** <br/> |23  <br/> |
|#NAME?  <br/> |**xlerrName** <br/> |29  <br/> |
|#NUM!  <br/> |**xlerrNum** <br/> |36  <br/> |
|#N/A  <br/> |**xlerrNA** <br/> |42  <br/> |
   
## <a name="return-value"></a>������������ ��������

Возвращает значение **xltypeBool** , содержащий код ошибки переданную. 
  
## <a name="example"></a>Пример

В этом примере используется функция **TempErr12** возвращает #VALUE! Ошибка в Excel. 
  
> [!NOTE]
> Функция библиотеки Framework **TempErr12** выделение памяти из внутреннего буфера, который обычно освобождается при вызове функции Framework **Excel12f** . Если в этом примере функция вызывается несколько раз без **Excel12f** вызов, утечка памяти. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

