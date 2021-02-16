---
title: Make Store Type Private Property
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Make Store Type Private Property
api_type:
- COM
ms.assetid: 7f489f55-46d4-8a88-6ebe-9db6446e69a5
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: da55afcabb1354959a71d6f10472c05540427b19
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428545"
---
# <a name="make-store-type-private-property"></a>Make Store Type Private Property

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обрабатывает вторичное хранилище как частное.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|В:  <br/> |[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик магазина  <br/> |
|Доступ к нему можно получить с помощью:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Тип доступа:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы предоставить любую функциональность магазина, поставщик магазина должен реализовать [IMsgStore : IMAPIProp](imsgstoreimapiprop.md) и вернуть действительный тег свойства для любого из этих свойств, переданных в вызов [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Когда тег свойства для любого из этих свойств передается в [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства. Поставщики магазина могут вызывать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или настроить эти свойства. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#storetypeprivate"  <br/> |
   
Поставщик магазина может использовать это свойство, чтобы Outlook обрабатывал его как личное, когда это дополнительное хранилище для пользователя. 
  
По умолчанию Outlook обрабатывает дополнительное хранилище так же, как хранилище делегатов, а элементы в дополнительном хранилище являются частными, только если пользователь пометит их как частные. Если это свойство имеет **значение true,** элементы, удаленные из дополнительного магазина, перемещаются в папку **"Удаленные"** в основном хранилище. Элементы, помеченные как частные, не отображаются. Черновики хранятся в папке "Черновики" в основном хранилище. 
  
Это свойство игнорируется, если версия Outlook является более ранней, чем Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение **false**.
  

