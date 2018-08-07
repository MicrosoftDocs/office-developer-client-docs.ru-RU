---
title: Каноническое свойство PidTagMappingSignature
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMappingSignature
api_type:
- HeaderDef
ms.assetid: a5e9f807-12a9-4bc9-a6a5-17579e747ffa
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0a83e0aa8f7ab1eb1f30e3ba97d3ea36f16fd873
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811335"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Каноническое свойство PidTagMappingSignature

  
  
**Относится к**: Outlook 
  
Содержит сопоставления подпись для именованных свойств конкретного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Идентификатор:  <br/> |0x0FF8  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Замечания

Рекомендуется, что объекты, с именем свойства предоставляют это свойство. Клиентское приложение должно проверять свойство **PR_MAPPING_SIGNATURE** обоих объектов при копировании с именем свойства из одного объекта в другой. Использование этого свойства можно свести к минимуму преобразование между имена и идентификаторы скопированные свойства. 
  
Если это свойство не существует для того или иного объекта MAPI, объект имеет свой собственный уникальное сопоставление имен и идентификаторов. В этом случае клиента необходимо вызвать метод [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) на объекте источника и затем [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) на целевой объект. 
  
Если два объекта имеют такое же значение **PR_MAPPING_SIGNATURE** , клиент переводить имя, идентификатор и идентификатор имени не требуется. Клиент может просто вызовите метод [IMAPIProp::GetProps](imapiprop-getprops.md) для источника, и затем метод [IMAPIProp::SetProps](imapiprop-setprops.md) в месте назначения. Это удобно для клиентов, выполняющие настраиваемые копирование именованных свойств, а также для реализации методов [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMAPIProp::CopyProps](imapiprop-copyprops.md) поставщиков. 
  
Дополнительные сведения об именованных свойств и сопоставлений имен и идентификаторов в разделе [Свойства с именем MAPI](mapi-named-properties.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

