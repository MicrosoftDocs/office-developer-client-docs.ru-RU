---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 3c28b1e8ab7e2d72d27cc6545b6ef57834ef5b6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807834"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Предоставляет функциональные возможности модуля поддержки в текущем сеансе MAPI к управлению учетными записями.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследует от:  <br/> |[Интерфейс IUnknown](http://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Клиент  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Порядке vtable

|||
|:-----|:-----|
|[Прототип 1](iolkaccounthelper-placeholder1.md) <br/> | *Этот член — это и не поддерживается.*  <br/> |
|[GetIdentity](iolkaccounthelper-getidentity.md) <br/> |Получает имя профиля учетной записи.  <br/> |
|[GetMapiSession](iolkaccounthelper-getmapisession.md) <br/> |Открытие сеанса MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.  <br/> |
|[HandsOffSession](iolkaccounthelper-handsoffsession.md) <br/> |Освобождает объект сеанса MAPI, возвращаемые [IOlkAccountHelper::GetMapiSession](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Замечания

Этот интерфейс передается [IOlkAccountManager::Init](iolkaccountmanager-init.md) при инициализации диспетчера учетных записей. 
  
## <a name="see-also"></a>См. также

- [About the Account Management API](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

