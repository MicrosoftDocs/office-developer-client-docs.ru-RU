---
title: IMsgStore IMAPIProp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMsgStore
api_type:
- COM
ms.assetid: 20090114-b183-4767-8971-a304a9aa47e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: af4bf73b58f7723066bb8fad7c087ba0238ceec2
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32348722"
---
# <a name="imsgstore--imapiprop"></a>IMsgStore : IMAPIProp

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Предоставляет доступ к сведениям о хранилище сообщений, а также к сообщениям и папкам.
  
|||
|:-----|:-----|
|Файл заголовка:  <br/> |MAPIDEFS. h  <br/> |
|Предоставлено:  <br/> |Объект хранилища сообщений  <br/> |
|Реализовано в:  <br/> |Поставщики хранилища сообщений  <br/> |
|Вызывающая сторона:  <br/> |Клиентские приложения, диспетчер очереди MAPI и MAPI  <br/> |
|Идентификатор интерфейса:  <br/> |Иид_имсгсторе  <br/> |
|Тип указателя:  <br/> |ЛПМДБ  <br/> |
|Модель транзакции:  <br/> |Не transactd  <br/> |
   
## <a name="vtable-order"></a>Заказ vtable

|||
|:-----|:-----|
|[Рекомендуем](imsgstore-advise.md) <br/> |Регистрируется для получения уведомлений об указанных событиях, влияющих на хранилище сообщений.  <br/> |
|[Unadvise](imsgstore-unadvise.md) <br/> |ОтМеняет отправку уведомлений, ранее настроенных с помощью вызова метода **IMsgStore:: Advise** .  <br/> |
|[CompareEntryIDs](imsgstore-compareentryids.md) <br/> |Сравнивает два идентификатора записи, чтобы определить, ссылаются ли они на одну и ту же запись в хранилище сообщений.  <br/> |
|[OpenEntry](imsgstore-openentry.md) <br/> |Открывает папку или сообщение и возвращает указатель интерфейса для получения дальнейших прав.  <br/> |
|[Сетрецеивефолдер](imsgstore-setreceivefolder.md) <br/> |Устанавливает папку в качестве назначения для входящих сообщений определенного класса сообщений.  <br/> |
|[Жетрецеивефолдер](imsgstore-getreceivefolder.md) <br/> |Получает папку, которая была установлена в качестве назначения для входящих сообщений указанного класса сообщений или в качестве папки получения по умолчанию для хранилища сообщений.  <br/> |
|[Жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) <br/> |Предоставляет доступ к таблице получения папки, в которой содержатся сведения обо всех папках получения для хранилища сообщений.  <br/> |
|[Сторелогофф](imsgstore-storelogoff.md) <br/> |Позволяет выполнять упорядоченный выход из хранилища сообщений.  <br/> |
|[Абортсубмит](imsgstore-abortsubmit.md) <br/> |Пытается удалить сообщение из исходящей очереди.  <br/> |
|[Жетаутгоингкуеуе](imsgstore-getoutgoingqueue.md) <br/> |Предоставляет доступ к таблице исходящей очереди, таблице, содержащей сведения обо всех сообщениях в исходящей очереди хранилища сообщений.  <br/> |
|[Сетлоккстате](imsgstore-setlockstate.md) <br/> |Блокировка или разблокировка сообщения.  <br/> |
|[Финишедмсг](imsgstore-finishedmsg.md) <br/> |Позволяет поставщику хранилища сообщений выполнять обработку отправленного сообщения.  <br/> |
|[Нотифиневмаил](imsgstore-notifynewmail.md) <br/> |����������� ��������� ���������, ����� ���������.  <br/> |
   
|**Обязательные свойства**|**Уровень доступа**|
|:-----|:-----|
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |Чтение и запись  <br/> |
|**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_рекорд_кэй** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_ентрид** ([PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_рекорд_кэй** ([PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_мдб_провидер** ([PidTagStoreProvider](pidtagstoreprovider-canonical-property.md))  <br/> |Только для чтения  <br/> |
|**Пр_сторе_суппорт_маск** ([PidTagStoreSupportMask](pidtagstoresupportmask-canonical-property.md))  <br/> |Только для чтения  <br/> |
   
Для хранилищ сообщений взаимосвязанных сообщений (IPM) используются следующие свойства:
  
- **Пр_ипм_аутбокс_ентрид** ([PidTagIpmOutboxEntryId](pidtagipmoutboxentryid-canonical-property.md))
    
- **Пр_ипм_сентмаил_ентрид** ([PidTagIpmSentMailEntryId](pidtagipmsentmailentryid-canonical-property.md))
    
- **Пр_ипм_субтри_ентрид** ([PidTagIpmSubtreeEntryId](pidtagipmsubtreeentryid-canonical-property.md))
    
- **Пр_ипм_вастебаскет_ентрид** ([PidTagIpmWastebasketEntryId](pidtagipmwastebasketentryid-canonical-property.md))
    
- **ПР_МДБ_ПРОВИДЕР**
    
- **ПР_СТОРЕ_СУППОРТ_МАСК**
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)

