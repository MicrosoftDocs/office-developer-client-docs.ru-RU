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
  
Содержит **true, если свойство PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)содержит то же текстовое **содержимое, что** и свойство PR_BODY ([PidTagBody)](pidtagbody-canonical-property.md)для этого сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_IN_SYNC  <br/> |
|Идентификатор:  <br/> |0x0E1F  <br/> |
|Тип данных:  <br/> |PT_BOOLEAN  <br/> |
|Область:  <br/> |Электронная почта  <br/> |
   
## <a name="remarks"></a>Примечания

Значение TRUE означает, что свойство **PR_BODY** ([PidTagBody),](pidtagbody-canonical-property.md)текстовая версия этого сообщения и **свойство PR_RTF_COMPRESSED** ([PidTagRtfCompressed)](pidtagrtfcompressed-canonical-property.md)версии RTF идентичны, за исключением пробела в **PR_BODY** и форматирования **в PR_RTF_COMPRESSED**. Текст в двух версиях состоит из одинаковых символов в одной последовательности.
  
Значение FALSE означает, что две версии не синхронизируются для текстового содержимого, но могут быть синхронизированы функцией [RTFSync.](rtfsync.md) Одна версия была изменена, а другая нет. 
  
Отсутствие значения означает, что две версии, если обе версии существуют или когда-либо существовали, не могут быть синхронизированы. Одна версия была удалена или изменена настолько быстро, что синхронизация больше невозмольна.
  
Клиентские приложения, которые **PR_RTF_COMPRESSED** должны установить значение FALSE в этом свойстве для принудительной синхронизации. Хранилища сообщений с RTF должны выполнять синхронизацию с помощью **RTFSync** во время вызова [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Клиенты с RTF должны  проверять параметры PR_RTF_IN_SYNC перед чтением PR_RTF_COMPRESSED и при необходимости вызывать **RTFSync.** 
  
Если **PR_BODY** были внесены изменения, кроме пробела, хранилище сообщений  должно удалить PR_RTF_IN_SYNC, чтобы завершить синхронизацию. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

