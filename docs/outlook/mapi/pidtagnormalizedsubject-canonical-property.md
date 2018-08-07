---
title: Каноническое свойство PidTagNormalizedSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagNormalizedSubject
api_type:
- HeaderDef
ms.assetid: 2000e6e8-d908-4814-8093-28f8011250c8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 74061f33a88dceb371cad00ef44f611b583f7ae2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811403"
---
# <a name="pidtagnormalizedsubject-canonical-property"></a>Каноническое свойство PidTagNormalizedSubject

  
  
**Относится к**: Outlook 
  
Тема сообщения содержит с любой префикс удалены.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_NORMALIZED_SUBJECT, PR_NORMALIZED_SUBJECT_A, PR_NORMALIZED_SUBJECT_W  <br/> |
|Идентификатор:  <br/> |0x0E1D  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства вычисляются с хранилищем сообщений или поставщиками из свойства **PR_SUBJECT_PREFIX** ([PidTagSubjectPrefix](pidtagsubjectprefix-canonical-property.md)) и **PR_SUBJECT** ([PidTagSubject](pidtagsubject-canonical-property.md)) транспорта следующим образом.
  
- Если **PR_SUBJECT_PREFIX** этот параметр указан и совпадает с началом из **PR_SUBJECT**, **PR_NORMALIZED_SUBJECT** и связанные свойства устанавливаются содержимое **PR_SUBJECT** с удаленным префиксом. 
    
- Если **PR_SUBJECT_PREFIX** этот параметр указан, но не является первоначальной подстроки из **PR_SUBJECT**, **PR_SUBJECT_PREFIX** удаления и перерасчете из **PR_SUBJECT** с помощью следующее правило: Если строка содержатся в **PR_SUBJECT** начинается с один-три буквенные символы, за которым следует двоеточие и пробелами, вместе с двоеточием и пустой строки становится префикса. Символы чисел, пробелов и знаков препинания не допустимый префикс символов. 
    
- Если **PR_SUBJECT_PREFIX** не существует, он вычисляется из **PR_SUBJECT** с помощью правила, описанные в предыдущем шаге. Это свойство затем присваивается содержимое **PR_SUBJECT** с удаленным префиксом. 
    
 **Примечание** При **PR_SUBJECT_PREFIX** — это пустая строка, **PR_SUBJECT** и это свойство, совпадают. 
  
В конечном счете это свойство должно быть частью **PR_SUBJECT** следующий префикс. Если префикс отсутствует, это свойство становится таким же, как **PR_SUBJECT**.
  
 Как часть реализации [IMAPIProp::SaveChanges](imapiprop-savechanges.md) следует вычисляемые **PR_SUBJECT_PREFIX** и это свойство. Клиентское приложение не может запрашивать пользователя метод [IMAPIProp::GetProps](imapiprop-getprops.md) для их значения, пока они не зафиксированы вызовом **IMAPIProp::SaveChanges** . 
  
Свойства темы — это обычно коротких строк менее 256 символов и поставщика хранилища сообщений не обязаны поддерживают интерфейс объекта связывания и внедрения (OLE) **IStream** на них. Клиент должен всегда сначала попытаться доступ через интерфейс **IMAPIProp** и прибегать к **IStream** только в том случае, если возвращается MAPI_E_NOT_ENOUGH_MEMORY. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для контакты и списки рассылки.
    
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

