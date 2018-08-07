---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- функция xlgetbinaryname [excel 2007]
localization_priority: Normal
ms.assetid: 66af3f78-65b5-42e0-82f9-ffd639d41751
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: d2332967e798b43a350c0733cd7398e2a921add6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807355"
---
# <a name="xlgetbinaryname"></a>xlGetBinaryName

**Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для возврата дескриптор для данных, сохраненных с помощью [функции xlDefineBinaryName](xldefinebinaryname.md). Данные с заданным именем двоичные сохраняется вместе с книгой и может быть доступен по имени в любое время. Для получения дополнительных сведений см раздел «Имя ограничения области двоичный» [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Параметры

_pxRes_ (**xltypeBigData** или **xltypeErr**)
  
Не удалось получить Bigdata структура извлеченные данные или ошибка является данных или имя не определено. Если функция возвращает, **hdata** членом **XLOPER**/ **XLOPER12** содержит маркер для именованного данных.  _pxRes_ нужно освободить в вызове **xlFree** больше не требуется. 
  
_pxName_ (**xltypeStr**)
  
Строка, задающая имя данных.
  
## <a name="remarks"></a>Замечания

Microsoft Excel несет ответственность за памяти дескриптор, возвращенный в **hdata**. В Windows дескриптор — это глобальный дескриптор памяти (выделены функцией **GlobalAlloc** ). 
  
## <a name="see-also"></a>См. также

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

