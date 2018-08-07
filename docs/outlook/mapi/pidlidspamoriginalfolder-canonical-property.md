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
ms.openlocfilehash: 4cb0243f38137afa820c3499a8b95954098bd6fc
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810566"
---
# <a name="pidlidspamoriginalfolder-canonical-property"></a>Каноническое свойство PidLidSpamOriginalFolder

  
  
**Относится к**: Outlook 
  
Указывает, какие папки сообщение находился до его было отфильтровано в папку нежелательной почты.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidSpamOriginalFolder  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x0000859C  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Нежелательной почты  <br/> |
   
## <a name="remarks"></a>Замечания

Значение этого свойства — это **идентификатор записи** для той папке, где сообщения до перемещения. Это свойство необходимо задать, когда сообщение помечено как нежелательная почта. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

