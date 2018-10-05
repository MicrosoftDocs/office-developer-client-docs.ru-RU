---
title: Каноническое свойство PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387750"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Каноническое свойство PidTagSearchRecipientEmailBcc

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит строку Юникод, запрашиваемый в список адресов электронной почты или отображаемые имена получателей, которые рассматриваются в строки **Скрытая копия** неотправленные сообщения в хранилище. 
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_RECIP_EMAIL_BCC_W  <br/> |
|Идентификатор:  <br/> |0x0EA8  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Access:  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство применяется только в том к сообщениям в хранилище, которые не были отправлены, поскольку сообщений, отправленных или полученных не содержат сведения о скрытой копии.
  
> [!NOTE]
> Этот тег ограничений MAPI, используется при поиске адресов электронной почты или отображаемые имена, в которых будет отправлено сообщение как скрытую копию, не могут быть определены в файле загружаемых заголовка, который в настоящий момент. Добавьте в код с помощью следующее значение: >`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
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

