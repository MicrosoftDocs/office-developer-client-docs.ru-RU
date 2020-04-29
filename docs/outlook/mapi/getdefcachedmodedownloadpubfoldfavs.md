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
  
Указывает, включен ли режим кэширования данных Exchange для папки **избранных общедоступных папок** , и является ли он принудительно примененной политикой. 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |MSMapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedModeDownloadPubFoldFavs(BOOL *pfPolicy); 

```

## <a name="parameters"></a>Параметры

 _пфполици_
  
> вышли **имеет значение true** , если возвращаемое значение принудительно применяется политикой, в противном случае — **false** . 
    
## <a name="return-values"></a>Возвращаемые значения

 **относится**
  
- Включено кэширование.
    
 **значения**
  
- Кэширование отключено.
    
## <a name="see-also"></a>См. также



[GetDefCachedMode](getdefcachedmode.md)

