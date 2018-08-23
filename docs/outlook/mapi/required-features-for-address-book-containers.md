---
title: Необходимые функции для контейнеров адресных книг
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3e221944-5dc9-4cce-8b47-73af84427aea
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 050a26f4b4e6c353881189f8c7b71c2e4c378d03
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577214"
---
# <a name="required-features-for-address-book-containers"></a>Необходимые функции для контейнеров адресных книг

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Большинство поставщиками адресных книг поддерживает по крайней мере один контейнер, некоторые из них можно изменить. Содержимое и таблиц иерархии, возможности поиска и разрешения имен, можно предоставить контейнеров адресной книги. Можно изменить контейнеров Разрешить удаление операций, таких как системы обмена сообщениями пользователи, списки рассылки или другие контейнеры и добавление записей из записей в других контейнеров или одноразовых шаблонов.
  
В следующей таблице описаны компоненты, необходимые для поставщиками адресных книг, которые имеют контейнеров, можно изменить или только для чтения, и как их реализовать.
  
|**Функция**|**Реализация**|
|:-----|:-----|
|Доступ пользователей системы обмена сообщениями  <br/> |Реализуйте метод [IABLogon::OpenEntry](iablogon-openentry.md) . Для получения дополнительных сведений см [Открытия адресной книги](opening-address-book-entries.md).  <br/> |
|Сравнение обмена мгновенными сообщениями пользователи  <br/> |Реализуйте метод [IABLogon::CompareEntryIDs](iablogon-compareentryids.md) . Для получения дополнительных сведений см [Сравнение адресной книги](comparing-address-book-entries.md).  <br/> |
|Создание пользователей системы обмена сообщениями  <br/> |1. Предоставление список шаблонов создания таблицы одноразовых за счет свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). [Таблица одноразовых контейнер](implementing-a-container-one-off-table.md)для получения дополнительных сведений см.  <br/> 2. реализуйте метод [IABContainer::CreateEntry](iabcontainer-createentry.md) . Для получения дополнительных сведений см [Добавление записей адресной книги](adding-address-book-entries.md).  <br/> |
|Скопируйте обмена мгновенными сообщениями пользователи  <br/> |Реализуйте метод [IABContainer::CopyEntries](iabcontainer-copyentries.md) . Для получения дополнительных сведений см. [Копирование адресной книги](copying-address-book-entries.md).  <br/> |
|Удаление пользователей системы обмена сообщениями  <br/> |Реализуйте метод [IABContainer::DeleteEntries](iabcontainer-deleteentries.md) . Для получения дополнительных сведений см [Удаление записей адресной книги](removing-address-book-entries.md).  <br/> |
|Предоставляют сводную информацию о системы обмена сообщениями пользователи  <br/> |Поддерживает свойство контейнера **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [���������� �������](contents-tables.md).  <br/> |
|Подробное описание системы обмена сообщениями пользователи  <br/> |Свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) поддерживается на системы обмена сообщениями пользователей и списки рассылки. Для получения дополнительных сведений см [Отображение сведений получателя](displaying-recipient-information.md) и [Отображать таблицы](display-tables.md).  <br/> |
|Содержатся подробные сведения о контейнере  <br/> |Свойство **PR_DETAILS_TABLE** поддерживается для контейнера. Для получения дополнительных сведений см [Отображение сведений получателя](displaying-recipient-information.md) и [Отображать таблицы](display-tables.md).  <br/> |
|Предоставление иерархический список контейнеров  <br/> |Поддерживает свойство контейнера **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Для получения дополнительных сведений см [Таблиц иерархии](hierarchy-tables.md).  <br/> |
|Поддержка обмена сообщениями свойств пользователя  <br/> |Реализация [IMailUser: IMAPIProp](imailuserimapiprop.md) интерфейса.  <br/> |
|Устранение неоднозначности имен  <br/> | Поддерживает ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  При необходимости реализуйте метод [IABContainer::ResolveNames](iabcontainer-resolvenames.md) . For more information, see [���������� ���������� ����](implementing-name-resolution.md).  <br/> |
   

