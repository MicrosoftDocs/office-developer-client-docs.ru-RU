---
title: Каноническое свойство PidLidSharingResponseType
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingResponseType
api_type:
- COM
ms.assetid: c27b1239-3612-4bb3-9f22-4b89ee9900cd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a645ee26b56355c6594f5667585becbcff2e3eec
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810557"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Каноническое свойство PidLidSharingResponseType

  
  
**Относится к**: Outlook 
  
Указывает тип ответа, с которого ответили получателя запрос общий доступ. Это свойство общего доступа сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingResponseType  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008A27  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства необходимо задать одно из следующих значений:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Нет ответа  <br/> |
|0x00000001  <br/> |Принято  <br/> |
|0x00000002  <br/> |Запрещен  <br/> |
   
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
