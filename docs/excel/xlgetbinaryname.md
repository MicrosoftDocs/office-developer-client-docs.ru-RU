---
title: xlGetBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlGetBinaryName
keywords:
- Функция кслжетбинаринаме [Excel 2007]
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
  
Используется для возврата дескриптора для данных, сохраненных [функцией кслдефинебинаринаме](xldefinebinaryname.md). Данные с определенным двоичным именем сохраняются вместе с книгой и могут быть доступны по имени в любое время. Дополнительные сведения см. в разделе "ограничения области двоичных имен [](known-issues-in-excel-xll-development.md)".
  
```cs
Excel12(xlGetBinaryName, LPXLOPER12 pxRes, 1, LPXLOPER12 pxName);
```

## <a name="parameters"></a>Параметры

_пксрес_ (**кслтипебигдата** или **кслтипирр**)
  
Структура Бигдата, указывающая извлеченные данные или ошибка — не удается получить данные или имя не определено. Когда функция возвращает значение, элемент **хдата** в элементе **XLOPER**/ **XLOPER12** содержит дескриптор для именованных данных.  _пксрес_ следует освобождать в вызове **кслфри** , когда он больше не требуется. 
  
_пкснаме_ (**кслтипестр**)
  
Строка, указывающая имя данных.
  
## <a name="remarks"></a>Примечания

Microsoft Excel владеет дескриптором памяти, возвращаемым в **хдата**. В Windows дескриптор является глобальным дескриптором памяти (выделенный функцией **глобалаллок** ). 
  
## <a name="see-also"></a>См. также

- [xlDefineBinaryName](xldefinebinaryname.md)
- [Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)

