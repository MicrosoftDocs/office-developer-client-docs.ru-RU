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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32358893"
---
# <a name="pidlidsharingcapabilities-canonical-property"></a>Каноническое свойство PidLidSharingCapabilities

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Обозначается как свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingCaps  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A17  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть заданной для одного из следующих значений:
  
|**Значение**|**Сценарий**|
|:-----|:-----|
|0x00040290  <br/> |Этот объект Обмена сообщениями относится к специальной папке.  <br/> |
|0x000402B0  <br/> |Этот объект общего доступа к сообщению не относится к специальной папке.  <br/> |
   
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

