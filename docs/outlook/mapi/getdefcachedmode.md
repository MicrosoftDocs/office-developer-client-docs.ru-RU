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
  
Указывает, включен ли режим кэширования данных Exchange для частного хранилища Exchange и является ли он принудительно примененным с помощью политики.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Экспортировано:  <br/> |MSMapi32. dll  <br/> |
|Вызывающая сторона:  <br/> |Client  <br/> |
|Реализовано в:  <br/> |Outlook  <br/> |
   
```cpp
BOOL GetDefCachedMode(BOOL *pfPolicy); 

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



[GetDefCachedModeDownloadPubFoldFavs](getdefcachedmodedownloadpubfoldfavs.md)

