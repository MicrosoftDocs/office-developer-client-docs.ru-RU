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
ms.openlocfilehash: bb2d347d218a7c33a2184bf1fcf181a11fa7d8fe
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808431"
---
# <a name="feid"></a>FEID

 
  
**Применимо к**: Outlook 
  
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

## <a name="members"></a>Элементы

 _abFlags_
  
> Идентификатор записи 4-байтных папки. Дополнительные сведения об идентификаторах запись MAPI можно **[ENTRYID](entryid.md)**. 
    
 _muid_
  
> GUID, идентифицирующий поставщика хранилища. В разделе mapidefs.h для определения типа **MAPIUID**. 
    
 _заполнитель_
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается.
    
 _ltid_
  
> Долгосрочные идентификатор папки.
    
## <a name="see-also"></a>См. также



[О репликации конечного автомата](about-the-replication-state-machine.md)
  
[��������� MAPI](mapi-constants.md)
  
[LTID](ltid.md)
  
[UPFLD](upfld.md)
  
[СИНХРОНИЗАЦИЯ](sync.md)

