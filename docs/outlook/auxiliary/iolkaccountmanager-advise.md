---
title: IOlkAccountManagerAdvise
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Регистрация клиента диспетчером учетной записи для уведомлений о всех учетных записей.
ms.openlocfilehash: 1fb697fef44b9ed32888527c3c9e467be69ba4c7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807839"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Регистрация клиента диспетчером учетной записи для уведомлений о всех учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Parameters

_pNotify_
  
> [in] Интерфейс [IOlkAccountNotify](iolkaccountnotify.md) , диспетчер учетных записей для отправки уведомлений для клиента. 
    
_pdwCookie_
  
> [out] Файл cookie, [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md) будет использоваться при удалении регистрации учетной записи. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|ЗНАЧЕНИЕ S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Указан недопустимый аргумент было предоставлено.  <br/> |
|E_OLK_NOT_INITIALIZED  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

