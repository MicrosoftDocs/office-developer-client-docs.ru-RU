---
title: Каноническое свойство PidTagIpmSubtreeEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmSubtreeEntryId
api_type:
- HeaderDef
ms.assetid: 5763fc78-5192-4162-be27-4aadc7ed65bc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 815685696dfc93bb6241f608ca0157e87e758e7b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412732"
---
# <a name="pidtagipmsubtreeentryid-canonical-property"></a>Каноническое свойство PidTagIpmSubtreeEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор корня поддерева папки межконтактного сообщения (IPM) в дереве папок хранилища сообщений. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ИПМ_СУБТРИ_ЕНТРИД  <br/> |
|Идентификатор:  <br/> |0x35E0  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство представляет корень иерархии IPM. Клиенты IPM не должны отображать папки, которые не являются подпапками папки, представленной этим свойством.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

