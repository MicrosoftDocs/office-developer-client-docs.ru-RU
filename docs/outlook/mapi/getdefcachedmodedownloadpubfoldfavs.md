---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ced6f2c6540e04a0bb4945ff98c4fda520322f03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581729"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, включена ли режима кэширования данных Exchange для **Общей папки "Избранное"** папки и ли это требование политики. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировать с:  <br/> |Msmapi32.dll  <br/> |
|Вызывается:  <br/> |Клиент  <br/> |
|Реализованный:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

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



[GetDefCachedMode](getdefcachedmode.md)

