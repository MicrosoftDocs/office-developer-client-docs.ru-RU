---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Функция кслдефинебинаринаме [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Относится к: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32310215"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Относится к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для выделения постоянного хранилища для **кслтипебигдата** **XLOPER**/ ****. Данные с определенным двоичным именем сохраняются вместе с книгой и могут быть доступны по имени в любое время. Дополнительные сведения см. в разделе "ограничения области двоичных имен [](known-issues-in-excel-xll-development.md)".
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Параметры

 _пкснаме_ (**кслтипестр**)
  
Строка, указывающая имя данных. В этой строке действуют те же ограничения именования, что и в определенных именах.
  
 _пксдата_ (**кслтипебигдата**)
  
Структура Бигдата, указывающая сохраняемые данные. При вызове этой функции элемент **лпбдата** структуры **бигдата** должен указать данные, для которых определяется имя, а элемент **КБДата** должен содержать длину данных в байтах. 
  
Если аргумент _пксдата_ не указан (**кслтипемиссинг**), удаляется именованное выделение, указанное с помощью _пкснаме_ . 
  
## <a name="see-also"></a>См. также



[xlGetBinaryName](xlgetbinaryname.md)


[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Известные проблемы разработки XLL в Excel](known-issues-in-excel-xll-development.md)

