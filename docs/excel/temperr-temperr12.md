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
- Функция темперр [Excel 2007], функция TempErr12 [Excel 2007]
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
  
Функция библиотеки Framework, которая создает временную структуру **XLOPER**/ **** , содержащую ошибку листа Microsoft Excel. 
  
```cs
LPXLOPER TempErr(WORD err);
LPXLOPER12 TempErr12(BOOL err);
```

## <a name="parameters"></a>Параметры

 _err_
  
Необходимый код ошибки или его литеральный числовой эквивалент, как показано в следующей таблице.
  
|**Ошибка**|**Код ошибки, определенный в XLCALL. Высоты**|**Эквивалент десятичного разделителя**|
|:-----|:-----|:-----|
|#NULL  <br/> |**Кслеррнулл** <br/> |нуль  <br/> |
|#ДЕЛ/0!  <br/> |**xlerrDiv0** <br/> |см  <br/> |
|#ЗНАЧ!  <br/> |**Кслеррвалуе** <br/> |15   <br/> |
|#ССЫЛКА!  <br/> |**Кслеррреф** <br/> |23  <br/> |
|#ИМЯ?  <br/> |**Кслеррнаме** <br/> |суммируемых  <br/> |
|#ЧИСЛО!  <br/> |**Кслеррнум** <br/> |36  <br/> |
|#Н/Д  <br/> |**Кслеррна** <br/> |42  <br/> |
   
## <a name="return-value"></a>Возвращаемое значение

Возвращает объект **кслтипебул** , содержащий код ошибки, который был передан. 
  
## <a name="example"></a>Пример

В этом примере функция **TempErr12** используется для возврата #VALUE! Ошибка в Excel. 
  
> [!NOTE]
> Функция библиотеки Framework **TempErr12** выделяет память из внутреннего буфера, который обычно освобождается при вызове функции **Excel12f** платформы. Если этот пример функции вызывается повторно без вызова **Excel12f** , происходит утечка памяти. 
  
 `\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
LPXLOPER WINAPI TempErrExample(void)
{
    return TempErr12(xlerrValue);
}
```

## <a name="see-also"></a>См. также



[Функции в библиотеке платформы](functions-in-the-framework-library.md)

