---
title: IOlkAccountManagerUnadvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.
ms.openlocfilehash: 0632bc6bd98e218cf323262ea480b020185438f3
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807855"
---
# <a name="iolkaccountmanagerunadvise"></a>IOlkAccountManager::Unadvise

Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей. 
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT Unadvise(
    DWORD dwCookie
);

```

## <a name="parameters"></a>Parameters

_dwCookie_
  
> [in] Файл cookie, возвращаемых [IOlkAccountManager::Advise](iolkaccountmanager-advise.md).
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

