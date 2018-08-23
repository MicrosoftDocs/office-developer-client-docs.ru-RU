---
title: NoFolderScan
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 4949aef9-4c96-82cc-cd13-57981e07cc40
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3416bc50e4628df2be09f9fe1a22d19530bcdff8
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578054"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, будет ли Microsoft Office Outlook необходимо сканировать папки Контакты для хранилища.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Предоставляется для:  <br/> |[IMsgStore: IMAPIProp](imsgstoreimapiprop.md) объект  <br/> |
|Созданные:  <br/> |Поставщик хранения  <br/> |
|Чтобы открыть:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тип доступа:  <br/> |Только чтение или чтение и запись в зависимости от поставщика хранилища  <br/> |
   
## <a name="remarks"></a>Замечания

Для обеспечения какие-либо функциональные возможности хранения, необходимо реализовать поставщика хранилища [IMAPIProp: IUnknown](imapipropiunknown.md) и возврата тег допустимым свойством для каких-либо из этих свойств, переданной в вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) . При передаче тега свойства для каких-либо из этих свойств в [IMAPIProp::GetProps](imapiprop-getprops.md), поставщик хранения также должен возвращать значение правильное свойство. Поставщики хранилища можно вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp](hrsetoneprop.md) , чтобы получить или задать эти свойства. 
  
Чтобы получить значение этого свойства, клиента следует сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства и укажите этот тег свойства в [IMAPIProp::GetProps](imapiprop-getprops.md) для получения значения. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md), укажите следующие значения для структуры [MAPINAMEID](mapinameid.md) , на которую указывает входного параметра _lppPropNames_.
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L «NoFolderScan»  <br/> |
   
Это свойство предоставляет способ для хранения поставщиков для указания в Outlook не сканировать папки Контакты в хранилище, чтобы предотвратить снижение производительности. Она используется в операции слияния почты, во время которых Outlook проверяет наличие и значение этого свойства перед началом сканирования.
  
По умолчанию это свойство не предоставляется для хранилища, это значит, что Outlook поддерживает сканирование папки Контакты в хранилище. Если свойство предоставляется, ниже приведены возможные значения:
  
- Нуль (0): Outlook можно выполнить проверку.
    
- Ненулевое значение: Outlook не следует сканировать списка контактов пользователя в хранилище.
    

