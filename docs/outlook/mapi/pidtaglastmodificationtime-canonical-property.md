---
title: Каноническое свойство PidTagLastModificationTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagLastModificationTime
api_type:
- HeaderDef
ms.assetid: a64e5300-6865-4588-8e1b-158cfd9c60c2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: dea709b457e28efef62718fc388621e01c4eb5bf
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32279711"
---
# <a name="pidtaglastmodificationtime-canonical-property"></a>Каноническое свойство PidTagLastModificationTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит дату и время последнего изменения объекта или подпроекта. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_LAST_MODIFICATION_TIME  <br/> |
|Идентификатор:  <br/> |0x3008  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Время сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Изначально этому свойству задается то же **значение, что** и для свойства PR_CREATION_TIME ([PidTagCreationTime).](pidtagcreationtime-canonical-property.md) Вложенные вложения могут обновлять его по мере необходимости, копируя время последнего изменения, поддерживаемые файловой системой. Клиентские приложения могут установить это свойство до первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) С этого времени поставщик должен обновлять **PR_LAST_MODIFICATION_TIME** во время каждого вызова **IMAPIProp::SaveChanges.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
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

