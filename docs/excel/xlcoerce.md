---
title: xlCoerce
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlCoerce
keywords:
- функция xlCoerce [excel 2007]
localization_priority: Normal
ms.assetid: 9d47c16c-a7e7-4998-b594-9cf001827b7b
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: e0474b81a6d24663fe85303efc8fe2fd62cfdd82
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807353"
---
# <a name="xlcoerce"></a>xlCoerce

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Преобразует один тип **XLOPER**/ **XLOPER12** в другую или ищет значений ячеек на листе. 
  
```cs
Excel12(xlCoerce, LPXLOPER12 pxRes, 2, LPXLOPER12 pxSource, LPXLOPER12 pxDestType);
```

## <a name="parameters"></a>Parameters

 _pxSource_
  
Источник **XLOPER**/ **XLOPER12** , которую требуется преобразовать. 
  
 _pxDestType_ (**xltypeInt**)
  
(Необязательно). Битовая маска итоговый типов вы готовы для приема. Чтобы указать несколько возможных типов следует использовать битовый оператор **или** (|). Если этот аргумент задан, ссылки на одну ячейку преобразуются в один из типов значение **xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil** (если ссылка на ячейку пуст) и ссылки на блоки ячеек преобразуются в **xltypeMulti**. Это делает **xlCoerce** самый удобный способ поиска значений ячеек. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает приведенное значение (**xltypeStr**, **xltypeNum**, **xltypeBool**, **xltypeErr**, **xltypeNil**или **xltypeMulti**).
  
## <a name="remarks"></a>Замечания

 **xlCoerce** невозможно преобразовать в или из **xltypeBigData** или **xltypeFlow**. Передача типа **xltypeMissing** или **xltypeNil** в качестве _pxDestType_ эквивалентно пропуска аргумента. Преобразование может не работать в некоторых случаях. Например некоторые строки невозможно преобразовать на номера, в то время как другие пользователи могут. 
  
Если массив или ссылка на ячейку несколькими преобразуется в тип одного значения, результатом является значение элемента верхней левой ячейки или массива.
  
## <a name="example"></a>Пример

Следующий код можно найти в `\SAMPLES\EXAMPLE\EXAMPLE.C`. 
  
> [!NOTE]
> Функция **xlcAlert** неявно пытается преобразовать аргумента в строку, чтобы шаг приведения, показанный фактически удаляется, а **xInt** может быть передан непосредственно к **xlcAlert**. Как и **xlcAlert** команда макрос, этот код только работает правильно при вызове из листа макросов. 
  
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



[функция xlSet](xlset.md)


[Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

