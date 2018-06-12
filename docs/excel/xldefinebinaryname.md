---
title: xlDefineBinaryName
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
f1_keywords:
- xlDefineBinaryName
keywords:
- функция xlDefineBinaryName [excel 2007]
localization_priority: Normal
ms.assetid: e3e8f91b-cc31-4f09-9941-f950ae96820a
description: '������� ����������: Excel 2013�| Office 2013�| Visual Studio'
ms.openlocfilehash: 14515cc262ea398a9f200c0de3a1f6b64c758b3d
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807339"
---
# <a name="xldefinebinaryname"></a>xlDefineBinaryName

 **Применимо к**: Excel 2013 | Office 2013 | Visual Studio 
  
Используется для выделения постоянное хранилище для **xltypeBigData** **XLOPER**/ **XLOPER12**. Данные с заданным именем двоичные сохраняется вместе с книгой и может осуществляться по имени в любое время. Для получения дополнительных сведений см «двоичный имя области» в разделе [Известные проблемы при разработке XLL для Excel](known-issues-in-excel-xll-development.md).
  
```cs
Excel12(xlDefineBinaryName, 0, 2, LPXLOPER12 pxName, LPXLOPER12 pxData);
```

## <a name="parameters"></a>Parameters

 _pxName_ (**xltypeStr**)
  
Строка, задающая имя данных. Строка — это может быть таким же ограничения именования следующим определенных имен.
  
 _pxData_ (**xltypeBigData**)
  
Bigdata структура данных для хранения. При вызове этой функции должны указывать член **lpbData** **bigdata** структуры данных, для которого определяется имя и член **cbData** должен содержать длина данных в байтах. 
  
Если аргумент _pxData_ не указанного (**xltypeMissing**), именованные распределения, указанного идентификатором _pxName_ будет удален. 
  
## <a name="see-also"></a>См. также



[xlGetBinaryName](xlgetbinaryname.md)


[Функции интерфейса API для C, которые могут вызываться только из DLL или XLL](c-api-functions-that-can-be-called-only-from-a-dll-or-xll.md)
  
[Известные проблемы, возникающие при разработке XLL для Excel](known-issues-in-excel-xll-development.md)

