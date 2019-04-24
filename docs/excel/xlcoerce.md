---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- Функция xlCoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303964"
---
# <a name="xlcoerce"></a>xlCoerce

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Преобразует один тип параметра ****/ **XLOPER12** в другой или ищет значения ячеек на листе. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Параметры

 _Пкссаурце_
  
Исходная ****/ **XLOPER12** , которую необходимо преобразовать. 
  
 _пксдесттипе_ (**кслтипеинт**)
  
(НеОбязательно). Битовая маска получаемых типов, которые вы готовы принять. Для указания нескольких возможных типов используйте оператор побитового **или** (|). Если этот аргумент опущен, ссылки на отдельные ячейки преобразуются в один из типов значений **кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **кслтипенил** (если ссылка на ячейку пустая) и ссылки на блоки ячейки преобразуются в **xltypeMulti**. Это делает **xlCoerce** самым удобным способом поиска значений ячеек. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает приведенное значение (**кслтипестр**, **кслтипенум**, **кслтипебул**, **кслтипирр**, **кслтипенил**или **xltypeMulti**).
  
## <a name="remarks"></a>Замечания

 **xlCoerce** не удается выполнить преобразование в **кслтипебигдата** или **кслтипефлов**. Передача типа **кслтипемиссинг** или **Кслтипенил** в качестве _пксдесттипе_ эквивалентна опущению аргумента. В некоторых случаях может возникнуть ошибка преобразования. Например, некоторые строки не могут быть преобразованы в числа, в то время как другие могут. 
  
Если массив или ссылка на несколько ячеек преобразуются в один тип значения, результатом будет значение верхней левой ячейки или элемента массива.
  
## <a name="example"></a>Пример

Приведенный ниже код можно найти в `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> Функция **кслкалерт** неявно пытается преобразовать аргумент в строку, чтобы шаг приведения, показанный здесь, мог быть удален, а **ксинт** можно передать напрямую в **кслкалерт**. Так как **кслкалерт** — командный макрос, этот код работает правильно только при вызове из листа макросов. 
  
```cs
short WINAPI xlCoerceExample(short iVal)
{
   XLOPER12 xStr, xInt, xDestType;
   xInt.xltype = xltypeInt;
   xInt.val.w = iVal;
   xDestType.xltype = xltypeInt;
   xDestType.val.w = xltypeStr;
   Excel12f(xlCoerce, &xStr, 2, (LPXLOPER12)&xInt, (LPXLOPER12)&xDestType);
   Excel12f(xlcAlert, 0, 1, (LPXLOPER12)&xStr);
   Excel12f(xlFree, 0, 1, (LPXLOPER12)&xStr);
   return 1;
}
```

## <a name="see-also"></a>См. также



[xlSet](xlset.md)


[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

