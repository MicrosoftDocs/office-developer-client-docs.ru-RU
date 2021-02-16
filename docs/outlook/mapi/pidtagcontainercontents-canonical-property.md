---
title: Каноническое свойство PidTagContainerContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerContents
api_type:
- HeaderDef
ms.assetid: 66dbe65a-b9fd-41d5-946f-ec8888363043
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5f0717c2a6def6f99f1e53217764e8820125b79d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283130"
---
# <a name="pidtagcontainercontents-canonical-property"></a>Каноническое свойство PidTagContainerContents

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит встроенный объект таблицы содержимого, который предоставляет сведения о контейнере.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_CONTENTS  <br/> |
|Идентификатор:  <br/> |0x360F  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md) Свойство типа PT_OBJECT не может быть успешно извлечено методом [IMAPIProp::GetProps;](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса. Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен. 
  
Чтобы получить содержимое таблицы, клиентские приложения должны вызвать [метод IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) For more information, see [���������� �������](contents-tables.md). 
  
Это **свойство, PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)похожи в использовании. Доступ к таблицам предоставляется несколькими свойствами MAPI: 
  
|**Property**|**Table**|
|:-----|:-----|
|PidTagContainerContents  <br/> |Таблица Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)  <br/> |Таблица Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents)](pidtagfolderassociatedcontents-canonical-property.md)  <br/> |Связанная таблица содержимого  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)  <br/> |Таблица Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)  <br/> |Таблица Recipient  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
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

