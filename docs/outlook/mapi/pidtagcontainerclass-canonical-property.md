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
ms.openlocfilehash: 9d40c21cde6bf3a6e8e37dda80dd6f900f233a0e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810967"
---
# <a name="pidtagcontainerclass-canonical-property"></a>Каноническое свойство PidTagContainerClass

  
  
**Относится к**: Outlook 
  
Содержит текстовая строка, описывающая тип папки. Несмотря на то, что это свойство игнорируется, как правило, версий Microsoft® Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 ожидается, что это свойство должен быть установлен.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x3613  <br/> |
|Тип данных:  <br/> |PT_STRING8 PT_UNICODE  <br/> |
|Область:  <br/> |Контейнер  <br/> |
   
## <a name="remarks"></a>Замечания

Эти свойства обычно не используется в Exchange Server. Тем не менее Microsoft Office Outlook® подключает их папки почтовых ящиков. Кроме того версии Exchange Server до диспетчера почтовых ящиков Exchange Server 2003 могут неправильно обрабатывать папок, которые не имеют следующие свойства.
  
Эти свойства может быть назначен строковых значений в следующей таблице.
  
|**Значение**|**Содержимое папки**|
|:-----|:-----|
|IPF. Встречи  <br/> |Встречи  <br/> |
|IPF. Контакт  <br/> |Контакты  <br/> |
|IPF. Журнал  <br/> |Записи журнала в Outlook  <br/> |
|IPF. Примечание  <br/> |Сообщения почты и заметки  <br/> |
|IPF. Заметки  <br/> |Записки Outlook  <br/> |
|IPF. Задача  <br/> |Задачи Outlook  <br/> |
   
Для папок, содержащих почтовых сообщений эти свойства должны быть установлены для IPF. Примечание.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXOCAL]](http://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Задает свойства и операции для встречи, приглашения на собрание и ответы.
    
[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов списка рассылки и контактов.
    
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

