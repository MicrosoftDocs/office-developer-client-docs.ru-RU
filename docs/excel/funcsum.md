---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- Функция функсум [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32304062"
---
# <a name="funcsum"></a>FuncSum

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Пример пользовательской функции листа, которая принимает от 1 до 29 аргументов и вычисляет их сумму. Каждый аргумент может быть одним числом, диапазоном или массивом. Когда GENERIC. XLL загружается, она регистрирует эту функцию, чтобы ее можно было вызывать из листа. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Параметры

 _PX1 — px29_ (**LPXLOPER12**)
  
Указатели на аргументы **XLOPER12** . Функция принимает любой тип входных данных, но кодируется только на числа, литеральные массивы чисел и диапазоны, содержащие только цифры или пустые ячейки. Если указано менее 29 аргументов, остальные аргументы предоставляются как **кслтипемиссинг**.
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

(**LPXLOPER12 кслтипенум** или **кслтипирр**)
  
Сумма аргументов или #VALUE! Если в указанном списке аргументов или в ячейке в диапазоне или элементе массива есть нечисловые значения.
  
### <a name="example"></a>Пример

Исходный `\SAMPLES\GENERIC\GENERIC.C` код для этой функции представлен в разделе. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

