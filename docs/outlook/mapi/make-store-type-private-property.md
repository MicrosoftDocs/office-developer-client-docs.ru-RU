---
title: Свойство, делающее тип хранилища частным
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
ms.openlocfilehash: 7f60d9524af18bb7f2e876386c45b84f207d42bc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809691"
---
# <a name="make-store-type-private-property"></a>Свойство, делающее тип хранилища частным

  
  
**Относится к**: Outlook 
  
Рассматривается как закрытый дополнительного хранилища.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Предоставляется для:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект  <br/> |
|Созданные:  <br/> |Поставщик хранения  <br/> |
|Чтобы открыть:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_BOOLEAN  <br/> |
|Тип доступа:  <br/> |Чтение и запись  <br/> |
   
## <a name="remarks"></a>Замечания

Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMsgStore: IMAPIProp](imsgstoreimapiprop.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство. Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства. 
  
Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PS_PUBLIC_STRINGS  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L "urn: schemas-microsoft-com:office:outlook #storetypeprivate»  <br/> |
   
Это свойство можно использовать поставщика хранилища будет считать его закрытого при дополнительного хранилища для пользователя в Outlook. 
  
По умолчанию Outlook считает дополнительного хранилища так же, как делегат хранилища и элементов в хранилище дополнительного частной, только если им специально частных. Когда это свойство имеет **значение true**, элементы, удаленные из дополнительного хранилища перемещаются в папку " **Удаленные** " в основного хранилища. Личным не отображаются. «Черновики», хранятся в папке «Черновики» в основного хранилища. 
  
Это свойство игнорируется, если используется Outlook версии более ранней, чем пакет обновления 1 для Microsoft Office Outlook 2003 или имеет значение **false**.
  

