---
title: Каноническое свойство PidLidSpamOriginalFolder
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidSpamOriginalFolder
api_type:
- COM
ms.assetid: 45846fe3-7ab3-4019-98bb-fe615889c31c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 561008782e7c1ffb8bc71cf4e3bc17befe69bbca
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331558"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>Каноническое свойство PidLidSpamOriginalFolder

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Указывает, в какой папке было отправлено сообщение до его фильтрации в папку нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSpamOriginalFolder  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный ИД (КРЫШКА):  <br/> |0x0000859C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Спам  <br/> |
   
## <a name="remarks"></a>Примечания

Значением этого свойства является **EntryID** папки, которая содержала сообщение перед его перемещением. Это свойство следует устанавливать, если сообщение помечено как нежелательное. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешающих и заблокированных сообщений, а также определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

