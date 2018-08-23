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
ms.openlocfilehash: 919b21490bb3b4418ba291e8e06198028c995b00
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570873"
---
# <a name="required-features-for-address-book-providers"></a>Необходимые функции для поставщиков адресных книг

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Поставщиками адресной книги может работать с сведения о получателях, который является временной или постоянной, локальный или удаленных, понятно один или несколько систем обмена сообщениями и отформатированными в таблицу диск файла или базы данных. Существует множество возможностей, которые можно реализовать поставщика адресных книг, тем самым Добавление значение и улучшение взаимодействия с клиентами и других поставщиков. Тем не менее некоторые функции являются обязательными.
  
Ниже перечислены компоненты, необходимые для всех поставщиками адресной книги и действия, которые необходимо выполнить их реализации.
  
|**Функция**|**Реализация**|
|:-----|:-----|
|Сеанс входа в систему  <br/> | Реализуйте функцию точки входа. [Функцию адресной книги поставщика](implementing-an-address-book-provider-entry-point-function.md)для получения дополнительных сведений см.  <br/>  Реализуйте метод [IABProvider::Logon](iabprovider-logon.md) . Для получения дополнительных сведений см [Реализация адресной книги поставщика входа в систему и выход из системы](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Выход из системы сеанса  <br/> |Реализуйте метод [IABProvider::Shutdown](iabprovider-shutdown.md) . Для получения дополнительных сведений см [Реализация адресной книги поставщика входа в систему и выход из системы](implementing-address-book-provider-logon-and-logoff.md).  <br/> |
|Создание идентификаторы записей  <br/> |Обеспечивают поддержку для свойства **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Для получения дополнительных сведений см [Идентификаторы MAPI записей](mapi-entry-identifiers.md) и [Идентификаторы адресной книги](address-book-identifiers.md).  <br/> |
|Внесение данных в таблице состояния  <br/> | Реализовать соответствующие методы [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса. Для получения дополнительных сведений см [Реализация объекта состояния](status-object-implementation.md).  <br/>  Поддерживает свойства необходимые состояние таблицы. Для получения дополнительных сведений см [Состояние](status-tables.md).  <br/>  Вызов [IMAPISupport::ModifyStatusRow](imapisupport-modifystatusrow.md).  <br/> |
|Обеспечивают поддержку ограниченный состояние объекта  <br/> | Реализуйте метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) .  <br/>  Возвращает MAPI_E_NO_SUPPORT от других методов **IMAPIStatus** .  <br/> |
|Поддержка интерактивных и программный конфигурации  <br/> | Реализуйте функцию точки входа службы сообщений.  <br/>  Внедрите таблицу отображения. Дополнительные сведения можно [Отображать таблицы](display-tables.md) и [Реализации отображения таблицы](display-table-implementation.md).  <br/>  Реализация свойств или вызвать метод [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) . Для получения дополнительных сведений см [Реализация таблицы свойств](property-sheet-implementation.md).  <br/> |
   
Кроме того Если поставщик поддерживает создание получателей, необходимо указать список создания шаблонов. Указать этот список с помощью метода [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) для включения всех шаблонов, поддерживаемых поставщиком и метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) каждого контейнера, чтобы открыть **PR_CREATE_TEMPLATES** ([ PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)) свойство и включают все шаблоны, которые поддерживаются в контейнере. Для получения дополнительных сведений см [Реализация одноразовых таблиц](implementing-one-off-tables.md).
  

