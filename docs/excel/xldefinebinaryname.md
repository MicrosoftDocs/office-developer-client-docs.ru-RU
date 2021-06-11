---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- функция xldefinebinaryname [Excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: 'Область применения: Excel 2013 | Office 2013 | Visual Studio'
ms.openlocfilehash: 3c7fc4f6b6fc7179c1ca84043895273b2781f8b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430254"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Область применения:** Excel 2013 | Office 2013 | Visual Studio 
  
Используется для выделения постоянного хранилища **для xltypeBigData** **XLOPER** /  **XLOPER12.** Данные с определенным двоичным именем сохраняются в книге и могут быть доступны по имени в любое время. Дополнительные сведения см. в "Двоичное ограничение области имен" в известных проблемах [Excel XLL Development.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parameters

 _pxName_ **(xltypeStr)**
  
Строка с указанием имени данных. Строка подвержена тем же ограничениям именования, что и определенные имена.
  
 _pxData_ **(xltypeBigData)**
  
Структура bigdata, указывая данные, которые будут храниться. При вызове этой функции член **lpbData** структуры **bigdata** должен указать на данные, для которых определяется имя, а член **cbData** должен содержать длину данных в bytes. 
  
Если аргумент  _pxData_ не указан **(xltypeMissing),** то указанное  _pxName_ выделено. 
  
## <a name="see-also"></a>См. также



[xlGetBinaryName](xlgetbinaryname.md)


[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Известные проблемы в Excel XLL](known-issues-in-excel-xll-development.md)

