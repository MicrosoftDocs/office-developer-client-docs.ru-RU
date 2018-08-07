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
ms.openlocfilehash: 420b2661e766ecf97a5e9e488e9c18f29cd91329
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19810022"
---
# <a name="mscapselector"></a>MSCAP_SELECTOR

  
  
**Относится к**: Outlook 
  
Задает возможности, чтобы возвратить хранилища.
  
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

## <a name="members"></a>Members

 *MSCAP_SEL_RESERVED1* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESERVED2* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_FOLDER* 
  
> Возможности о вспомогательных папок для хранилища.
    
 *MSCAP_SEL_RESERVED3* 
  
> Этот член зарезервирован для внутреннего использования Outlook и не поддерживается. 
    
 *MSCAP_SEL_RESTRICTION* 
  
> Возможности о поддержке ограничения для хранилища.
    

