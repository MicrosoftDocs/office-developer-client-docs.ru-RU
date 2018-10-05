---
title: Каноническое свойство PidTagAttachTransportName
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachTransportName
api_type:
- HeaderDef
ms.assetid: 701fca52-0f96-4019-80cd-c0ccd059ff9b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bd3a22bf55d03f3a9f06bf5c19650407bcc5627d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400518"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Каноническое свойство PidTagAttachTransportName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя файла вложения, изменена, поэтому его можно связать с сообщениями TNEF. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A, PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Идентификатор:  <br/> |0x370C  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Поставщик транспорта и TNEF использовать эти свойства. Обычно не отображаются на клиентские приложения. 
  
Эти свойства часто используемые TNEF при системы обмена сообщениями не поддерживает заданный имена файлов. Например они используются при присоединении пользователя несколько файлов с тем же именем, например пять файлы с именем конфигурации. SYS. Поставщика транспорта необходимо изменить имена, чтобы убедиться в том, что они являются уникальными. Имя каждого изменения отображается в **PR_ATTACH_TRANSPORT_NAME** его вложение и связанными свойствами. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

