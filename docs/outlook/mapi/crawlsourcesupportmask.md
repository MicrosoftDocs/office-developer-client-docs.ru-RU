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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, следует ли Microsoft Office Outlook сканировать папки в хранилище, включая папки Контакты, календарь и задачи, при запуске, чтобы заполнить область навигации.
  
## <a name="quick-info"></a>Краткие сведения

|||
|:-----|:-----|
|Предоставлено:  <br/> |[IMsgStore: объект IMAPIProp](imsgstoreimapiprop.md)  <br/> |
|Создано:  <br/> |Поставщик хранилища  <br/> |
|Доступ:  <br/> |Outlook и другие клиенты  <br/> |
|Тип свойства:  <br/> |PT_LONG  <br/> |
|Тип доступа:  <br/> |Только чтение или чтение и запись в зависимости от поставщика услуг хранения  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы обеспечить какую бы то ни было функцию хранилища, поставщик магазина должен реализовать [IMAPIProp: IUnknown](imapipropiunknown.md) и вернуть допустимый тег свойства для любого из этих свойств, переданного в вызов [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) . Когда тег свойства для любого из этих свойств передается в [IMAPIProp::-PROPS](imapiprop-getprops.md), поставщик хранилища также должен возвращать правильное значение свойства. Поставщики хранилища могут вызывать [хржетонепроп](hrgetoneprop.md) и [хрсетонепроп](hrsetoneprop.md) для получения или задания этих свойств. 
  
Чтобы получить значение этого свойства, клиент должен сначала использовать [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) , чтобы получить Тег Property, а затем указать этот тег свойства в [IMAPIProp:: Prop](imapiprop-getprops.md) для получения значения. При вызове [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)укажите следующие значения для структуры [мапинамеид](mapinameid.md) , на которую указывает входный параметр _лпппропнамес_:
  
|||
|:-----|:-----|
|Лпгуид:  <br/> |PSETID_Common  <br/> |
|Улкинд:  <br/> |MNID_STRING  <br/> |
|Тип. Лпвстрнаме:  <br/> |L "Кравлсаурцесуппортмаск"  <br/> |
   
Это свойство позволяет поставщикам услуг магазина указывать, следует ли Outlook сканировать различные папки в хранилище. Он используется при запуске, когда Outlook сканирует существующие папки в каждом открытом хранилище для заполнения области **навигации** ; Перед началом сканирования Outlook проверяет наличие и значение этого свойства в хранилище. 
  
По умолчанию это свойство не отображается в хранилище, что означает, что Outlook может сканировать папки в хранилище. Если свойство предоставлено, могут быть доступны следующие значения:
  
```
enum { 
 CSM_DEFAULT              = 0, 
 CSM_DO_NOT_CRAWL         = 1 << 0x0, 
 CSM_CLIENT_DO_NOT_CHANGE = 1 << 0xF 
};
```

CSM_DEFAULT
  
- Outlook может сканировать папки в хранилище.
    
CSM_DO_NOT_CRAWL
  
- Outlook не должен сканировать папки в хранилище.
    
CSM_CLIENT_DO_NOT_CHANGE
  
- Не разрешать клиентам изменять это свойство в хранилище. Обратите внимание, что константа **CSM_CLIENT_DO_NOT_CHANGE** предназначена для использования в будущем и в настоящее время не реализована. Пока хранилище может запретить клиентам изменять этот флаг, хардкодинг значение, которое возвращает магазин для этого свойства. 
    

