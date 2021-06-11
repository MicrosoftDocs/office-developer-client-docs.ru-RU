---
title: Открытие записей адресной книги
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 017a62c0-49c6-47fb-acce-db58e6bb9cc5
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6ebd6009700742e9b1159bc95ff0496c423e512c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422161"
---
# <a name="opening-address-book-entries"></a>Открытие записей адресной книги

**Область применения**: Outlook 2013 | Outlook 2016 
  
Если клиент или поставщик запросили открыть один из объектов, MAPI вызывает метод [IABLogon::OpenEntry](iablogon-openentry.md) поставщика. MAPI определяет, что идентификатор записи, представляющий целевой объект, принадлежит поставщику, изучив часть [MAPIUID](mapiuid.md) идентификатора входа и сопопределив его с **MAPIUID,** который поставщик зарегистрировал в вызове **в IMAPISupport::SetProviderUID**. После этого MAPI вызывает метод **OpenEntry.** Поставщик должен отвечать на запросы соответствующего объекта — контейнера, списка рассылки или пользователя обмена сообщениями. 
  
Идентификатор записи NULL указывает запрос на открытие корневого контейнера поставщика адресной книги. Клиенты открывают корневой контейнер для доступа к таблице иерархии и получателям. Поставщики адресных книг, которые поставляют только шаблоны для создания разных получателей, не поддерживают вызов **OpenEntry** для корневого контейнера. 
  
### <a name="to-implement-iablogonopenentry"></a>Реализация IABLogon::OpenEntry
  
1. Убедитесь, что идентификатор записи является допустимым идентификатором, поддерживаемым поставщиком. Если это не допустимый идентификатор входа, верни MAPI_E_INVALID_ENTRYID. 
    
2. Проверьте флаг, который передается с параметром _ulFlags._ Если MAPI прошел в MAPI_MODIFY и поставщик не разрешает изменять его объекты, не удается вернуть значение MAPI_E_ACCESS_DENIED ошибки. 
    
3. Убедитесь, что интерфейс, запрашиваемый в  _параметре lpInterface,_ действителен для типа объекта, который был предложен открыть поставщику. Если недействительный параметр был пройден, сбой и возвращение значения MAPI_E_INTERFACE_NOT_SUPPORTED ошибки. 
    
4. Если параметр  _cbEntryID_ ноль, это запрос на открытие корневого контейнера поставщика. Создайте корневой контейнер и верни указатель для реализации интерфейса **IABContainer.** 
    
5. Если поставщик реализует несколько объектов с логотипом, каждый из которых имеет собственный зарегистрированный **MAPIUID,** на карте **MAPIUID,** содержался в идентификаторе входа с соответствующим объектом logon. 
    
6. Определите, какой тип объекта представляет идентификатор записи: пользователь сообщения, список рассылки или контейнер, принадлежащий поставщику, или разовый пользователь или список рассылки сообщений, чтобы можно было установить соответствующее значение для _параметра lpulObjectType._ 
    
7. Создайте объект соответствующего типа и установите следующие основные свойства:
    
    - **PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)
    - **PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)
    - **PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)
    - **PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)
    
8. Вычислять **PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)  и PR_DISPLAY_NAME [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)из сведений в идентификаторе записи.
    
9. Верни указатель в реализацию интерфейса для объекта. 
    

