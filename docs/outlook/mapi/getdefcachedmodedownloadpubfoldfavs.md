---
title: GetDefCachedModeDownloadPubFoldFavs
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 2dd95561-ed8f-8a3b-6532-b53556f16666
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: cb93d9ae4e6660c208d74e43bb26be4dbd55f4e1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808566"
---
# <a name="getdefcachedmodedownloadpubfoldfavs"></a>GetDefCachedModeDownloadPubFoldFavs

  
  
**Применимо к**: Outlook 
  
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

## <a name="parameters"></a>Parameters

 _pfPolicy_
  
> [out] **значение true,** Если возвращаемое значение обеспечивается политики **значение false** , если он не установлен. 
    
## <a name="return-values"></a>Возвращаемые значения

 **значение true**
  
- Кэширование.
    
 **false**
  
- Кэширование отключено.
    
## <a name="see-also"></a>См. также



[GetDefCachedMode](getdefcachedmode.md)

