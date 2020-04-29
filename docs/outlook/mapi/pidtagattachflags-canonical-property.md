---
title: Каноническое свойство PidTagAttachFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAttachFlags
api_type:
- HeaderDef
ms.assetid: 47e01131-f399-43cb-9815-aba69638c3fb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: efccd75cce04e4e392a7fbd9feecc7c8b49ab57e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339335"
---
# <a name="pidtagattachflags-canonical-property"></a>Каноническое свойство PidTagAttachFlags

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3714  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство используется для поддержки MHTML. 
  
Для битовой маски **PR_ATTACH_FLAGS** можно задать один или несколько следующих флагов: 
  
ATT_INVISIBLE_IN_HTML 
  
> Указывает, что это вложение недоступно для HTML-приложений отображения и должно игнорироваться при обработке MIME. 
    
ATT_INVISIBLE_IN_RTF 
  
> Указывает, что это вложение недоступно для отображения приложений в формате RTF и должно игнорироваться MAPI.
    
Если свойство **PR_ATTACH_FLAGS** равно нулю или отсутствует, вложение обрабатывается всеми приложениями. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

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

