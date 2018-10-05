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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25385335"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Каноническое свойство PidTagContainerHierarchy

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит объект таблицы внедренных иерархии, предоставляющий информацию о дочерних контейнеров. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_HIERARCHY  <br/> |
|Идентификатор:  <br/> |0x360E  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Контейнер  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции. Как свойство типа **PT_OBJECT**не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающего идентификатор интерфейса IID_IMAPITable. Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если он имеет значение, но при необходимости можно сообщить или не в том случае, если он не установлен. 
  
Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md) . Для получения дополнительных сведений см [Таблиц иерархии](hierarchy-tables.md). 
  
 **PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), а это свойство похожи в использовании. Несколько свойств MAPI предоставляют доступ к таблицы: 
  
|**Свойство**|**Table**|
|:-----|:-----|
|**PR_CONTAINER_CONTENTS** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Содержимое таблицы  <br/> |
|**PR_CONTAINER_HIERARCHY** <br/> |Таблица иерархии  <br/> |
|**PR_FOLDER_ASSOCIATED_CONTENTS** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Связанное содержимое таблицы  <br/> |
|**PR_MESSAGE_ATTACHMENTS** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |В таблице вложений  <br/> |
|**PR_MESSAGE_RECIPIENTS** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |В таблице получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447 и встречи и собрания объекты.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

