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
ms.openlocfilehash: d12e8510686f51698981c47327f79ef40d3ec342
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32342550"
---
# <a name="pidtagmappingsignature-canonical-property"></a>Каноническое свойство PidTagMappingSignature

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит подпись сопоставления для именных свойств определенного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_MAPPING_SIGNATURE  <br/> |
|Идентификатор:  <br/> |0x0FF8  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Разное  <br/> |
   
## <a name="remarks"></a>Примечания

Рекомендуется, чтобы объекты с именем свойства подвергали этому свойству. Клиентская заявка должна проверять **PR_MAPPING_SIGNATURE** обоих объектов при копировании именных свойств с одного объекта на другой. Использование этого свойства может свести к минимуму перевод между именами и идентификаторами скопированные свойства. 
  
Если этого свойства не существует для данного объекта MAPI, то у объекта есть свое уникальное сопоставление имен и идентификаторов. В этом случае клиент должен вызвать метод [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) на исходный объект, а затем метод [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) на объекте назначения. 
  
Если два объекта имеют **одинаковое PR_MAPPING_SIGNATURE,** клиенту не нужно переводить имя в идентификатор и идентификатор на имя. Клиент может просто вызвать метод [IMAPIProp::GetProps](imapiprop-getprops.md) в источнике, а затем метод [IMAPIProp::SetProps](imapiprop-setprops.md) в пункте назначения. Это удобно для клиентов, которые выполняют настраиваемую копирование именных свойств, а также для поставщиков, реализующих методы [IMAPIProp::CopyTo](imapiprop-copyto.md) и [IMAPIProp::CopyProps.](imapiprop-copyprops.md) 
  
Дополнительные сведения о свойствах имен и сопоставлении имен и идентификаторов см. в документе [MAPI Named Properties.](mapi-named-properties.md) 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[MAPINAMEID](mapinameid.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

