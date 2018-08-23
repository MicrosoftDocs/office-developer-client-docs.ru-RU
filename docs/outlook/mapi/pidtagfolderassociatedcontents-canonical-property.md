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
ms.openlocfilehash: ae09488b99cd55e5cfca23f504d81ac5919633d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574155"
---
# <a name="pidtagfolderassociatedcontents-canonical-property"></a>Каноническое свойство PidTagFolderAssociatedContents

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит объект внедренного содержимого таблицы, предоставляющий информацию о таблице связанного содержимого. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_FOLDER_ASSOCIATED_CONTENTS  <br/> |
|Идентификатор:  <br/> |0x3610  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Связанное содержимое таблицы представляет вложенной папке, которая не отображается в таблице стандартных содержимое. Она содержит папку связанного или скрытым, сообщения. 
  
Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции. Как свойство типа **PT_OBJECT**не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса **IID_IMAPITable** . Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если оно установлено, но может сообщать о его или не в том случае, если не указано. 
  
Для получения содержимого таблицы, клиентские приложения необходимо вызвать метод [IMAPIContainer::GetContentsTable](imapicontainer-getcontentstable.md) . Дополнительные сведения о таблицах содержимое папки просмотрите [Содержимое таблицы](contents-tables.md) и [Отображение Содержание папки](displaying-a-folder-contents-table.md). 
  
При использовании похожи **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md)) и это свойство. Несколько свойств MAPI предоставляют доступ к таблицы: 
  
|**Свойство**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Содержимое таблицы  <br/> |
|**PR_CONTAINER_HIERARCHY** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Таблица иерархии  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** <br/> |Связанное содержимое таблицы  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |В таблице вложений  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |В таблице получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](http://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания элементов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagAssociatedContentCount](pidtagassociatedcontentcount-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

