---
title: xlfCaller
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlfCaller
keywords:
- Функция xlfcaller [excel 2007]
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
  
Возвращает сведения о ячейке, диапазоне ячеек, команде в меню, средстве на панели инструментов или объекте, который вызвал команду или функцию DLL, которая в настоящее время запущена.
  
|**Код, который вызван из**|**Возвращаемое значение**|
|:-----|:-----|
|DLL  <br/> |ИД регистрации.  <br/> |
|Одна ячейка  <br/> |Ссылка на одну ячейку.  <br/> |
|Формула массива с несколькими ячейками  <br/> |Справочник по нескольким ячейкам.  <br/> |
|Выражение условного форматирования  <br/> |Ссылка на ячейку, к которой применяется условие форматирования.  <br/> |
|Меню  <br/> | Массив из четырех элементов из одной строки:  <br/>  ИД панели.  <br/>  Позиция меню.  <br/>  Положение подменю.  <br/>  Положение команды.  <br/> |
|Панель инструментов  <br/> | Массив из двух элементов с одной строкой:  <br/>  Номер панели инструментов для встроенных панели инструментов или имя панели инструментов для настраиваемой панели инструментов.  <br/>  Положение на панели инструментов.  <br/> |
|Графический объект  <br/> |Идентификатор объекта (имя объекта).  <br/> |
|Команда, связанная с xlcOnEnter, ON. ВВОД, схимя событий  <br/> |Ссылка на в введенную ячейку или ячейки.  <br/> |
|Команда, связанная с xlcOnDoubleclick, ON. DOUBLECLICK, ловушек событий.  <br/> |Ячейка, которая была дважды щелкнуть (не обязательно активная ячейка).  <br/> |
|Auto_Open, autoClose, Auto_Activate или Auto_Deactivate макроса  <br/> |Имя вызываемой таблицы.  <br/> |
|Другие методы, не перечисленные  <br/> |#ССЫЛКА! Ошибка  <br/> |
   
```cs
Excel12(xlfCaller, (LPXLOPER12) pxRes,0);
```

## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

Возвращаемого значения является одним из следующих типов данных **XLOPER** /  **XLOPER12:** **xltypeRef**, **xltypeSRef**, **xltypeNum**, **xltypeStr**, **xltypeErr** или **xltypeMulti**. Так как три из этих типов указывают на выделенную память, возвращаемое значение **xlfCaller** всегда должно быть освобождено при вызове функции [xlFree,](xlfree.md) когда она больше не требуется. 
  
Дополнительные сведения об **XLOPERs** /  **XLOPER12 см.** в руководстве по управлению [памятью в Excel.](memory-management-in-excel.md)
  
## <a name="remarks"></a>Примечания

Эта функция является единственной функцией, не относякойся к таблицам, которая может быть вызвана из функции таблицы DLL/XLL. Другие информационные функции XLM могут быть вызваны только из команд или эквивалентных функций листа макроса.
  
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

