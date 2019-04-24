---
title: Написание средства удаленного просмотра
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f4d7d42f-688a-4199-b972-dd42528c0cdf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 1d7fea7f92a315b9671d17c82a82d5d7d180f4bb
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32325664"
---
# <a name="writing-a-remote-viewer"></a>Написание средства удаленного просмотра

**Область применения**: Outlook 2013 | Outlook 2016 
  
Удаленное средство просмотра это окно в клиентском приложении, которое предоставляет контролируемый доступ к сообщениям, хранящимся на другом компьютере. Этот контролируемый доступ может работать на медленном канале связи. Вместо получения полного набора доступных сообщений каждый раз, когда пользователь открывает папку, удаленное средство просмотра сначала отображает только заголовки. Затем пользователь выбирает из заголовков, для которых сообщения отображаются в полном объеме. Клиенты удаленного средства просмотра могут разрешить пользователям удалять сообщения перед их загрузкой. 
  
## <a name="to-retrieve-the-headers-of-messages-stored-remotely"></a>Извлечение заголовков сообщений, сохраненных удаленно
  
1. Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к таблице состояния. 
    
2. Call [IMAPITable:: Ограничьте](imapitable-restrict.md) для ограничения таблицы состояния только теми строками, для которых в **столбце\_тип\_ресурса PR** ([PidTagResourceType](pidtagresourcetype-canonical-property.md)) задано значение\_"\_поставщик транспорта MAPI". 
    
3. Call [IMAPITable:: метода SetColumns](imapitable-setcolumns.md) , чтобы включить следующие столбцы в таблицу состояния: 
   - **Идентификатор\_EntryID** ([PidTagEntryId](pidtagentryid-canonical-property.md))
   - **Методы\_ресурсов\_PR** ([PidTagResourceMethods](pidtagresourcemethods-canonical-property.md))
   - **Тип\_ресурса\_PR**, **дисплей\_поставщика\_PR** ([PidTagProviderDisplay](pidtagproviderdisplay-canonical-property.md))
   - **Код\_состояния\_** ([PidTagStatusCode](pidtagstatuscode-canonical-property.md)).
    
4. ВыЗовите [хркуеряллровс](hrqueryallrows.md) для получения всех строк в таблице Status. 
    
5. Передайте идентификатор записи для каждой строки в таблице при вызове [IMAPISession:: OpenEntry](imapisession-openentry.md). Так как этот интерфейс маршалируется из контекста процесса диспетчера очереди MAPI в контекст процесса клиента, в отличие от интерфейсов, обычно получаемых из адресной книги или поставщиков хранилищ сообщений, проблемы с многопоточностью имеют более высокую важность. 
    
6. ВыЗовите метод [IUnknown:: QueryInterface](https://msdn.microsoft.com/library/54d5ff80-18db-43f2-b636-f93ac053146d.aspx) объекта status, передав иид_имапифолдер в качестве идентификатора интерфейса, чтобы получить удаленную папку. Удаленная папка не является полной реализацией папки; Он поддерживает только подмножество методов и свойств папки. Один из обязательных методов, [IMAPIProp:: PROPS](imapiprop-getprops.md), поддерживает извлечение следующих свойств:
    
    |||
    |:-----|:-----|
    |**Доступ\_по пр** ([PidTagAccess](pidtagaccess-canonical-property.md))  <br/> |**Пр_акцесс_левел** ([PidTagAccessLevel](pidtagaccesslevel-canonical-property.md))  <br/> |
    |**Пр_контент_каунт** ([PidTagContentCount](pidtagcontentcount-canonical-property.md))  <br/> |**Пр_ассок_контент_каунт** ([PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md))  <br/> |
    |**Пр_фолдер_типе** ([PidTagFolderType](pidtagfoldertype-canonical-property.md))  <br/> |**Пр_обжект_типе** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))  <br/> |
    |**ВЛОЖЕНные папки PR\_** ([PidTagSubfolders](pidtagsubfolders-canonical-property.md))  <br/> |**Пр_креатион_тиме** ([PidTagCreationTime](pidtagcreationtime-canonical-property.md))  <br/> |
    |**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))  <br/> |
    
    Удаленные папки также должны поддерживать методы [IMAPIProp:: жетпроплист](imapiprop-getproplist.md), [IMAPIContainer:: жетконтентстабле](imapicontainer-getcontentstable.md)и [IMAPIFolder:: сетмессажестатус](imapifolder-setmessagestatus.md) . Таблицы содержимого удаленной папки обычно поддерживают следующие столбцы: 
        
    |||
    |:-----|:-----|
    |**\_Дисплей\_(пр** ) ([PidTagDisplayTo](pidtagdisplayto-canonical-property.md))  <br/> |**Идентификатор\_EntryID (пр)** <br/> |
    |**PR\_хасаттач** ([PidTagHasAttachments](pidtaghasattachments-canonical-property.md))  <br/> |**Пр_импортанце** ([PidTagImportance](pidtagimportance-canonical-property.md))  <br/> |
    |**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |**Пр_мессаже_класс** ([PidTagMessageClass](pidtagmessageclass-canonical-property.md))  <br/> |
    |**PR\_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md))  <br/> |**Пр_мессаже_флагс** ([PidTagMessageFlags](pidtagmessageflags-canonical-property.md))  <br/> |
    |**PR\_мессаже_довнлоад_тиме** ([PidTagMessageDownloadTime](pidtagmessagedownloadtime-canonical-property.md))  <br/> |**Пр_мессаже_сизе** ([PidTagMessageSize](pidtagmessagesize-canonical-property.md))  <br/> |
    |**Пр_мсг_статус** ([PidTagMessageStatus](pidtagmessagestatus-canonical-property.md))  <br/> |**ПР_ОБЖЕКТ_ТИПЕ** <br/> |
    |**Пр_нормализед_субжект** ([PidTagNormalizedSubject](pidtagnormalizedsubject-canonical-property.md))  <br/> |**Пр_приорити** ([PidTagPriority](pidtagpriority-canonical-property.md))  <br/> |
    |**Пр_сендер_наме** ([PidTagSenderName](pidtagsendername-canonical-property.md))  <br/> |**Пр_сенситивити** ([PidTagSensitivity](pidtagsensitivity-canonical-property.md))  <br/> |
    |**PR\_сент_репресентинг_наме** ([PidTagSentRepresentingName](pidtagsentrepresentingname-canonical-property.md))  <br/> |**Пр_субжект** ([PidTagSubject](pidtagsubject-canonical-property.md))  <br/> |
   
7. ВыЗовите метод [имапистатус:: валидатестате](imapistatus-validatestate.md) поставщика транспорта в первый раз, когда один из вариантов передачи выбран. Установите флаг процесса РЕФРЕШ_КСП_ХЕАДЕР_КАЧЕ или ПРОЦЕСС_КСП_ХЕАДЕР_КАЧЕ, а также флаг ШОВ_КСП_ССЕССИОН_УИ, чтобы разрешить отображение пользовательского интерфейса. 
    
   > [!NOTE]
   > Чтобы пометить определенный заголовок сообщения для загрузки или удаления, клиент вызывает [IMAPIFolder:: сетмессажестатус](imapifolder-setmessagestatus.md) и ЗАДАЕТ флаг МСГСТАТУС_РЕМОТЕ_ДОВНЛОАД или мсгстатус_ремоте_делете. 
  

