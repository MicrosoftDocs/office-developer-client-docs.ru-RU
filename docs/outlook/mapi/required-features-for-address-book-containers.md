---
title: Необходимые функции для контейнеров адресной книги
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439683"
---
# <a name="required-features-for-address-book-containers"></a>Необходимые функции для контейнеров адресной книги

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Большинство поставщиков адресных книг поддерживают хотя бы один контейнер, некоторые из которых можно модификировать. Контейнеры адресных книг могут предоставить содержимое и таблицы иерархии, возможности поиска и разрешение имен. Измеримые контейнеры позволяют удалять записи, такие как пользователи сообщений, списки рассылки или другие контейнеры, а также добавление записей из записей в других контейнерах или из разных шаблонов.
  
В следующей таблице описываются функции, необходимые поставщикам адресных книг, у которых есть контейнеры, которые можно модификировать или только для чтения, а также их реализация.
  
|**Функция**|**Методика реализации**|
|:-----|:-----|
|Доступ к пользователям сообщений  <br/> |Реализуют [метод IABLogon::OpenEntry.](iablogon-openentry.md) Дополнительные сведения [см. в записях открываемой адресной книги.](opening-address-book-entries.md)  <br/> |
|Сравнение пользователей системы обмена сообщениями  <br/> |Реализуют [метод IABLogon::CompareEntryIDs.](iablogon-compareentryids.md) Дополнительные сведения см. в статьях ["Сравнение записей адресной книги".](comparing-address-book-entries.md)  <br/> |
|Создание пользователей системы обмена сообщениями  <br/> |1. Предоставление списка шаблонов создания в одноразовой таблице путем поддержки **свойства PR_CREATE_TEMPLATES** ([PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md) Дополнительные сведения см. в таблице ["Реализация контейнерных One-Off".](implementing-a-container-one-off-table.md)  <br/> 2. Реализуйте [метод IABContainer::CreateEntry.](iabcontainer-createentry.md) Дополнительные сведения см. в [добавлении записей адресной книги.](adding-address-book-entries.md)  <br/> |
|Копирование пользователей системы обмена сообщениями  <br/> |Реализуют [метод IABContainer::CopyEntries.](iabcontainer-copyentries.md) Дополнительные сведения см. в статьях ["Копирование записей адресной книги".](copying-address-book-entries.md)  <br/> |
|Удаление пользователей системы обмена сообщениями  <br/> |Реализуйте [метод IABContainer::D eleteEntries.](iabcontainer-deleteentries.md) Дополнительные сведения см. в [статьях "Удаление записей адресной книги".](removing-address-book-entries.md)  <br/> |
|Предоставление сводных сведений о пользователях сообщений  <br/> |Поддержка свойства контейнера **PR_CONTAINER_CONTENTS** ([PidTagContainerContents).](pidtagcontainercontents-canonical-property.md) For more information, see [���������� �������](contents-tables.md).  <br/> |
|Предоставление подробных сведений о пользователях сообщений  <br/> |Поддержка свойства **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)для пользователей сообщений и списков рассылки. Дополнительные сведения см. в таблице ["Отображение сведений о получателях](displaying-recipient-information.md) и [отображение таблиц".](display-tables.md)  <br/> |
|Предоставление подробных сведений о контейнере  <br/> |Поддержка **PR_DETAILS_TABLE** контейнера. Дополнительные сведения см. в таблице ["Отображение сведений о получателях](displaying-recipient-information.md) и [отображение таблиц".](display-tables.md)  <br/> |
|Предоставление иерархического списка контейнеров  <br/> |Поддержка свойства контейнера **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy).](pidtagcontainerhierarchy-canonical-property.md) Дополнительные сведения см. [в таблицах иерархии.](hierarchy-tables.md)  <br/> |
|Поддержка свойств пользователей сообщений  <br/> |Реализация [интерфейса IMailUser : IMAPIProp.](imailuserimapiprop.md)  <br/> |
|Устранение неоднозначности имен  <br/> | Поддержка ограничения **PR_ANR** ([PidTagAnr).](pidtaganr-canonical-property.md)  <br/>  При желании реализуют [метод IABContainer::ResolveNames.](iabcontainer-resolvenames.md) For more information, see [���������� ���������� ����](implementing-name-resolution.md).  <br/> |
   

