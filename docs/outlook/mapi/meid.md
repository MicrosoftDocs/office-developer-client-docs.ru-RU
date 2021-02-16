---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Last modified: July 03, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430310"
---
# <a name="meid"></a>MEID

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Идентификатор элемента Outlook. Он содержит идентификатор записи и другую релевантную информацию.
  
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

## <a name="members"></a>Элементы

 _abFlags_
  
> 4-byte entry identifier for the Outlook item. Дополнительные сведения об идентификаторах записей MAPI см. в **[entryID.](entryid.md)** 
    
 _muid_
  
> GUID, идентифицирует поставщика магазина. Определение типа **MAPIUID** см. в mapidefs.h. 
    
 _placeholder_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _ltidFld_
  
> Долгосрочный ИД папки.
    
 _ltidMsg_
  
> Долгосрочный ИД элемента Outlook.
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[SYNC](sync.md)
  
[UPMSG](upmsg.md)

