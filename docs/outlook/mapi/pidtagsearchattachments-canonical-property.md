---
title: Каноническое свойство PidTagSearchAttachments
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 534c3881-e12f-f228-7760-788fe2b72ae8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 80d1fc3f711369471eb2c1473700f13a6b995594
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578509"
---
# <a name="pidtagsearchattachments-canonical-property"></a>Каноническое свойство PidTagSearchAttachments

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит строку Юникод, запрашиваемый в содержимое вложения в хранилище.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_ATTACHMENTS_W  <br/> |
|Идентификатор:  <br/> |0x0EA5  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Поиск  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

> [!NOTE]
> Этот тег ограничений MAPI, используется при поиске содержимое вложения, не могут быть определены в файле загружаемых заголовка, который в настоящий момент. Добавьте в код с помощью следующее значение: >`#define PR_SEARCH_ATTACHMENTS_W PROP_TAG(PT_UNICODE, 0x0EA5)`
  
### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Задает свойства и операции для управления конфигурации список папок поиска.
    
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

