---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- функция xlgetbinaryname [Excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 6d063213e3f83451e8a072e71f0878174214f73e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412466"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для возврата ручки для данных, сохраненных функцией [xlDefineBinaryName.](xldefinebinaryname.md) Данные с определенным двоичным именем сохраняются в книге и могут быть доступны по имени в любое время. Дополнительные сведения см. в "Двоичное ограничение области имен" в известных проблемах [Excel XLL Development.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Parameters

_pxRes_ **(xltypeBigData** или **xltypeErr)**
  
Структура bigdata, указывавая извлеченные данные или ошибка, — данные не могут быть извлечены или имя не определено. Когда функция возвращается, член **hdata** **XLOPER XLOPER12** содержит ручку /   для названных данных.  _pxRes_ следует освободить при вызове **на xlFree,** если это больше не требуется. 
  
_pxName_ **(xltypeStr)**
  
Строка с указанием имени данных.
  
## <a name="remarks"></a>Примечания

Microsoft Excel владеет возвращенной в hdata ручкой **памяти.** В Windows, ручка является глобальной ручкой памяти (выделенной функцией **GlobalAlloc).** 
  
## <a name="see-also"></a>См. также

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

