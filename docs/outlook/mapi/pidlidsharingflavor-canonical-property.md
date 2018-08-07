---
title: Каноническое свойство PidLidSharingFlavor
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingFlavor
api_type:
- COM
ms.assetid: c91ab5c7-82ac-4895-bf54-2863ca5e2410
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0333f0c309d89436c50a58124500f1b359584954
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810531"
---
# <a name="pidlidsharingflavor-canonical-property"></a>Каноническое свойство PidLidSharingFlavor

  
  
**Относится к**: Outlook 
  
Определяет, как свойство общего доступа сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingFlavor  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008A18  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Sharing  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства должно быть одно из следующих:
  
|**Значение**|**Тип объекта, общий доступ к сообщения**|
|:-----|:-----|
|0x00020310  <br/> |Приглашения на общий доступ для отдельной папки.  <br/> |
|0x00000310  <br/> |Приглашения на общий доступ к папке, которая не является отдельной папки.  <br/> |
|0x00020500  <br/> |Запрос на общий доступ.  <br/> |
|0x00020710  <br/> |Оба приглашения на общий доступ для отдельной папки и запрос на общий доступ для получателя соответствует специальную папку.  <br/> |
|0x00025100  <br/> |Общего доступа ответа, отклонения запроса.  <br/> |
|0x00023310  <br/> |Ответ общего доступа, принимает запрос (также тип приглашение для совместного использования).  <br/> |
   
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

