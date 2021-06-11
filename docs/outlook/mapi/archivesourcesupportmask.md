---
title: ArchiveSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- ArchiveSourceSupportMask
api_type:
- COM
ms.assetid: e35216e0-c23f-70f2-0d5f-1ac5dc00fd8c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6fc5e8eb74d79d0a30ae6a423772ce741dee4562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418094"
---
# <a name="archivesourcesupportmask"></a>ArchiveSourceSupportMask

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли Microsoft Office Outlook сканировать папки в магазине и архивировать их автоматически.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Выставлено на:  <br/> |[Объект IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик магазинов  <br/> |
|Доступ к ним:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тип доступа:  <br/> |Только для чтения или чтения/записи в зависимости от поставщика магазина  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы обеспечить любую функциональность магазина, поставщик магазина должен реализовать [IMAPIProp : IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданных [вызову IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md) Когда тег свойства для любого из этих свойств передается [IMAPIProp::GetProps,](imapiprop-getprops.md)поставщик магазина также должен вернуть правильное значение свойства. Поставщики магазинов могут вызвать [HrGetOneProp](hrgetoneprop.md) и [HrSetOneProp,](hrsetoneprop.md) чтобы получить или установить эти свойства. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) для получения тега свойства, а затем указать этот тег свойства в [IMAPIProp::GetProps,](imapiprop-getprops.md) чтобы получить значение. При вызове [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [MAPINAMEID,](mapinameid.md) на которые указывает параметр _ввода lppPropNames:_
  
|||
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_STRING  <br/> |
|Kind.lpwstrName:  <br/> |L"ArchiveSourceSupportMask"  <br/> |
   
Это свойство позволяет поставщикам магазинов указывать, следует ли Outlook сканировать папки в магазине и архивировать их автоматически.
  
По умолчанию это свойство не подвергается воздействию в магазине, что Outlook может проверять папки в магазине. Если свойство выставлено, возможные значения:
  
```cpp
enum { 
 ASM_DEFAULT              = 0, 
 ASM_DO_NOT_ARCHIVE         = 1 << 0x0, 
 ASM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

ASM_DEFAULT
  
- Outlook можно сканировать папки в магазине.
    
ASM_DO_NOT_ARCHIVE
  
- Outlook не следует сканировать папки в магазине.
    
ASM_CLIENT_DO_NOT_CHANGE
  
- Не позволяйте клиентам изменять это свойство в магазине. Обратите внимание, **что ASM_CLIENT_DO_NOT_CHANGE** для будущей ссылки и в настоящее время не реализована. В настоящее время магазин может запретить клиентам изменять этот флаг, жестко задав значение, которое возвращает хранилище для этого свойства. 
    

