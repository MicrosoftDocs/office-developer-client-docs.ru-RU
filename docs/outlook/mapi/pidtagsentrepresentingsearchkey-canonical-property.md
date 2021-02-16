---
title: Каноническое свойство PidTagSentRepresentingSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagSentRepresentingSearchKey
api_type:
- COM
ms.assetid: 7a49b944-cef1-4642-9208-b137fd61171a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: a9361f3027453742acbe50c3de01d860289cd0ed
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356688"
---
# <a name="pidtagsentrepresentingsearchkey-canonical-property"></a>Каноническое свойство PidTagSentRepresentingSearchKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ поиска для пользователя обмена сообщениями, представленного отправищиком.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SENT_REPRESENTING_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x003B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Address  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является одним из свойств адреса для пользователя обмена сообщениями, представленного отправищиком. Когда клиентская приложение отправляет сообщение от имени другого клиента, оно должно установить для всех представленных свойств отправитель значения для этого клиента. Пользователь обмена сообщениями, отправляющий сообщения от своего имени, обычно оставляет представленные свойства отправитель ненамеренными.
  
Отправляющий клиент всегда должен оставить это свойство без изменений. Если он не затенен, поставщик транспорта должен установить для него PR_SENDER_SEARCH_KEY **(** [PidTagSenderSearchKey)](pidtagsendersearchkey-canonical-property.md)в исходящие копии сообщения и оставить его ненастроенным в локальной копии.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOMSG]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Указывает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразуется между IETF RFC2445, RFC2446 и RFC2447, а также объектами встреч и собраний.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
[[MS-OXOPOST]](https://msdn.microsoft.com/library/9b18fdab-aacd-4d73-9534-be9b6ba2f115%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов post.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для списков контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

