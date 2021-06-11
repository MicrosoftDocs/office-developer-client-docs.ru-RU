---
title: Скрыть свойство параметра Обновления собрания
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
# <a name="hide-meeting-update-option-property"></a>Скрыть свойство параметра Обновления собрания

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Скрывает возможность отправки обновлений собраний только добавленным или удаленным участникам.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Выставлено на:  <br/> |[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик магазинов  <br/> |
|Доступ к ним:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Тип доступа:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства. Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"urn:schemas-microsoft-com:office:outlook#allornonemtupdatedlg"  <br/> |
   
Поставщик магазина, использующий сервер для отправки обновлений собраний, может изменить диалоговое окно Отправка обновления **участникам.** Эта функция полезна, так как при отправке обновления собрания сервер не знает, какие участники были добавлены или удалены пользователем после первоначального запроса собрания. Если это свойство **верно,** обновление **Отправка** только для добавленных или удаленных участников не отображается в диалоговом окне **Отправка** обновления участникам. 
  
Это свойство игнорируется, если версия Outlook более ранней Microsoft Office Outlook 2003 Пакет обновления 1, или если его значение является **ложным.**
  

