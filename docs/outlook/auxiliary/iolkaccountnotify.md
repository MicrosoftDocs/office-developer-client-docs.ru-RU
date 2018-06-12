---
title: IOlkAccountNotify
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 360854bb-e9be-a784-e80b-3f18418ded1b
ms.openlocfilehash: f4b57ad1062df9aa1809e8eb422a2c983adcac4a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807865"
---
# <a name="iolkaccountnotify"></a>IOlkAccountNotify

Предоставляет обратный вызов клиента для изменения учетной записи.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[IOlkErrorUnknown](iolkerrorunknown.md) <br/> |
|Предоставлено:  <br/> | Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkAccountNotify  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Уведомления](iolkaccountnotify-notify.md) <br/> |Уведомляет клиента о изменения для указанной учетной записи.  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс передается [IOlkAccountManager::Advise](iolkaccountmanager-advise.md) при настройке уведомлений. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

