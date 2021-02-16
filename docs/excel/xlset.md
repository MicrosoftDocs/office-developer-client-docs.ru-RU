---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- Функция xlset [excel 2007]
localization_priority: Normal
ms.assetid: 121e6212-0692-4430-97be-4792b53719bf
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 0912c1d40882933778d0df927ceb9de773063444
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404605"
---
# <a name="xlset"></a>xlSet

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Очень быстро помещает постоянные значения в ячейки или диапазоны. Дополнительные сведения см. в подразении "XlSet and Workbooks with Array Formulas" в подраздах "Известные проблемы в разработке [XLL для Excel".](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Параметры

_pxReference_ (**xltypeRef** или **xltypeSRef**)
  
Прямоугольная ссылка, описывающие целевую ячейку или ячейки. Ссылка должна описывать смежные ячейки, чтобы в **xltypeRef** было установлено `val.mref.lpmref->count` 1. 
  
_pxValue_
  
Значение или значения, которые необходимо поместить в ячейку или ячейки. Дополнительные сведения см. в разделе "Замечания".
  
## <a name="remarks"></a>Примечания

### <a name="pxvalue-argument"></a>Аргумент pxValue

_pxValue_ может быть значением или массивом. Если это значение, этим значением заполняется весь диапазон назначения. Если это массив (**xltypeMulti),** элементы массива помещаются в соответствующие расположения в прямоугольнике.
  
При использовании горизонтального массива для второго аргумента он дублируется вниз, чтобы заполнить весь прямоугольник. При использовании вертикального массива он дублируется вправо для заполнения всего прямоугольника. Если вы используете прямоугольный массив, который слишком мал для прямоугольного диапазона, в который вы хотите поместить его, этот диапазон заполнен **#N/A.**
  
Если целевой диапазон меньше, чем исходный массив, значения копируется в пределах целевого диапазона, а дополнительные данные игнорируются.
  
Чтобы очистить элемент конечного прямоугольника, используйте элемент массива типов **xltypeNil** в массиве источника. Чтобы очистить весь прямоугольник назначения, опустить второй аргумент. 
  
### <a name="restrictions"></a>Ограничения

**XLSet** нельзя отменить. Кроме того, он уничтожает все сведения об отмене, которые могли быть доступны ранее. 
  
**xlSet** может поместить в ячейки только константы, а не формулы. 
  
**xlSet** работает как функция, эквивалентная командам класса 3; то есть она доступна только в DLL, если DLL-объект вызван из объекта, макроса,  меню, панели  инструментов, сочетания клавиш  или кнопки "Выполнить" в диалоговом окне макроса (доступ к ней можно получить с помощью вкладки "Вид" на ленте, начиная с Excel 2007, и меню "Инструменты" в предыдущих версиях).  
  
## <a name="example"></a>Пример

В следующем примере заполняется значение B205:B206, переданное из макроса. В этом примере функции команды требуется аргумент, поэтому он будет работать, только если он вызван из листа макроса XLM или из модуля VBA с помощью метода **Application.Run.** 
  
`\SAMPLES\EXAMPLE\EXAMPLE.C`
  
```cs
short WINAPI xlSetExample(short int iVal)
{
   XLOPER12 xRef, xValue;
   xRef.xltype = xltypeSRef;
   xRef.val.sref.count = 1;
   xRef.val.sref.ref.rwFirst = 204;
   xRef.val.sref.ref.rwLast = 205;
   xRef.val.sref.ref.colFirst = 1;
   xRef.val.sref.ref.colLast = 1;
   xValue.xltype = xltypeInt;
   xValue.val.w = iVal;
   Excel12(xlSet, 0, 2, (LPXLOPER12)&xRef, (LPXLOPER12)&xValue);
   return 1;
}
```

## <a name="see-also"></a>См. также

- [xlCoerce](xlcoerce.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

