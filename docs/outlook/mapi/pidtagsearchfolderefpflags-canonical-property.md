---
title: Каноническое свойство PidTagSearchFolderEfpFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSearchFolderEfpFlags
api_type:
- COM
ms.assetid: ef82a75f-a09f-4880-ba6a-e739b16422a3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d670aa91cc60c051f8464f9d83536b888b44ca9e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32336430"
---
# <a name="pidtagsearchfolderefpflags-canonical-property"></a>Каноническое свойство PidTagSearchFolderEfpFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит расширенные флаги папок, которые применяются к контейнеру папки поиска для папки поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_WB_SF_EFP_FLAGS  <br/> |
|Идентификатор:  <br/> |0x6848  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно конкретно содержать флаги в **свойстве PR_EXTENDED_FOLDER_FLAGS** [(PidTagExtendedFolderFlags)](pidtagextendedfolderflags-canonical-property.md)и под-свойство **ExtendedFlags** в поле b для папки. Сведения о флагах папок см. [в [MS-OXOCFG].](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Указывает свойства и операции для управления конфигурацией списка папки поиска.
    
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

