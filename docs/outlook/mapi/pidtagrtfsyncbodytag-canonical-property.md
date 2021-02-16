---
title: Каноническое свойство PidTagRtfSyncBodyTag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRtfSyncBodyTag
api_type:
- COM
ms.assetid: 2dab5018-4214-4162-93bc-e5565f3ac24c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 24ef1d4e3e936426aea8216119e8ada9f6122e95
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331180"
---
# <a name="pidtagrtfsyncbodytag-canonical-property"></a>Каноническое свойство PidTagRtfSyncBodyTag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит важные символы, которые отображаются в начале текста сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RTF_SYNC_BODY_TAG, PR_RTF_SYNC_BODY_TAG_A, PR_RTF_SYNC_BODY_TAG_W  <br/> |
|Идентификатор:  <br/> |0x1008  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Сообщение MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Функция [RTFSync](rtfsync.md) использует текстовый тег, чтобы указать начало текста сообщения. При внесении изменений в текст тег используется для поиска начала предыдущего текста. 
  
Эти свойства являются вспомогательными свойствами формата RICH Text. Они используются функцией **RTFSync** и не предназначены для непосредственного использования клиентских приложений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXTNEF]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное представление потока.
    
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

