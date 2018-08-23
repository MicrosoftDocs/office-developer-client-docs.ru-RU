---
title: Свойство отображения размеров папок на сервере
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Display Server Folder Sizes Property
api_type:
- COM
ms.assetid: 38429fdb-be93-213a-a780-80f9837f55fa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f1ec10bde39f853a80540b48216478edc4e41f12
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584312"
---
# <a name="display-server-folder-sizes-property"></a>Свойство отображения размеров папок на сервере

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Отображает размеры указанных папках на сервере в диалоговом окне Outlook **Размер папки** . 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Предоставляется для:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект  <br/> |
|Созданные:  <br/> |Поставщик хранения  <br/> |
|Чтобы открыть:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Тип доступа:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство. Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства. 
  
Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #serverfoldersizes»  <br/> |
   
Это свойство поддерживается в Microsoft Outlook 2003 с пакетом обновления (SP) 1. Если используется Outlook версии более ранней, чем Outlook 2003 пакет обновления 1 или имеет значение **false**, Outlook будут отображаться только размеры папок локального хранилища. Если это свойство задано для хранилища, который использует Outlook 2003 SP 1, Outlook будет запрашивать размер каждой указанной папке на локальном диске и серверы. 
  
Для отправки запросов о размер папки на сервере, Outlook откроется в папку на хранилище с [IMsgStore::OpenEntry](imsgstore-openentry.md), передав флаг **MAPI_NO_CACHE**, и затем отправляет запрос для **PR_MESSAGE_SIZE_EXTENDED**. Затем поставщик хранения должен возвращать размер папки на сервере.
  
Чтобы запросить размер в папку на локальном диске, Outlook откроется в папку без флага **MAPI_NO_CACHE** . Он затем выполняется запрос **PR_MESSAGE_SIZE_EXTENDED**; поставщик хранения должен возвращать размер указанную папку на локальном диске.
  
С помощью этого набора свойств поставщики хранилища, синхронизировать содержимое хранилища на сервере можно отобразить данных размер папки на сервере в диалоговом окне Outlook **Размер папки** . Пользователи могут сравнить их текущего использования хранилища сервера с квоты сервера. 
  

