---
title: xlSet
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlSet
keywords:
- функция xlset [Excel 2007]
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
  
Очень быстро помещает постоянные значения в ячейки или диапазоны. Дополнительные сведения см. в книге "xlSet и книги с формулами массива" в [журнале Known Issues in Excel XLL Development.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlSet, LPXLOPER12 pxRes, 2, LPXLOPER12 pxReference, LPXLOPER pxValue);
```

## <a name="parameters"></a>Parameters

_pxReference_ **(xltypeRef** или **xltypeSRef)**
  
Прямоугольная ссылка с описанием целевой ячейки или ячейки. Ссылка должна описывать соседние ячейки, чтобы в **xltypeRef** было `val.mref.lpmref->count` установлено 1. 
  
_pxValue_
  
Значение или значения, которые необходимо поместить в ячейку или ячейки. Дополнительные сведения см. в разделе "Замечания".
  
## <a name="remarks"></a>Примечания

### <a name="pxvalue-argument"></a>аргумент pxValue

_pxValue может_ быть значением или массивом. Если это значение, весь диапазон назначения заполняется этим значением. Если это массив **(xltypeMulti),** элементы массива помещаются в соответствующие расположения прямоугольника.
  
Если для второго аргумента используется горизонтальный массив, он дублируется вниз, чтобы заполнить весь прямоугольник. Если вы используете вертикальный массив, он дублируется правой для заполнения всего прямоугольника. Если вы используете прямоугольный массив и он слишком мал для прямоугольного диапазона, в который вы хотите поместить его, этот диапазон **#N/A.**
  
Если целевой диапазон меньше массива исходных данных, значения копируется до пределов целевого диапазона, а дополнительные данные игнорируются.
  
Чтобы очистить элемент прямоугольника назначения, используйте элемент **массива типа xltypeNil** в массиве источника. Чтобы очистить весь прямоугольник назначения, ограничь второй аргумент. 
  
### <a name="restrictions"></a>Ограничения

**xlSet** нельзя отменить. Кроме того, он уничтожает любые сведения об отменить, которые могли быть доступны ранее. 
  
**xlSet** может поместить в ячейки только константы, а не формулы. 
  
**xlSet** ведет себя как функция, эквивалентная классу 3; то есть она доступна только в DLL, когда DLL вызвана из объекта, макроса, меню, панели  инструментов, клавиши ярлыка  или кнопки **Выполнить** в диалоговом окне Макрос (доступ к нему можно получить из вкладки Просмотр на ленте, начиная с Excel 2007 г., и меню **Tools** в более ранних версиях). 
  
## <a name="example"></a>Пример

В следующем примере B205:B206 заполняется значение, переданное с макроса. Этот пример функции команды требует аргумента, поэтому он будет работать только в том случае, если он вызван с макрос XLM или из модуля VBA с помощью **метода Application.Run.** 
  
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

