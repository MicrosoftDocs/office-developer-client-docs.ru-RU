---
title: Иолкаккаунтманажерадвисе
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c88f087e-4ff4-0837-186d-b6e761468a4d
description: Регистрирует клиента с помощью диспетчера учетных записей для уведомлений, касающихся всех учетных записей.
ms.openlocfilehash: 5460d55d906d382ce40ecd3fd9277cf370295680
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322199"
---
# <a name="iolkaccountmanageradvise"></a>IOlkAccountManager::Advise

Регистрирует клиента с помощью диспетчера учетных записей для уведомлений, касающихся всех учетных записей.
  
## <a name="quick-info"></a>Краткие сведения

See [IOlkAccountManager](iolkaccountmanager.md).
  
```cpp
HRESULT IOlkAccountManager::Advise (  
    IOlkAccountNotify *pNotify, 
    DWORD *pdwCookie 
);
```

## <a name="parameters"></a>Параметры

_Пнотифи_
  
> возврата Интерфейс [иолкаккаунтнотифи](iolkaccountnotify.md) , который диспетчер учетных записей будет использовать для отправки уведомлений клиенту. 
    
_Пдвкукие_
  
> вышли Файл cookie, [иолкаккаунтманажер:: unadvise](iolkaccountmanager-unadvise.md) будет использоваться при удалении регистрации для учетной записи. 
    
## <a name="return-values"></a>Возвращаемые значения

|**HRESULT**|**Description**|
|:-----|:-----|
|S_OK  <br/> |The call succeeded.  <br/> |
|E_INVALIDARG  <br/> |Указан недопустимый аргумент.  <br/> |
|Е_ОЛК_НОТ_ИНИТИАЛИЗЕД  <br/> |The account manager has not been initialized for use.  <br/> |
   
## <a name="see-also"></a>См. также

- [Constants (Account management API)](constants-account-management-api.md)  
- [IOlkAccountManager::Unadvise](iolkaccountmanager-unadvise.md)

