---
title: Каноническое свойство PidLidSharingInitiatorEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingInitiatorEntryId
api_type:
- COM
ms.assetid: 47f00706-83df-49cb-bda7-ef572d76a020
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bfe682fc3263278c6e1d02a29a8b6432f41ac79e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309529"
---
# <a name="pidlidsharinginitiatorentryid-canonical-property"></a>Каноническое свойство PidLidSharingInitiatorEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Обозначается как свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingInitiatorEid  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x00008A09  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Общий доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Этому свойству должно быть задано значение свойства **PR_ENTRYID** ([PidTagEntryId)](pidtagentryid-canonical-property.md)для адресной книги во время входа пользователя (см. [[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXSHARE]](https://msdn.microsoft.com/library/e4e5bd27-d5e0-43f9-a6ea-550876724f3d%28Office.15%29.aspx)
  
> Папки почтовых ящиков разделяются между клиентами.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

