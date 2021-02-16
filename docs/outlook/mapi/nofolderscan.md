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
ms.openlocfilehash: fc5f5a42e2b1e57374ff80a9333b927cc8dba120
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436813"
---
# <a name="nofolderscan"></a>NoFolderScan

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли Microsoft Office Outlook сканировать папки "Контакты" в хранилище.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|В:  <br/> |[IMsgStore : объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик store  <br/> |
|Доступ к нему можно получить с помощью:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тип доступа:  <br/> |Только для чтения или чтения и записи в зависимости от поставщика магазина  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы предоставить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть действительный тег свойства для любого из этих свойств, переданных в вызов [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Когда тег свойства для любого из этих свойств передается в [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства. Поставщики магазина могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или настроить эти свойства. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает входной параметр _lppPropNames:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"NoFolderScan"  <br/> |
   
Это свойство позволяет поставщикам магазина указывать Outlook, чтобы не сканировать папки "Контакты" в хранилище, чтобы избежать ухудшения производительности. Он используется в операциях слияния почты, во время которых Outlook проверяет наличие и значение этого свойства перед началом проверки.
  
По умолчанию это свойство не выставит в магазине, что означает, что Outlook может сканировать папку "Контакты" в магазине. Если свойство имеется, возможны следующие значения:
  
- Ноль (0): Outlook может выполнять сканирование.
    
- Ненулевые значения: Outlook не должен сканировать папки "Контакты" в магазине.
    

