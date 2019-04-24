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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357619"
---
# <a name="pidlidcustomflag-canonical-property"></a>Каноническое свойство PidLidCustomFlag

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Битовая маска, указывающая способ настройки сообщения, например, сохраненный с настраиваемыми свойствами.
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидкустомфлаг  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008251  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
   
## <a name="remarks"></a>Примечания

Чтобы получить значение этого свойства, сначала используйте **[IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md)** , чтобы получить тег свойства, а затем укажите этот тег свойства в **[IMAPIProp:: Prop](imapiprop-getprops.md)** , чтобы получить значение. 
  
Возможны следующие флаги:
  
****

|**Константа**|**Значение**|
|:-----|:-----|
|INSP_ONEOFFFLAGS  <br/> |0x0D000000  <br/> |
|INSP_PROPDEFINITION  <br/> |0x02000000  <br/> |
   
При вызове **IMAPIProp:: жетидсфромнамес**укажите следующие значения для структуры **[мапинамеид](mapinameid.md)** , на которую указывает входной параметр *лпппропнамес* . 
  
****

|**Member**|**Значение**|
|:-----|:-----|
|Лпгуид:  <br/> |Псетид_коммон  <br/> |
|Улкинд:  <br/> |MNID_ID  <br/> |
|Вид: крышка:  <br/> |Диспидкустомфлаг  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Задает определения свойств.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

