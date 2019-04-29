---
title: MEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa8f18d9-691d-d0cc-a660-f15ea6cff6ce
description: 'Дата последнего изменения: 03 июля, 2012'
ms.openlocfilehash: a9aea0db700de9c82aa2a41a443ebf03da8ce9b3
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430310"
---
# <a name="meid"></a>MEID

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Идентификатор элемента Outlook. Он содержит идентификатор записи и другую важную информацию.
  
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

 _Абфлагс_
  
> Идентификатор записи (4 байта) для элемента Outlook. Дополнительные сведения об идентификаторах записей MAPI приведены в разделе **[EntryID](entryid.md)**. 
    
 _Muid_
  
> GUID, определяющий поставщика хранилища. Определение типа **мапиуид**можно найти в файле MAPIDEFS. h. 
    
 _нагляд_
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.
    
 _Лтидфлд_
  
> Долгосрочный идентификатор папки.
    
 _Лтидмсг_
  
> Долгосрочный идентификатор элемента Outlook.
    
## <a name="see-also"></a>См. также



[Сведения об API репликации](about-the-replication-api.md)
  
[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[LTID](ltid.md)
  
[Синхр](sync.md)
  
[UPMSG](upmsg.md)

