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
ms.openlocfilehash: 1b725dc5151f1f088f2547a1ef82d322c8458b6e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810035"
---
# <a name="meid"></a>MEID

 
  
**Относится к**: Outlook 
  
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

