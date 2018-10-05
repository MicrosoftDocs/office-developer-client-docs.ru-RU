---
title: Каноническое свойство PidLidSharingCapabilities
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingCapabilities
api_type:
- COM
ms.assetid: 86b3eab2-2594-4204-aedf-8ce2ee3b81ce
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d44851e1c863cb117eed3462eb98de87f8d1f0be
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25388324"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a>Каноническое свойство PidLidSharingCapabilities

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Определяет, как свойство общего доступа сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingCaps  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008A17  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство должно быть задано одно из следующих значений:
  
|**Значение**|**Сценарий**|
|:-----|:-----|
|0x00040290  <br/> |Этот объект общего доступа к Message связана с особой папкой.  <br/> |
|0x000402B0  <br/> |Этот объект общего доступа к сообщения не связан специальную папку.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Открывает общий доступ папки почтовых ящиков между клиентами.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

