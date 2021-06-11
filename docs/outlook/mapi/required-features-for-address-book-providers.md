---
title: Необходимые функции для поставщиков адресных книг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: e2ccddd7-65e8-41f6-8e21-a4ae98190a96
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 56ca15440c8d323dbab1b6a92a01941106b86934
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33421398"
---
# <a name="required-features-for-address-book-providers"></a>Необходимые функции для поставщиков адресных книг

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Поставщики адресных книг могут работать с данными получателей, которые являются временными или постоянными, локальными или удаленными, понятными для одной или более систем обмена сообщениями и форматируемыми для дискового файла или таблицы баз данных. Существует множество функций, которые поставщик адресных книг может реализовать, тем самым повышая ценность и улучшая возможность работы с клиентами и другими поставщиками. Однако требуется несколько функций.
  
В следующей таблице описываются функции, необходимые для всех поставщиков адресных книг, и действия, которые необходимо предпринять для их реализации.
  
|**Функция**|**Методика реализации**|
|:-----|:-----|
|Логотип сеанса  <br/> | Реализация функции точки входа. Дополнительные сведения см. в [книге Реализация функции](implementing-an-address-book-provider-entry-point-function.md)точки входа поставщика адресных книг.  <br/>  Реализация [метода IABProvider::Logon.](iabprovider-logon.md) Дополнительные сведения см. в [журнале Implementing Address Book Provider Logon and Logoff.](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Журнал сеанса  <br/> |Реализация [метода IABProvider::Shutdown.](iabprovider-shutdown.md) Дополнительные сведения см. в [журнале Implementing Address Book Provider Logon and Logoff.](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Создание идентификаторов записей  <br/> |Поддержка свойства **PR_ENTRYID** [(PidTagEntryId).](pidtagentryid-canonical-property.md) Дополнительные сведения см. в [документе MAPI Entry Identifiers](mapi-entry-identifiers.md) and [Address Book Identifiers.](address-book-identifiers.md)  <br/> |
|Внести вклад в таблицу состояния  <br/> | Реализация соответствующих методов [интерфейса IMAPIStatus: IMAPIProp.](imapistatusimapiprop.md) Дополнительные сведения см. в [дополнительных сведениях о реализации объектов status.](status-object-implementation.md)  <br/>  Поддержка необходимых свойств таблицы состояния. Дополнительные сведения см. в [таблице Status Tables.](status-tables.md)  <br/>  Вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Предоставление поддержки объектов с ограниченным состоянием  <br/> | Реализация [метода IMAPIStatus::ValidateState.](imapistatus-validatestate.md)  <br/>  Возврат MAPI_E_NO_SUPPORT из других **методов IMAPIStatus.**  <br/> |
|Поддержка интерактивной и программной конфигурации  <br/> | Реализация функции точки входа службы сообщений.  <br/>  Реализация таблицы отображения. Дополнительные сведения см. в [таблицах отображения и](display-tables.md) [реализации таблиц отображения.](display-table-implementation.md)  <br/>  Реализация листа свойств или вызов [метода IMAPISupport::D ConfigPropsheet.](imapisupport-doconfigpropsheet.md) Дополнительные сведения см. в [реализации листа свойств.](property-sheet-implementation.md)  <br/> |
   
Кроме того, если поставщик поддерживает создание получателей, необходимо предоставить список шаблонов создания. Поставляем этот список, реализуя метод [IABLogon::GetOneOffTable,](iablogon-getoneofftable.md) чтобы включить все шаблоны, поддерживаемые вашим поставщиком, и метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) каждого контейнера, чтобы открыть свойство **PR_CREATE_TEMPLATES** [(PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)и включить все шаблоны, поддерживаемые контейнером. Дополнительные сведения см. в [One-Off Таблицы](implementing-one-off-tables.md).
  

