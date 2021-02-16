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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Поставщики адресных книг могут работать с временной или постоянной информацией о получателях, локальной или удаленной, понятной для одной или более систем обмена сообщениями и отформатированной для файла диска или таблицы базы данных. Существует множество функций, которые может реализовать поставщик адресной книги, тем самым повышая ценность и улучшая возможности связи с клиентами и другими поставщиками. Однако требуется несколько функций.
  
В следующей таблице описываются функции, необходимые для всех поставщиков адресных книг, а также действия, которые необходимо выполнить для их реализации.
  
|**Функция**|**Методика реализации**|
|:-----|:-----|
|Сеанс для логотипа  <br/> | Реализация функции точки входа. Дополнительные сведения [см. в реализации функции](implementing-an-address-book-provider-entry-point-function.md)точки входа поставщика адресной книги.  <br/>  Реализуют [метод IABProvider::Logon.](iabprovider-logon.md) Дополнительные сведения см. в окне "Реализация входа и входа поставщика адресной [книги".](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Выйдите из сеанса  <br/> |Реализуют [метод IABProvider::Shutdown.](iabprovider-shutdown.md) Дополнительные сведения см. в окне "Реализация входа и входа поставщика адресной [книги".](implementing-address-book-provider-logon-and-logoff.md)  <br/> |
|Создание идентификаторов записей  <br/> |Обеспечение поддержки свойства **PR_ENTRYID** ([PidTagEntryId).](pidtagentryid-canonical-property.md) Дополнительные сведения см. в документе [MAPI Entry Identifiers](mapi-entry-identifiers.md) and [Address Book Identifiers.](address-book-identifiers.md)  <br/> |
|Участие в таблице состояния  <br/> | Реализуют соответствующие методы [интерфейса IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md) Дополнительные сведения см. в [реализации объекта status.](status-object-implementation.md)  <br/>  Поддержка необходимых свойств таблицы состояния. Дополнительные сведения см. в [таблицах состояния.](status-tables.md)  <br/>  Вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Предоставление поддержки объектов с ограниченным состоянием  <br/> | Реализуют [метод IMAPIStatus::ValidateState.](imapistatus-validatestate.md)  <br/>  Возвращает MAPI_E_NO_SUPPORT из других методов **IMAPIStatus.**  <br/> |
|Поддержка интерактивной и программной настройки  <br/> | Реализация функции точки входа службы сообщений.  <br/>  Реализация таблицы отображения. Дополнительные сведения [см.](display-tables.md) в таблице отображения и [реализации таблиц отображения.](display-table-implementation.md)  <br/>  Реализуют лист свойств или вызовите метод [IMAPISupport::D oConfigPropsheet.](imapisupport-doconfigpropsheet.md) Дополнительные сведения см. в [реализации листа свойств.](property-sheet-implementation.md)  <br/> |
   
Кроме того, если поставщик поддерживает создание получателей, необходимо предоставить список шаблонов создания. Передайте этот список, реализуя метод [IABLogon::GetOneOffTable,](iablogon-getoneofftable.md) чтобы включить все шаблоны, поддерживаемые поставщиком, и метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) каждого контейнера для открытия свойства **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates)](pidtagcreatetemplates-canonical-property.md)и включить все шаблоны, поддерживаемые контейнером. Дополнительные сведения [см. в One-Off Таблицы.](implementing-one-off-tables.md)
  

