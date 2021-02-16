---
title: Каноническое свойство PidTagFolderAssociatedContents
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagFolderAssociatedContents
api_type:
- HeaderDef
ms.assetid: d1f3f589-dc2d-4538-a13f-278dad29bcc7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c85c5d7c3e80508c4d328f69ac4ad15f0f2c355a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316305"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Каноническое свойство PidTagFolderAssociatedContents

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит встроенный объект таблицы содержимого, который предоставляет сведения о связанной таблице содержимого. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Идентификатор:  <br/> |0x3610  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Связанная таблица содержимого представляет в подчиненную, которая не появляется в стандартной таблице содержимого. Он содержит связанные или скрытые сообщения папки. 
  
Это свойство можно исключить в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) или включить в операции [IMAPIProp::CopyProps.](imapiprop-copyprops.md) В качестве свойства типа **PT_OBJECT** его невозможно получить с помощью метода [IMAPIProp::GetProps;](imapiprop-getprops.md) Доступ к его содержимому должен получить метод [IMAPIProp::OpenProperty,](imapiprop-openproperty.md) запрашивающий идентификатор IID_IMAPITable интерфейса.  Поставщики служб должны сообщить о нем методу [IMAPIProp::GetPropList,](imapiprop-getproplist.md) если он установлен, но при желании может сообщить о нем или нет, если он не за установлен. 
  
Чтобы получить содержимое таблицы, клиентские приложения должны вызывать метод [IMAPIContainer::GetContentsTable.](imapicontainer-getcontentstable.md) Дополнительные сведения о таблицах содержимого папок см. в таблицах "Содержимое" и "Отображение [](contents-tables.md) [таблицы содержимого папки".](displaying-a-folder-contents-table.md) 
  
The **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy),](pidtagcontainerhierarchy-canonical-property.md)and this property are similar in usage. Доступ к таблицам предоставляется несколькими свойствами MAPI: 
  
|**Property**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents)](pidtagcontainercontents-canonical-property.md)  <br/> |Таблица Contents  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy)](pidtagcontainerhierarchy-canonical-property.md)  <br/> |Таблица Hierarchy  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Связанная таблица содержимого  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments)](pidtagmessageattachments-canonical-property.md)  <br/> |Таблица Attachment  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients)](pidtagmessagerecipients-canonical-property.md)  <br/> |Таблица Recipient  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также элементами встреч и собраний.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

