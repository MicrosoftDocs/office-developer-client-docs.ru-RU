---
title: MSCAP_SELECTOR
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f28ac144-f5ac-fd83-2b72-8d6e5fd74b6e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9c5d8ab5bbac91250f3b8c552ad891c62134526e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417205"
---
# <a name="mscap_selector"></a>MSCAP_SELECTOR

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает возможности, возвращаемые для хранилища.
  
## <a name="quick-info"></a>Краткие сведения

```cpp
typedef enum 
{ 
    MSCAP_SEL_RESERVED1 = 0, 
    MSCAP_SEL_RESERVED2, 
    MSCAP_SEL_FOLDER, 
    MSCAP_SEL_RESERVED3, 
    MSCAP_SEL_RESTRICTION, 
} MSCAP_SELECTOR;
```

## <a name="members"></a>Элементы

 *MSCAP_SEL_RESERVED1* 
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
 *MSCAP_SEL_FOLDER* 
  
> Возможности, связанные с вспомогательными папками в магазине.
    
 *MSCAP_SEL_RESERVED3* 
  
> Этот член зарезервирован для внутреннего использования в Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Возможности, связанные с поддержкой ограничений в магазине.
    

