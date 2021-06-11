---
title: CrawlSourceSupportMask
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- CrawlSourceSupportMask
api_type:
- COM
ms.assetid: d0a2f7ea-df6a-89e8-18c2-ac92e0a20edc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: cc3fcedb73b4acbd85529615d857403b4c268f3d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420915"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли Microsoft Office Outlook в магазине, включая папки Contacts, Calendar и Tasks, при запуске для заполнения области навигации.
  
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
|Kind.lpwstrName:  <br/> |L"CrawlSourceSupportMask"  <br/> |
   
Это свойство позволяет поставщикам магазинов указать, следует ли Outlook сканировать различные папки в магазине. Он используется при запуске, Outlook сканирует существующие папки в каждом открытом магазине для заполнения области **навигации;** Outlook проверить наличие и значение этого свойства в магазине перед началом проверки. 
  
По умолчанию это свойство не подвергается воздействию в магазине, что Outlook может проверять папки в магазине. Если свойство выставлено, возможные значения:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook можно сканировать папки в магазине.
    
CSM_DO_NOT_CRAWL
  
- Outlook не следует сканировать папки в магазине.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Не позволяйте клиентам изменять это свойство в магазине. Обратите внимание, **что CSM_CLIENT_DO_NOT_CHANGE** для будущей ссылки и в настоящее время не реализована. В настоящее время магазин может запретить клиентам изменять этот флаг, жестко задав значение, которое возвращает хранилище для этого свойства. 
    

