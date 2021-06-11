---
title: Необязательные функции для поставщиков адресных книг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f1558259-7f0b-4731-80d2-88e51e203df0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9f5d8f0cd1b21f58e4e5c7d7ccd6cb19f3626c38
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33414573"
---
# <a name="optional-features-for-address-book-providers"></a>Необязательные функции для поставщиков адресных книг

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Существует множество необязательных функций для поставщиков адресных книг. Некоторые из наиболее распространенных функций включают в себя:
  
- Выступая в качестве иностранного поставщика, разрешив добавлять записи из одного из контейнеров в контейнер другого поставщика.
    
- Действуя в качестве поставщика хостинга, добавляя записи от другого поставщика в один из контейнеров.
    
- Расширенный поиск.
    
- Префикс прокрутки через таблицы контента.
    
- Поддержка списков рассылки.
    
- Поддержка уведомления о событиях.
    
В следующей таблице кратко описаны эти необязательные функции и их реализация:
  
|**Функция**|**Методика реализации**|
|:-----|:-----|
|Шаблоны поставок для создания записей для списков получателей сообщений  <br/> |Реализация [метода IABLogon::GetOneOffTable.](iablogon-getoneofftable.md) Дополнительные сведения см. в [таблице One-Off Tables](one-off-tables.md) and [Implementing One-Off Tables.](implementing-one-off-tables.md)  <br/> |
|Получатели группы в именоваемом подразделении  <br/> |Поддержка свойств списков рассылки путем реализации [интерфейса IDistList : IMAPIContainer.](idistlistimapicontainer.md)  <br/> |
|Выступать в качестве иностранного поставщика адресных книг, разрешив добавлять записи в контейнер в другом поставщике  <br/> | Поддержка привязки кода к данным в принимающем поставщике с помощью:  <br/>  Поддержка **свойства PR_TEMPLATEID** [(PidTagTemplateid)](pidtagtemplateid-canonical-property.md)для пользователей сообщений и списков рассылки. Дополнительные сведения см. [в книге Идентификаторы адресной книги.](address-book-identifiers.md)  <br/>  Реализация метода [IABLogon::OpenTemplateID.](iablogon-opentemplateid.md) Дополнительные сведения см. [в книге Acting as a Foreign Address Book Provider](acting-as-a-foreign-address-book-provider.md).  <br/> |
|Действуя в качестве поставщика адресной книги, вставляя записи от другого поставщика  <br/> |Поддержка привязки данных к коду от иностранного поставщика, позвонив по [методу IMAPISupport::OpenTemplateID.](imapisupport-opentemplateid.md) Дополнительные сведения см. в [книге Acting as a Host Address Book Provider](acting-as-a-host-address-book-provider.md).  <br/> |
|Прокрутка префикса  <br/> |Поддержка ограничений на таблицы содержимого контейнера. Дополнительные сведения см. [в дополнительных сведениях об ограничениях.](about-restrictions.md)  <br/> |
|Расширенный поиск в контейнере  <br/> |Поддержка **свойства PR_SEARCH** [(PidTagSearch)](pidtagsearch-canonical-property.md)в контейнерах. Дополнительные сведения см. в [дополнительных сведениях о внедрении расширенных поисков.](implementing-advanced-searching.md)  <br/> |
|Уведомление о событии  <br/> |Реализация [методов IABLogon:::Advise](iablogon-advise.md) и [IABLogon::Unadvise.](iablogon-unadvise.md) Дополнительные сведения см. в [приложениях Event Notification in MAPI](event-notification-in-mapi.md) и [Supporting Event Notification.](supporting-event-notification.md)  <br/> |
   
Для уведомления о событиях метод **IABLogon::Advise** будет вызван MAPI, когда клиент вызывает **IAddrBook:::Advise** для регистрации уведомлений в любом из контейнеров, пользователей сообщений или списков рассылки. Однако, так как поддержка уведомления о событиях необязательна, вы можете MAPI_E_NO_SUPPORT из этих методов. Однако MAPI рекомендует по крайней мере поддерживать уведомления в таблицах контента и поддерживать все типы уведомлений об объектах, за исключением  _fnevSearchComplete_ и  _события fnevCriticalError_ для добавления значения. 
  

