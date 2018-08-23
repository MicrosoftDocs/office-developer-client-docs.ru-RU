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
ms.openlocfilehash: cc8ff946081fb7817f0f6018acefbe31293a13a0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581778"
---
# <a name="crawlsourcesupportmask"></a>CrawlSourceSupportMask

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Указывает, будет ли Microsoft Office Outlook необходимо сканировать папки хранилища, включая папки контактов, календаря и задач, при загрузке системы для заполнения области навигации.
  
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
|Kind.lpwstrName:  <br/> |L «CrawlSourceSupportMask»  <br/> |
   
Это свойство позволяет поставщиков хранилища указать, должна ли Outlook сканировать различных папок в хранилище. Используется при запуске Outlook проверок существующие папки для каждого открытого хранилища для заполнения области **переходов** ; Outlook проверяет наличие и значение этого свойства для хранилища перед началом сканирования. 
  
По умолчанию это свойство не доступен для хранилища, это значит, что Outlook поддерживает сканирование папок в хранилище. Если свойство предоставляется, ниже приведены возможные значения:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook поддерживает сканирование папок в хранилище.
    
CSM_DO_NOT_CRAWL
  
- Outlook не следует сканировать папок в хранилище.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Не разрешать клиентов для изменения этого свойства в хранилище. Обратите внимание на то, что константу **CSM_CLIENT_DO_NOT_CHANGE** является для последующего использования и не реализованы в настоящее время. Теперь хранилище можно запретить изменять этот флаг, жестко значение, которое возвращает хранилище для этого свойства клиентов. 
    

