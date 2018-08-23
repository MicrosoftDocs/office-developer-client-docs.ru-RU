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
ms.openlocfilehash: 91a56acf4afc7453496fa89becd905184101c910
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591396"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
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

