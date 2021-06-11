---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- функция xlfcaller [Excel 2007]
localization_priority: Normal
ms.assetid: de4b119c-ae2e-4207-9783-8d5692a4d052
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: fb788375504cefab75fde9513147c1d54acdaa07
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33405732"
---
# <a name="xlfcaller"></a>xlfCaller

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Возвращает сведения о ячейке, диапазоне ячеек, команде в меню, инструменте на панели инструментов или объекте, который называется командой или функцией DLL, которая в настоящее время запущена.
  
|**Код, отозвался**|**Возвращаемое значение**|
|:-----|:-----|
|DLL  <br/> |ID регистра.  <br/> |
|Одна ячейка  <br/> |Одноклеточная ссылка.  <br/> |
|Формула многоклеточного массива  <br/> |Многоклеточная ссылка.  <br/> |
|Условное выражение форматирования  <br/> |Ссылка на ячейку, к которой применяется условие форматирования.  <br/> |
|Меню  <br/> | Массив однорядного массива из четырех элементов:  <br/>  Код панели.  <br/>  Положение меню.  <br/>  Положение submenu.  <br/>  Положение команды.  <br/> |
|Панель инструментов  <br/> | Двухэлементный однорядный массив:  <br/>  Номер панели инструментов для встроенных панели инструментов или имя панели инструментов для настраиваемой панели инструментов.  <br/>  Положение на панели инструментов.  <br/> |
|Графический объект  <br/> |Идентификатор объекта (имя объекта).  <br/> |
|Команда, связанная с xlcOnEnter, ON. ENTER, ловушка событий  <br/> |Ссылка на вступаемую ячейку или ячейки.  <br/> |
|Команда, связанная с xlcOnDoubleclick, ON. DOUBLECLICK, ловушка событий.  <br/> |Ячейка, дважды щелкнув ее (не обязательно активная ячейка).  <br/> |
|Auto_Open, autoClose, Auto_Activate или Auto_Deactivate макроса  <br/> |Имя листа вызова.  <br/> |
|Другие методы, не перечисленные  <br/> |#ССЫЛКА! Ошибка  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращаемого значения является одним из следующих типов данных **XLOPER** /  **XLOPER12:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr**, или **xltypeMulti**. Так как три из этих типов указывают на выделенную память, возвращаемое значение **xlfCaller** всегда должно быть освобождено при вызове функции [xlFree,](xlfree.md) когда она больше не требуется. 
  
Дополнительные сведения о **XLOPERs** /  **XLOPER12 см.** в Excel. [](memory-management-in-excel.md)
  
## <a name="remarks"></a>Примечания

Эта функция является единственной функцией, которая не имеет таблицы, которая может быть вызвана из функции таблицы DLL/XLL. Другие функции XLM-информации могут быть вызваны только из команд или эквивалентных функций макрос листа.
  
## <a name="example"></a>Пример

 `\SAMPLES\EXAMPLE\EXAMPLE.C`. Эта функция вызывает макрос команды (xlcSelect) и будет правильно работать только при вызове с листа макроса.
  
```cs
short WINAPI CallerExample(void)
{
   XLOPER12 xRes;
   Excel12(xlfCaller, &xRes, 0);
   Excel12(xlcSelect, 0, 1, (LPXLOPER12)&xRes);
   Excel12(xlFree, 0, 1, (LPXLOPER12)&xRes);
   return 1;
}
```

## <a name="see-also"></a>См. также



[Необходимые и полезные функции XLM из API C](essential-and-useful-c-api-xlm-functions.md)

