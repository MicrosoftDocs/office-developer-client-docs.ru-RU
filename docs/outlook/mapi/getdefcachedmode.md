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
ms.openlocfilehash: 8e8a6ac07e14af52337b6e280fa58274df453c65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412746"
---
# <a name="getdefcachedmode"></a>GetDefCachedMode

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, включен ли режим кэшации Exchange для частного магазина Exchange и является ли этот режим принудительно применен политикой.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортируется по:  <br/> |msmapi32.dll  <br/> |
|Вызывающая сторона:  <br/> |Клиент  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

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



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

