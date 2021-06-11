---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- функция xlcoerce [Excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d84839535d5eb913ca8a62d631238e3330683d0e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424835"
---
# <a name="xlcoerce"></a>xlCoerce

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Преобразует один тип **XLOPER** /  **XLOPER12 в** другой или ищет значения ячейки на листе. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameters

 _pxSource_
  
Источник **XLOPER** /  **XLOPER12,** который необходимо преобразовать. 
  
 _pxDestType_ **(xltypeInt)**
  
(Необязательный). Бит-маска из типов, которые вы готовы принять. Для указания нескольких возможных типов следует использовать оператор **bitwise OR** (|). Если этот аргумент опущен, ссылки на отдельные ячейки преобразуются в один из типов значений **xltypeStr,** **xltypeNum,** **xltypeBool,** **xltypeErr,** **xltypeNil** (если ссылаемая ячейка пуста), а ссылки на блоки клеток преобразуются в **xltypeMulti**. Это делает **xlCoerce** наиболее удобным способом для наблюдения за значениями ячейки. 
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращает принудительное значение **(xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**, или **xltypeMulti**).
  
## <a name="remarks"></a>Примечания

 **xlCoerce не может** преобразовать в **xltypeBigData** или **xltypeFlow.** Передача **типа xltypeMissing** или **xltypeNil** в  _качестве pxDestType_ эквивалентна опущению аргумента. В некоторых случаях преобразование может привести к сбойу. Например, некоторые строки не могут быть преобразованы в числа, в то время как другие могут. 
  
Если массив или многоклеточная ссылка преобразуется в один тип значения, результатом является значение верхнего левого элемента или элемента массива.
  
## <a name="example"></a>Пример

Следующий код можно найти в  `\SAMPLES\EXAMPLE\EXAMPLE.C` . 
  
> [!NOTE]
> Функция **xlcAlert** неявно пытается преобразовать аргумент в строку, чтобы показанный здесь шаг принуждения мог быть удален, а **xInt** можно передать непосредственно **в xlcAlert.** Поскольку **xlcAlert** — это макрос команды, этот код работает правильно только при названии с макроса. 
  
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

