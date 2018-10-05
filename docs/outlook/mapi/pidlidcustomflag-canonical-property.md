---
title: Каноническое свойство PidLidCustomFlag
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidCustomFlag
api_type:
- COM
ms.assetid: bfb7fd1e-774f-9a2f-fbbe-ba7f68ed8663
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9a131c633b8dcf9b0e5070f01de8fcab90a18ade
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384201"
---
# <a name="pidlidcustomflag-canonical-property"></a>Каноническое свойство PidLidCustomFlag

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Битовая маска, которая указывает, как сообщение настроенную, например, сохраненных в настраиваемых свойств.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidCustomFlag  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x00008251  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Замечания

Чтобы получить значение этого свойства, сначала использовать **[IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md)** для получения тега свойства и укажите этот тег свойства в **[IMAPIProp::GetProps](imapiprop-getprops.md)** для получения значения. 
  
Флаги, как показано ниже:
  
****

|**Constant**|**Значение**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
При вызове **IMAPIProp::GetIDsFromNames**, укажите следующие значения для структуры **[MAPINAMEID](mapinameid.md)** , на который указывает входного параметра *lppPropNames* . 
  
****

|**Элемент**|**Значение**|
|:-----|:-----|
|lpGuid:  <br/> |PSETID_Common  <br/> |
|ulKind:  <br/> |MNID_ID  <br/> |
|Kind.lID:  <br/> |dispidCustomFlag  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств.
    
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

