---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Последнее изменение: 03 июля 2012 г.'
ms.openlocfilehash: 24cc4b00f02c61395565fb7ddeb6a5b5a62afdc5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591942"
---
# <a name="meid"></a>MEID

 
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Идентификатор элемента Outlook. Он содержит идентификатор входа и другие необходимые сведения.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
struct MEID 
{ 
    BYTE abFlags[4]; 
    MAPIUID muid; 
    WORD placeholder; 
    LTID ltidFld; 
    LTID ltidMsg; 
};
```

## <a name="members"></a>Members

 _abFlags_
  
> Идентификатор записи 4-байтных для элемента Outlook. Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, идентифицирующий поставщика хранилища. В разделе mapidefs.h для определения типа **MAPIUID**. 
    
 _заполнитель_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _ltidFld_
  
> Долгосрочные идентификатор папки.
    
 _ltidMsg_
  
> Долгосрочные идентификатор элемента Outlook.
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

