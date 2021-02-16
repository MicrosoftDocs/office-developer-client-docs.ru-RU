---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- Функция xldefinebinaryname [excel 2007]
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
  
Используется для выделения постоянного хранилища для **XLtypeBigData** **XLOPER** /  **XLOPER12.** Данные с определенным двоичным именем сохраняются в книге и доступны по имени в любое время. Дополнительные сведения см. в подразданном "Binary Name Scope Limitation" (Ограничение области двоичных имен) в подраздах ["Известные проблемы" в разработке XLL для Excel.](known-issues-in-excel-xll-development.md)
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Параметры

 _pxName_ (**xltypeStr)**
  
Строка, указывая имя данных. На строку распространяются те же ограничения именования, что и на определенные имена.
  
 _pxData_ (**xltypeBigData)**
  
Структура bigdata, указывав данные, которые необходимо сохранить. При вызове этой функции член **lpbData** в структуре **bigdata** должен указать данные, для которых определяется имя, а член **cbData** должен содержать длину данных в bytes. 
  
Если аргумент  _pxData_ не указан (**xltypeMissing),** именованный выделение, заданное  _pxName,_ удаляется. 
  
## <a name="see-also"></a>См. также



[xlGetBinaryName](xlgetbinaryname.md)


[Функции API C, которые можно вызывать только из библиотеки DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Известные проблемы в разработке XLL для Excel](known-issues-in-excel-xll-development.md)

