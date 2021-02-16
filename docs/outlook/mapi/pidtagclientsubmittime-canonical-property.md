---
title: Каноническое свойство PidTagClientSubmitTime
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagClientSubmitTime
api_type:
- HeaderDef
ms.assetid: d46e1063-6421-410d-a445-7477fea42089
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 851441e419c17d8f5fef27c785ea4b829a4ae443
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345719"
---
# <a name="pidtagclientsubmittime-canonical-property"></a>Каноническое свойство PidTagClientSubmitTime

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит дату и время отправки сообщения отправив сообщение. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CLIENT_SUBMIT_TIME  <br/> |
|Идентификатор:  <br/> |0x0039  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Время сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Поставщик магазина задает **PR_CLIENT_SUBMIT_TIME** время, в которое клиентский приложение называло [IMessage::SubmitMessage.](imessage-submitmessage.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
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

