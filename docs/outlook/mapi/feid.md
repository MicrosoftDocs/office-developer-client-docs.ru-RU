---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Last modified: July 02, 2012'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409813"
---
# <a name="feid"></a>FEID

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Идентификатор папки. Он содержит идентификатор записи и другую релевантную информацию.
  
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

## <a name="members"></a>Элементы

 _abFlags_
  
> 4-byte entry identifier for the folder. Дополнительные сведения об идентификаторах записей MAPI см. в **[entryID.](entryid.md)** 
    
 _muid_
  
> GUID, идентифицирует поставщика магазина. Определение типа **MAPIUID** см. в mapidefs.h. 
    
 _placeholder_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _ltid_
  
> Долгосрочный ИД папки.
    
## <a name="see-also"></a>См. также



[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[SYNC](sync.md)

