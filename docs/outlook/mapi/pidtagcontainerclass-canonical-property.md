---
title: Каноническое свойство PidTagContainerClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerClass
api_type:
- HeaderDef
ms.assetid: db249e9e-f1f0-4b95-8cd9-daa7c53ddb32
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c5b80831607f473208ce987a720c7e80e44b6d80
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32283151"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Каноническое свойство PidTagContainerClass

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, описывающую тип папки. Несмотря на то, что это свойство обычно игнорируется, версии Microsoft ® Exchange Server до Exchange Server 2003 поЧтовых ящиков ожидают, что это свойство присутствует.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНТАИНЕР_КЛАСС, ПР_КОНТАИНЕР_КЛАСС_А, ПР_КОНТАИНЕР_КЛАСС_В  <br/> |
|Идентификатор:  <br/> |0x3613  <br/> |
|Тип данных:  <br/> |PT_STRING8, ПТ_УНИКОДЕ  <br/> |
|Область:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства обычно не используются сервером Exchange Server. Однако Microsoft Office Outlook ® присоединяет их к папкам почтовых ящиков. Кроме того, версии сервера Exchange Server до Exchange Server 2003 поЧтовых ящиков могут неправильно обрабатывать папки, не имеющие этих свойств.
  
Этим свойствам можно присвоить строковые значения в приведенной ниже таблице.
  
|**Значение**|**Содержимое папки**|
|:-----|:-----|
|Кросс. События  <br/> |Встречи  <br/> |
|Кросс. Лицу  <br/> |Контакты  <br/> |
|Кросс. Фин  <br/> |Записи дневника Outlook  <br/> |
|Кросс. Ноте  <br/> |ПоЧтовые сообщения и заметки  <br/> |
|Кросс. Стиккиноте  <br/> |Outlook для клейких заМеток  <br/> |
|Кросс. Ее  <br/> |Задачи Outlook  <br/> |
   
Для папок, содержащих почтовые сообщения, эти свойства должны иметь значение IPF. Ноте.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.
    
[[MS — ОКСОКАЛ]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответных сообщений.
    
[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, которые являются допустимыми для объектов контакта и личного списка рассылки.
    
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

