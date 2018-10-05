---
title: Каноническое свойство PidTagRoamingBinary
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: f06bf063-fc95-46f9-b5fa-3f127a59ebda
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ead7c9c33c92240ba5e458b68635b766caaa9760
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401673"
---
# <a name="pidtagroamingbinary-canonical-property"></a>Каноническое свойство PidTagRoamingBinary

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит поток сообщений, связанных с подкласс **IPM. Конфигурация** класса. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROAMING_BINARYSTREAM  <br/> |
|Идентификатор:  <br/> |0x7C09  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Конфигурация  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство содержит поток данных, связанных с **IPM. Конфигурация** сообщение класс сообщения. Формат потока зависит от класса сообщения. Например сообщение типа класса **IPM. Configuration.Autocomplete** может быть в формате [потока автозаполнения](autocomplete-stream.md).
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

