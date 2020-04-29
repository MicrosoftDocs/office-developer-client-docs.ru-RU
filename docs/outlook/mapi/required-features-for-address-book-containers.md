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
ms.openlocfilehash: abdbd9030e0ea053d39b49ecc76a78821be9df82
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439683"
---
# <a name="required-features-for-address-book-containers"></a>Необходимые функции для контейнеров адресных книг

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Большинство поставщиков адресных книг поддерживают по крайней мере один контейнер, некоторые из них могут быть изменены. Контейнеры адресных книг могут предоставлять содержимое и таблицы иерархий, возможности поиска и разрешение имен. Изменяемые контейнеры позволяют удалять такие записи, как пользователи обмена сообщениями, списки рассылки или другие контейнеры, а также добавлять записи из элементов в других контейнерах или из одноразовых шаблонов.
  
В следующей таблице описаны функции, которые необходимы поставщикам адресных книг, которые имеют контейнеры, изменяемые или доступные только для чтения, а также способы их реализации.
  
|**Функция**|**Методика реализации**|
|:-----|:-----|
|Доступ к сообщениям для пользователей  <br/> |Реализуйте метод [иаблогон:: OpenEntry](iablogon-openentry.md) . Более подробную информацию можно узнать в разделе [Открытие записей адресной книги](opening-address-book-entries.md).  <br/> |
|Сравнение пользователей обмена сообщениями  <br/> |Реализуйте метод [иаблогон:: метод compareentryids](iablogon-compareentryids.md) . Для получения дополнительных сведений см раздел [Сравнение записей адресной книги](comparing-address-book-entries.md).  <br/> |
|Создание пользователей обмена сообщениями  <br/> |1. Предоставьте список шаблонов создания в одноразовой таблице, дополнив свойство **PR_CREATE_TEMPLATES** ([PidTagCreateTemplates](pidtagcreatetemplates-canonical-property.md)). Дополнительные сведения см в разделе [Реализация одноразовой таблицы контейнера](implementing-a-container-one-off-table.md).  <br/> 2. реализуйте метод [иабконтаинер:: креатинтри](iabcontainer-createentry.md) . Дополнительную информацию можно узнать в статье [Добавление записей адресной книги](adding-address-book-entries.md).  <br/> |
|Копирование пользователей обмена сообщениями  <br/> |Реализуйте метод [иабконтаинер:: копентриес](iabcontainer-copyentries.md) . Более подробную информацию можно узнать в статье [копирование записей адресной книги](copying-address-book-entries.md).  <br/> |
|Удаление пользователей обмена сообщениями  <br/> |Реализуйте метод [иабконтаинер::D елетинтриес](iabcontainer-deleteentries.md) . Более подробную информацию можно узнать в статье [Удаление записей адресной книги](removing-address-book-entries.md).  <br/> |
|Предоставление сводных сведений о пользователях для обмена сообщениями  <br/> |Поддерживает свойство Container **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)). For more information, see [���������� �������](contents-tables.md).  <br/> |
|Предоставление подробных сведений о пользователях системы обмена сообщениями  <br/> |Поддерживает свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) для пользователей обмена сообщениями и списков рассылки. Дополнительную информацию можно узнать в статье [Отображение сведений о получателях](displaying-recipient-information.md) и [таблицах отображения](display-tables.md).  <br/> |
|Предоставление подробных сведений о контейнере  <br/> |Поддерживает свойство **PR_DETAILS_TABLE** контейнера. Дополнительную информацию можно узнать в статье [Отображение сведений о получателях](displaying-recipient-information.md) и [таблицах отображения](display-tables.md).  <br/> |
|Предоставление иерархического списка контейнеров  <br/> |Поддерживает свойство Container **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)). Более подробную информацию можно узнать в статье [Иерархия Tables](hierarchy-tables.md).  <br/> |
|Свойства пользователя обмена сообщениями в службу поддержки  <br/> |Реализуйте интерфейс [имаилусер: IMAPIProp](imailuserimapiprop.md) .  <br/> |
|Разрешение неоднозначных имен  <br/> | Поддерживает ограничение свойства **PR_ANR** ([PidTagAnr](pidtaganr-canonical-property.md)).  <br/>  При необходимости реализуйте метод [иабконтаинер:: ResolveNames](iabcontainer-resolvenames.md) . For more information, see [���������� ���������� ����](implementing-name-resolution.md).  <br/> |
   

