---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- функция funcsum [excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 0b991cf5cdae90522abc9512193ee556e4c6e6e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807263"
---
# <a name="funcsum"></a>FuncSum

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательских функция, которая принимает аргументы усечение и вычисляет их сумма. Каждый аргумент может быть единые номера, диапазон или массив. При загрузке GENERIC.xll регистрирует эту функцию, чтобы его можно вызывать из рабочего листа. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameters

 _px1 px29_ (**LPXLOPER12**)
  
Указатели на **XLOPER12** аргументов. Функция принимает любой тип ввода, но закодированные только для работы с номера, литерал массивы номера и диапазоны, содержащие только числа или пустые ячейки. Если не указано меньше 29 аргументов, оставшихся аргументов как **xltypeMissing**.
  
## <a name="property-valuereturn-value"></a>Значение свойства или возвращаемое значение

(**LPXLOPER12 xltypeNum** или **xltypeErr**)
  
Суммы аргументы или #VALUE! При наличии других символов, в списке заданный аргумент или в ячейку в диапазоне или элемент массива.
  
### <a name="example"></a>Пример

Просмотреть `\SAMPLES\GENERIC\GENERIC.C` исходный код для этой функции. 
  
## <a name="see-also"></a>См. также



[В универсальные библиотеки DLL](functions-in-the-generic-dll.md)

