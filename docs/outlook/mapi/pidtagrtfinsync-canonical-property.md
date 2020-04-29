---
title: Каноническое свойство PidTagRtfInSync
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfInSync
api_type:
- COM
ms.assetid: 443cc68e-7898-4285-a606-f916fcd18554
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ed038faf44f350b041191373cf573e7e185337c7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357878"
---
# <a name="pidtagrtfinsync-canonical-property"></a>Каноническое свойство PidTagRtfInSync

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение TRUE, если свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)) имеет то же текстовое содержимое, что и свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)) для этого сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Идентификатор:  <br/> |0x0E1F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Значение TRUE означает, что свойство **PR_BODY** ([PidTagBody](pidtagbody-canonical-property.md)), версия обычного текста этого сообщения и свойство **PR_RTF_COMPRESSED** ([PidTagRtfCompressed](pidtagrtfcompressed-canonical-property.md)), версия RTF, идентичны за исключением пробелов в **PR_BODY** и форматирования в **PR_RTF_COMPRESSED**. Текст в двух версиях состоит из одних и тех же символов в одной и той же последовательности.
  
Значение FALSE означает, что две версии не синхронизируются для текстового содержимого, но могут быть синхронизированы с помощью функции [ртфсинк](rtfsync.md) . Одна и та же версия была изменена, а другая нет. 
  
Значение не означает, что две версии (если они существуют или когда-либо существовали) не могут быть синхронизированы. Одна версия была удалена или изменена таким образом, что синхронизация более невозможна.
  
В клиентском приложении с измененными **PR_RTF_COMPRESSED** для принудительной синхронизации в этом свойстве должно быть задано значение false. Хранилища сообщений с поддержкой RTF должны выполнять синхронизацию с помощью **ртфсинк** во время вызова [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Клиенты, поддерживающие RTF, должны проверять параметры **PR_RTF_IN_SYNC** перед чтением **PR_RTF_COMPRESSED**, и при необходимости вызывать **ртфсинк** в первую очередь. 
  
Если **PR_BODY** имеет изменения, которые отличаются от пробелов, то хранилище сообщений должно удалить **PR_RTF_IN_SYNC** для завершения синхронизации. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

