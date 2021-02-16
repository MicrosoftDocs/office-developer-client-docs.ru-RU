---
title: Display Server Folder Sizes Property
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
ms.openlocfilehash: 85a8b5216eac1dd4e4cebd1313cb31c9b5d70227
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434552"
---
# <a name="display-server-folder-sizes-property"></a>Display Server Folder Sizes Property

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Отображает размеры указанных папок на сервере в диалоговом окне "Размер **папки** Outlook". 
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|В:  <br/> |[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик store  <br/> |
|Доступ к нему можно получить с помощью:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Тип доступа:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы предоставить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть действительный тег свойства для любого из этих свойств, переданных в вызов [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Когда тег свойства для любого из этих свойств передается в [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства. Поставщики магазина могут вызывать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или настроить эти свойства. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#serverfoldersizes"  <br/> |
   
Это свойство поддерживается в Microsoft Outlook 2003 Пакет обновления (SP1). Если версия Outlook более ранга, чем Outlook 2003 с sp 1, или если ее значение **false,** Outlook будет отображать только размеры папок в локальном хранилище. Если это свойство установлено в хранилище, использующем Outlook 2003 с sp 1, Outlook будет запрашивать размер каждой указанной папки на сервере и локальном диске. 
  
Чтобы запросить размер папки на сервере, Outlook открывает в магазине папку с [IMsgStore::OpenEntry,](imsgstore-openentry.md)передает флаг **MAPI_NO_CACHE,** а затем запрашивает **PR_MESSAGE_SIZE_EXTENDED.** Затем поставщик магазина должен вернуть размер папки на сервере.
  
Чтобы запросить размер папки на локальном диске, Outlook открывает папку **без** MAPI_NO_CACHE флага. Затем он запрашивает **PR_MESSAGE_SIZE_EXTENDED;** Поставщик магазина должен вернуть размер указанной папки на локальном диске.
  
С помощью этого набора свойств поставщики содержимого, синхронизируются с сервером,  могут отображать данные о размере папки на сервере в диалоговом окне "Размер папки Outlook". Затем пользователи могут сравнить текущее использование хранилища сервера с квотами сервера. 
  

