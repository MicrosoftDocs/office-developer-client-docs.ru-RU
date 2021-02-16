---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Регистрирует клиент в диспетчере учетных записей для уведомлений о всех учетных записях.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427712"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Регистрирует клиент в диспетчере учетных записей для уведомлений о всех учетных записях.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Параметры

_pNotify_
  
> [in] Интерфейс [IOlkAccountNotify,](iolkaccountnotify.md) который диспетчер учетных записей будет использовать для отправки уведомлений клиенту. 
    
_pdwCookie_
  
> [out] Файл cookie, который будет использовать [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) при удалении регистрации учетной записи. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Предоставлен недопустимый аргумент.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

