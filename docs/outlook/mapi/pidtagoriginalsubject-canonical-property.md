---
title: Каноническое свойство PidTagOriginalSubject
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSubject
api_type:
- COM
ms.assetid: 8668ba4f-3236-4a87-a5aa-9cf7eea3d87b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: de957c33165cc96eec82bf95c8f292c5b323676a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331145"
---
# <a name="pidtagoriginalsubject-canonical-property"></a>Каноническое свойство PidTagOriginalSubject

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит тему исходного сообщения для использования в отчете о сообщении.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SUBJECT, PR_ORIGINAL_SUBJECT_A, PR_ORIGINAL_SUBJECT_W  <br/> |
|Идентификатор:  <br/> |0x0049  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства изначально задают то же значение, что **и PR_SUBJECT** [(PidTagSubject).](pidtagsubject-canonical-property.md)
  
Свойства субъекта, как правило, являются небольшими строками менее 256 символов, и поставщик магазина сообщений не обязан поддерживать интерфейс **IStream,** связывающий объекты и встраив их. Клиент всегда должен сначала попытаться получить доступ через **интерфейс IMAPIProp** и прибегать к **IStream** только MAPI_E_NOT_ENOUGH_MEMORY **возвращается.** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые на объектах сообщений электронной почты.
    
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

