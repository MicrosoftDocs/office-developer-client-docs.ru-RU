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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, описываемую тип папки. Хотя это свойство обычно игнорируется, версии Microsoft® Exchange Server предшествующие Exchange Server Mailbox Manager 2003, ожидают, что это свойство будет присутствовать.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_CLASS, PR_CONTAINER_CLASS_A, PR_CONTAINER_CLASS_W  <br/> |
|Идентификатор:  <br/> |0x3613  <br/> |
|Тип данных:  <br/> |PT_STRING8, PT_UNICODE  <br/> |
|Область:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Примечания

Эти свойства обычно не используются Exchange Server. Однако Microsoft Office Outlook® вложенные в папки почтовых ящиков. Кроме того, версии Exchange Server, предшествующие Exchange Server 2003 Mailbox Manager, могут неправильно обрабатывать папки, которые не имеют этих свойств.
  
Этим свойствам могут быть назначены строки, указанные в следующей таблице.
  
|**Значение**|**Содержимое папки**|
|:-----|:-----|
|IPF. Встреча  <br/> |Встречи  <br/> |
|IPF. Контакт  <br/> |Контакты  <br/> |
|IPF. Журнал  <br/> |Записи журнала Outlook  <br/> |
|IPF. Примечание  <br/> |Почтовые сообщения и заметки  <br/> |
|IPF. StickyNote  <br/> |Заметки о тиках Outlook  <br/> |
|IPF. Задача  <br/> |Задачи Outlook  <br/> |
   
Для папок, содержащих сообщения электронной почты, эти свойства должны иметь iPF. Примечание.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.
    
[[MS-OXOCAL]](https://msdn.microsoft.com/library/09861fde-c8e4-4028-9346-e7c214cfdba1%28Office.15%29.aspx)
  
> Указывает свойства и операции для встреч, запросов на собрание и ответных сообщений.
    
[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)
  
> Указывает свойства и операции, которые разрешены для объектов контактов и личных списков рассылки.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

