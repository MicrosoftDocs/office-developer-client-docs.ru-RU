---
title: LTID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 17a412ba-3f74-ba94-0ffa-01dae63fc157
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 4a60e2fe3a58e1d696ae9645e03ce8dde5340d9a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809663"
---
# <a name="ltid"></a>LTID

  
  
**Применимо к**: Outlook 
  
Универсальный длинный идентификатор термина объекта в хранилище Outlook.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct LTID 
{ 
    GUID guid; 
    BYTE globcnt[6]; 
    WORD wLevel; 
};
```

## <a name="members"></a>Элементы

 _Идентификатор GUID_
  
- [out] Идентификатор GUID сервера, создавшее этот объект.
    
 _globcnt_
  
- [out] 6-байтовое уникальный номер, идентифицирующий объекта в хранилище Outlook.
    
 _wLevel_
  
- [out] Уровень иерархии идентификатор записи для Exchange избранные общей папки.
    
## <a name="see-also"></a>См. также



[О репликации API](about-the-replication-api.md)
  
[О репликации конечного автомата](about-the-replication-state-machine.md)
  
[FEID](feid.md)

