---
title: Каноническое свойство PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332860"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Каноническое свойство PidTagContainerHierarchy

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит встроенный объект таблицы иерархии, который предоставляет сведения о детских контейнерах. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Идентификатор:  <br/> |0x360E  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в [операциях IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в [операции IMAPIProp::CopyProps.](imapiprop-copyprops.md) Как свойство типа **PT_OBJECT,** его невозможно успешно получить [методом IMAPIProp::GetProps;](imapiprop-getprops.md) Его содержимое должно быть доступны [методом IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивая идентификатор IID_IMAPITable интерфейса. Поставщики услуг должны сообщить об этом [методу IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он за установлен, но может сообщить об этом или нет, если он не установлен. 
  
Чтобы получить содержимое таблицы, клиентская заявка должна вызвать [метод IMAPIContainer::GetHierarchyTable.](imapicontainer-gethierarchytable.md) Дополнительные сведения см. в [таблице Иерархия.](hierarchy-tables.md) 
  
 **PR_CONTAINER_CONTENTS** [(PidTagContainerContents),](pidtagcontainercontents-canonical-property.md) **PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents),](pidtagfolderassociatedcontents-canonical-property.md)и это свойство аналогично по использованию. Несколько свойств MAPI предоставляют доступ к таблицам: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** [(PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)  <br/> |Таблица контента  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Таблица иерархии  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** [(PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)  <br/> |Связанная таблица контента  <br/> |
|**PR_MESSAGE_ATTACHMENTS** [(PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)  <br/> |Таблица вложений  <br/> |
|**PR_MESSAGE_RECIPIENTS** [(PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)  <br/> |Таблица получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.
    
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

