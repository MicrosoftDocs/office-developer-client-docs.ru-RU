---
title: Каноническое свойство PidLidSharingProviderUrl
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingProviderUrl
api_type:
- COM
ms.assetid: d217ab33-d697-4d27-a962-08d551d301f0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: eab12ef45846a8f58eb3cf327fbb40777010be7f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810541"
---
# <a name="pidlidsharingproviderurl-canonical-property"></a>Каноническое свойство PidLidSharingProviderUrl

  
  
**Относится к**: Outlook 
  
Указывает URL-адрес, связанные с общего доступа поставщика и заданной свойством **dispidSharingProviderGuid** ([PidLidSharingProviderGuid](pidlidsharingproviderguid-canonical-property.md)). Это свойство общего доступа сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingProviderUrl  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008A03  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство обычно используется, чтобы предоставить дополнительные сведения о поставщике общего доступа, но можно пропустить.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXSHARE]](http://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Открывает общий доступ папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

