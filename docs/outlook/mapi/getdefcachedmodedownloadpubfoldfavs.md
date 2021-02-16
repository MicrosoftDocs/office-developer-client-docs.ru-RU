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
ms.openlocfilehash: 5e623c9d40ffd2dd276bd9601676244644bb3402
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417709"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, включен ли режим кэшации Exchange для папки "Избранное общедоступных папок" и является ли этот режим принудительно применен политикой.  
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется по:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Параметры

 _pfPolicy_
  
> [out] имеет значение **true,** если возвращаемого значения принудительно политики, **false,** если это не так. 
    
## <a name="return-values"></a>Возвращаемые значения

 **true**
  
- Кэшинг включен.
    
 **false**
  
- Кэшинг отключен.
    
## <a name="see-also"></a>См. также



[GetDefCachedMode](getdefcachedmode.md)

