---
title: IOlkAccountHelper
manager: soliver
ms.date: 12/07/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: fc2972da-80e9-50e2-10b3-585eb63e9103
ms.openlocfilehash: 241babe45b543fb00c0d2756a2e846303a1717b2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32322157"
---
# <a name="iolkaccounthelper"></a>IOlkAccountHelper

Предоставляет вспомогательные функциональные возможности в текущем сеансе MAPI для управления учетными записями.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Наследование от:  <br/> |[Интерфейс](https://msdn.microsoft.com/library/33f1d79a-33fc-4ce5-a372-e08bda378332%28Office.15%29.aspx) <br/> |
|Предоставлено:  <br/> |Client  <br/> |
|Идентификатор интерфейса:  <br/> |IID_IOlkAccountHelper  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Placeholder1](iolkaccounthelper-placeholder1.md) <br/> | *Этот элемент является заполнителем и не поддерживается.*  <br/> |
|[Идентификация по длинности](iolkaccounthelper-getidentity.md) <br/> |Получает имя профиля учетной записи.  <br/> |
|[жетмаписессион](iolkaccounthelper-getmapisession.md) <br/> |Открывает сеанс MAPI и поддерживает ссылку на сеанс для диспетчера учетных записей.  <br/> |
|[хандсоффсессион](iolkaccounthelper-handsoffsession.md) <br/> |Освобождает объект сеанса MAPI, возвращенный функцией [иолкаккаунселпер:: жетмаписессион](iolkaccounthelper-getmapisession.md).  <br/> |
   
## <a name="remarks"></a>Примечания

Этот интерфейс передается в [иолкаккаунтманажер:: init](iolkaccountmanager-init.md) при инициализации диспетчера учетных записей. 
  
## <a name="see-also"></a>См. также

- [Сведения об API управления учетными записями](about-the-account-management-api.md) 
- [Constants (Account management API)](constants-account-management-api.md)

