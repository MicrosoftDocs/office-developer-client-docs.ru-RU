---
title: Каноническое свойство PidTagViewDescriptorName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagViewDescriptorName
api_type:
- COM
ms.assetid: 1e689ee4-9e89-4328-beb9-05c80a6544a0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ab906d83ae4ad46747fd9037728620db1d656d25
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360727"
---
# <a name="pidtagviewdescriptorname-canonical-property"></a>Каноническое свойство PidTagViewDescriptorName

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя дескриптора представления.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_VD_NAME, PR_VD_NAME_A, PR_VD_NAME_W  <br/> |
|Идентификатор:  <br/> |0x7006  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Передаваемое сообщение с определенным классом сообщений  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства должны быть задаваемы непустой строке для сообщения о соударяемой информации о папке (FAI), содержащих определения представления.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

