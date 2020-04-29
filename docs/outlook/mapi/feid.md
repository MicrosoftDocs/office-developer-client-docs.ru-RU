---
title: FEID
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dde7eec-df3d-723c-db08-7ff0b6107a0b
description: 'Дата последнего изменения: 02 июля 2012 г.'
ms.openlocfilehash: 88716719857cfd623d30a3684fc997ea8019455e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409813"
---
# <a name="feid"></a>FEID

 
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Идентификатор папки. Он содержит идентификатор записи и другую важную информацию.
  
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

 _абфлагс_
  
> Идентификатор записи (4 байта) для папки. Дополнительные сведения об идентификаторах записей MAPI приведены в разделе **[EntryID](entryid.md)**. 
    
 _Muid_
  
> GUID, определяющий поставщика хранилища. Определение типа **мапиуид**можно найти в файле MAPIDEFS. h. 
    
 _нагляд_
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается.
    
 _лтид_
  
> Долгосрочный идентификатор папки.
    
## <a name="see-also"></a>См. также



[Сведения о конечном автомате репликации](about-the-replication-state-machine.md)
  
[Константы MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[Синхр](sync.md)

