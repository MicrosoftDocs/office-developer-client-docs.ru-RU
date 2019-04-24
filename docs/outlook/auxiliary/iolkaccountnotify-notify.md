---
title: Иолкаккаунтнотифинотифи
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: dbce1c47-1252-ddeb-64ae-d52118e6821f
description: Уведомляет клиента об изменениях указанной учетной записи.
ms.openlocfilehash: 269d8a8bd605c9d8a0a4057e87895522d8587ee9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321968"
---
# <a name="iolkaccountnotifynotify"></a>IOlkAccountNotify::Notify

Уведомляет клиента об изменениях указанной учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

Обратитесь к разделу [иолкаккаунтнотифи](iolkaccountnotify.md).
  
```cpp
HRESULT IOlkAccount::Notify(  
    DWORD dwNotify, 
    DWORD dwAcctID, 
    DWORD dwFlags 
);

```

## <a name="parameters"></a>Параметры

_Двнотифи_
  
> возврата Тип уведомления. Поддерживаются такие значения:
    
   - НОТИФИ_АККТ_ЧАНЖЕД 
    
   - НОТИФИ_АККТ_КРЕАТЕД 
    
   - НОТИФИ_АККТ_ДЕЛЕТЕД
    
   - НОТИФИ_АККТ_ОРДЕР_ЧАНЖЕД 
    
   - НОТИФИ_АККТ_ПРЕДЕЛЕТЕД 
    
 _Двакктид_
  
> возврата Идентификатор учетной записи, которая была создана, изменена, удалена или предварительно удалена.
    
 _dwFlags_
  
>  возврата Не используется. ОЛК_АККАУНТ_НО_ФЛАГС — единственное поддерживаемое значение. 
    
## <a name="return-values"></a>Возвращаемые значения

S_OK if the call succeeded; otherwise, an error code.
  
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager](iolkaccountmanager.md)

