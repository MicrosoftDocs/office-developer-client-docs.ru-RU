---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Последнее изменение: 2 июля 2012.'
ms.openlocfilehash: 3e534f91863e2a1300e03d112d1f532f486eedd9
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22588309"
---
# <a name="feid"></a>FEID

 
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Идентификатор для папки. Он содержит идентификатор входа и другие необходимые сведения.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct FEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltid; 
};
```

## <a name="members"></a>Members

 _abFlags_
  
> Идентификатор записи 4-байтных папки. Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, идентифицирующий поставщика хранилища. В разделе mapidefs.h для определения типа **MAPIUID**. 
    
 _заполнитель_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _ltid_
  
> Долгосрочные идентификатор папки.
    
## <a name="see-also"></a>См. также



[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

