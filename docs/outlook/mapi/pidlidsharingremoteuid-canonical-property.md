---
title: Каноническое свойство PidLidSharingRemoteUid
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSharingRemoteUid
api_type:
- COM
ms.assetid: cfe3b728-317b-4871-adea-e2fdf8441da7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c3e783934367ad7c5c1a9a760aa8a24525901832
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331264"
---
# <a name="pidlidsharingremoteuid-canonical-property"></a>Каноническое свойство PidLidSharingRemoteUid

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает ID записи удаленной папки, которая является общей. Это свойство общего сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSharingRemoteUid  <br/> |
|Набор свойств:  <br/> |PSETID_Sharing  <br/> |
|Long ID (LID):  <br/> |0x00008A06  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Доступ  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть задано для представления hexadecimal string значения свойства[PR_ENTRYID (PidTagEntryId)](pidtagentryid-canonical-property.md)в совместной папке. Это свойство общего сообщения.
  
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

