---
title: FuncSum
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- FuncSum
keywords:
- функция funcsum [Excel 2007]
localization_priority: Normal
ms.assetid: 934192ef-8a89-4dbb-bd37-01e92ba24256
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 14db5812165812161cf7031f75338a981251dfd2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406943"
---
# <a name="funcsum"></a>FuncSum

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Пример функции таблицы, определяемой пользователем, которая принимает от 1 до 29 аргументов и вычисляет их сумму. Каждый аргумент может быть одним числом, диапазоном или массивом. При загрузке GENERIC.xll она регистрирует эту функцию, чтобы она была вызвана из таблицы. 
  
```cs
LPXLOPER12 WINAPI FuncSum(LPXLOPER12 px1, LPXLOPER12 px2, LPXLOPER12 px3,LPXLOPER12 px4, LPXLOPER12 px5, LPXLOPER12 px6, LPXLOPER12 px7,LPXLOPER12 px8, LPXLOPER12 px9, LPXLOPER12 px10, LPXLOPER12 px11,LPXLOPER12 px12, LPXLOPER12 px13, LPXLOPER12 px14, LPXLOPER12 px15,LPXLOPER12 px16, LPXLOPER12 px17, LPXLOPER12 px18, LPXLOPER12 px19,LPXLOPER12 px20, LPXLOPER12 px21, LPXLOPER12 px22, LPXLOPER12 px23,LPXLOPER12 px24, LPXLOPER12 px25, LPXLOPER12 px26, LPXLOPER12 px27,LPXLOPER12 px28, LPXLOPER12 px29);
```

## <a name="parameters"></a>Parameters

 _px1-px29_ **(LPXLOPER12)**
  
Указатели на **аргументы XLOPER12.** Функция принимает любой тип ввода, но кодируется только для работы с числами, литеральными массивами чисел и диапазонами, содержащими только цифры или пустые ячейки. Если предоставлено менее 29 аргументов, остальные аргументы будут предоставлены в **качестве xltypeMissing.**
  
## <a name="property-valuereturn-value"></a>Значение свойства и возвращаемое значение

(**LPXLOPER12 xltypeNum** или **xltypeErr**)
  
Сумма аргументов или #VALUE! если в списке предоставленных аргументов нет числовых данных или в ячейке в диапазоне или элементе массива.
  
### <a name="example"></a>Пример

См.  `\SAMPLES\GENERIC\GENERIC.C` исходный код этой функции. 
  
## <a name="see-also"></a>См. также



[Функции в универсальной библиотеке DLL](functions-in-the-generic-dll.md)

