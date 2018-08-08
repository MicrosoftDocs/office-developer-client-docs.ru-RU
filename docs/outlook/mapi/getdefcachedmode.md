---
title: GetDefCachedMode
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 325b6b47-b6a6-503e-e9bb-65ef7b73d659
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7595fac4346a537eed86550432f56a761c27c0ec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808567"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Относится к**: Outlook 
  
Указывает, включена ли режима кэширования данных Exchange для закрытого хранилища Exchange и ли это требование политики.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Параметры

 _pfPolicy_
  
> [out] **значение true,** Если возвращаемое значение обеспечивается политики **значение false** , если он не установлен. 
    
## <a name="return-values"></a>Возвращаемые значения

 **значение true**
  
- Кэширование.
    
 **false**
  
- Кэширование отключено.
    
## <a name="see-also"></a>См. также



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

