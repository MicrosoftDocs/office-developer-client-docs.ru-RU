---
title: xlSheetNm
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSheetNm
keywords:
- функция xlsheetnm [excel 2007]
localization_priority: Normal
ms.assetid: bcb16207-5499-4474-b006-51ccde1002d7
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 815565d886b1aea203f6b3b9774325d6b534abd2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807376"
---
# <a name="xlsheetnm"></a>xlSheetNm

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает имя листа электронной таблицы или макрос из его идентификатор внутреннего листа, содержатся в внешней ссылки или имя активного листа, если передается внутреннюю ссылку.
  
```cs
Excel12(xlSheetNm, LPXLOPER12 pxRes, 1, LPXLOPER12 pxExtref);
```

## <a name="parameters"></a>Параметры

_pxExtref_ (**xltypeRef** или **xltypeSRef**)
  
Ссылка на лист, имя которого вы хотите.
  
При передаче внешняя ссылка (**xltypeRef**) должны содержать только идентификатор листа. Структуры данных, которые описывают ячеек на листе игнорируется, а не должна быть предоставлена. Если идентификатор нулевое значение, **xlSheetNm** возвращает имя активного листа. 
  
При передаче внутренних справочных (**xltypeSef**) **xlSheetNm** возвращает имя активного листа. 
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

Возвращает имя листа (**xltypeStr**) в виде `[Book1]Sheet1`.
  
## <a name="example"></a>Пример

Следующий пример отображает имя листа, из которой был вызван функцию. Функция работает правильно, только в том случае, если вызов выполняется из листа макросов во время выполнения команды макросов XLM. Это, так как он вызывает **xlcAlert**, который можно выполнить только команды, и он должен быть вызван из листа, а не диалоговое окно, меню или панели команд в порядке для **xlfCaller** возвращает ссылку на. 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSheetNmExample(void)
{
   XLOPER12 xRes, xSheetName;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlSheetNm, &xSheetName, 1, (LPXLOPER12)&xRes);
   Excel12(xlcAlert, 0, 1, (LPXLOPER12)&xSheetName);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xSheetName);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [xlSheetId](xlsheetid.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

