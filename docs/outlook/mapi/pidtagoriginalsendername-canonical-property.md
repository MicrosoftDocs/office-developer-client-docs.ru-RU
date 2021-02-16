---
title: Каноническое свойство PidTagOriginalSenderName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagOriginalSenderName
api_type:
- COM
ms.assetid: 5e3b7764-b122-4405-be4f-7fec571c7dfc
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 521fb544152dcb903450ff7dbd05ecbac808afe0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342611"
---
# <a name="pidtagoriginalsendername-canonical-property"></a>Каноническое свойство PidTagOriginalSenderName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит отображаемую имя отправитель первой версии сообщения, то есть сообщение перед переадащением или ответом.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ORIGINAL_SENDER_NAME, PR_ORIGINAL_SENDER_NAME_A, PR_ORIGINAL_SENDER_NAME_W  <br/> |
|Идентификатор:  <br/> |0x005A  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Общие сообщения  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства являются примерами свойств адреса исходного отправитель сообщения. При первой отправке сообщения клиентские приложения должны установить для этих свойств значение **свойства PR_SENDER_NAME** ([PidTagSenderName).](pidtagsendername-canonical-property.md) Оно никогда не меняется, когда сообщение переадовыно или отвечает на него.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
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

