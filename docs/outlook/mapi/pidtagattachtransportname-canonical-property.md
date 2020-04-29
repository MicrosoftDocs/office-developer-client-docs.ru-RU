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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32361070"
---
# <a name="pidtagattachtransportname-canonical-property"></a>Каноническое свойство PidTagAttachTransportName

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя файла вложения, измененного таким образом, что его можно связать с сообщениями в формате TNEF. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_TRANSPORT_NAME, PR_ATTACH_TRANSPORT_NAME_A PR_ATTACH_TRANSPORT_NAME_W  <br/> |
|Идентификатор:  <br/> |0x370C  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

В формате TNEF и транспортном поставщике используются эти свойства. Они обычно недоступны для клиентских приложений. 
  
Эти свойства обычно используются в формате TNEF, когда базовая система обмена сообщениями не поддерживает указанные имена файлов. Например, они используются, когда пользователь присоединяет несколько файлов с одинаковыми именами, например, пять файлов с именем CONFIG. SYS. Поставщик транспорта должен изменить имена, чтобы убедиться, что они уникальны. Каждое измененное имя отображается в **PR_ATTACH_TRANSPORT_NAME** вложения и связанных с ним свойствах. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

