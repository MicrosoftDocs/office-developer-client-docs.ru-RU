---
title: Каноническое свойство PidTagStoreEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagStoreEntryId
api_type:
- COM
ms.assetid: 0d705667-19f4-4eda-a068-e65ea8f00d9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ffe4798c5e8ef200619b060a58e868cc4a1b2bc2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22590073"
---
# <a name="pidtagstoreentryid-canonical-property"></a>Каноническое свойство PidTagStoreEntryId

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит уникальный идентификатор хранилища сообщений, где находится объект.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_STORE_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0FFB  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для открытия хранилища сообщений с помощью метода [IMAPISession::OpenMsgStore](imapisession-openmsgstore.md) . Он также используется для открытия любой объект, владельцем которого является хранилища сообщений. 
  
Для хранилища сообщений это свойство идентичен свойство магазина собственные **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)). Клиентское приложение позволяет сравнивать два свойства, с помощью метода [IMAPISession::CompareEntryIDs](imapisession-compareentryids.md) . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Открывает общий доступ папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

