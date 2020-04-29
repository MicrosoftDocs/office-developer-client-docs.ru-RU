---
title: иолкаккаунтманажерунадвисе
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: ea5cbf9f-25cc-9cca-9be0-d2deed576153
description: Отменяет регистрацию клиента с помощью диспетчера учетных записей для уведомлений для всех учетных записей.
ms.openlocfilehash: 0b954413b06cb1aa1b6fc4e0e9666f108bf81fbe
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430989"
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

## <a name="parameters"></a>Параметры

_двкукие_
  
> возврата Файл cookie, возвращенный функцией [иолкаккаунтманажер:: Advise](iolkaccountmanager-advise.md).
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Один или несколько аргументов являются недопустимыми.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Advise](iolkaccountmanager-advise.md)

