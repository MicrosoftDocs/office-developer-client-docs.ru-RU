---
title: Скрытие свойства параметра обновления собрания
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- Hide Meeting Update Option Property
api_type:
- COM
ms.assetid: 9e7b413f-a88a-a4ec-8d57-1f3058cce4a4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac7c891fa05560231a257f9bd52ccbbfe564b49d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412102"
---
# <a name="hide-meeting-update-option-property"></a>Скрытие свойства параметра обновления собрания

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Скрывает параметр отправки обновлений собрания только добавленным или удаленным участникам.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|В:  <br/> |[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик магазина  <br/> |
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
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#allornonemtgupdatedlg"  <br/> |
   
Поставщик магазина, использующий сервер для отправки обновлений собрания, может изменить диалоговое окно "Отправить обновление **участникам".** Эта функция полезна, так как при отправке сервером обновления собрания серверу не известно, какие участники были добавлены или удалены пользователем с момента первоначального запроса на собрание. Если это свойство имеет  свойство **true,** параметр "Отправить обновление только добавленным или удаленным участникам" не отображается в диалоговом окне "Отправить обновление **участникам".** 
  
Это свойство игнорируется, если версия Outlook является более ранней, чем Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение **false**.
  

