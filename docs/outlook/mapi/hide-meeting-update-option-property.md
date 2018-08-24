---
title: Свойство параметра для скрытия обновления собрания
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
ms.openlocfilehash: 65255e14fd849d730e92bd86027642eef2c687bc
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22584977"
---
# <a name="hide-meeting-update-option-property"></a>Свойство параметра для скрытия обновления собрания

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Скрывает отправка обновлений встреч только добавленным или удаленным участникам.
  
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
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #allornonemtgupdatedlg»  <br/> |
   
Поставщик хранилища, которое использует сервер для отправки обновлений встреч можно изменить диалоговое окно **Отправить обновление участникам** . Эта функция полезна, так как при сервер отправляет обновление собрания, сервер не знаете, какие участники были добавлены или удалены пользователем, начиная с начального приглашения на собрание. Если это свойство имеет **значение true**, параметр **Отправить обновления только добавленным или удаленным участникам** не отображается в диалоговом окне **Отправить обновление участникам** . 
  
Это свойство игнорируется, если используется Outlook версии более ранней, чем пакет обновления 1 для Microsoft Office Outlook 2003 или имеет значение **false**.
  

