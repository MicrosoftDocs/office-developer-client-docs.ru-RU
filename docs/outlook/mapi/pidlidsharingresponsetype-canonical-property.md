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
ms.openlocfilehash: 34e8a3c73715a75b8007646e5ba3b0dc3e1ae919
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331194"
---
# <a name="pidlidsharingresponsetype-canonical-property"></a>Каноническое свойство PidLidSharingResponseType

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает тип ответа, на который ответил получатель запроса общего доступа. Это свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingResponseType  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A27  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть заданной одному из следующих значений:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Нет ответа  <br/> |
|0x00000001  <br/> |Accepted  <br/> |
|0x00000002  <br/> |Отклонено  <br/> |
   
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

