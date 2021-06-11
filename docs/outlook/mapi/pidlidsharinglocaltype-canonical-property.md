---
title: Каноническое свойство PidLidSharingLocalType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingLocalType
api_type:
- COM
ms.assetid: 6ac438a1-d36f-424f-b4b4-d6f2d26fd350
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: aa1f76a3f410294de9c7ebfb3e64bbb1cd6cc25c
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336829"
---
# <a name="pidlidsharinglocaltype-canonical-property"></a>Каноническое свойство PidLidSharingLocalType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает значение свойства **PR_CONTAINER_CLASS** [(PidTagContainerClass)](pidtagcontainerclass-canonical-property.md)для совместной папки. Это свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingLocalType  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A14  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть одним из следующих:
  
- "IPF. Назначение"
    
- "IPF. Контакт"
    
- "IPF. Задача"
    
- "IPF. StickyNote"
    
- "IPF. Журнал"
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Делит папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

