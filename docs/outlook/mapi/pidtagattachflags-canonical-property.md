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
ms.openlocfilehash: b934f9694061e17118be35e3fabeeff3bbc61a37
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810844"
---
# <a name="pidtagattachflags-canonical-property"></a>Каноническое свойство PidTagAttachFlags

  
  
**Относится к**: Outlook 
  
Содержит битовую маску флагов для вложения. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ATTACH_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3714  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Вложение в сообщение  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство используется для поддержки MHTML. 
  
Один или несколько из следующих флагов можно задать для битовой маски **PR_ATTACH_FLAGS** : 
  
ATT_INVISIBLE_IN_HTML 
  
> Указывает, что это вложение не доступен для приложений отображения HTML и должны учитываться в многоцелевые расширения почтового стандарта Интернета (MIME) обработки. 
    
ATT_INVISIBLE_IN_RTF 
  
> Указывает, что это вложение не доступен для приложений, визуализации в форматированный текст (RTF) и должны учитываться MAPI.
    
Если свойство **PR_ATTACH_FLAGS** равно нулю или отсутствует вложения — для обработки всех приложений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

