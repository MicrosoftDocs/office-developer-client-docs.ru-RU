---
title: Каноническое свойство PidTagListHelp
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagListHelp
api_type:
- HeaderDef
ms.assetid: 403324b8-c992-4823-aa0f-0414b283debc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 588747205ee3922fef7b107dc024f074a6ee527e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279631"
---
# <a name="pidtaglisthelp-canonical-property"></a>Каноническое свойство PidTagListHelp

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение поля List-Help MIME.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LIST_HELP, PR_LIST_HELP_A, PR_LIST_HELP_W  <br/> |
|Идентификатор:  <br/> |0x1043  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы создать List-Help поля, клиенты должны установить  необходимое значение PR_LIST_HELP или связанного свойства. Авторы MIME должны скопировать это значение в List-Help загона. 
  
Чтобы установить значение этих свойств, связанных с сервером списков, клиенты MIME должны записать поля загона, как указано в следующей таблице:
  
|**Property**|**Предпочтительное имя поля для загона**|**Альтернативное имя поля загона**|
|:-----|:-----|:-----|
|**PR_LIST_HELP** <br/> |List-Help  <br/> |X-List-Help  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

