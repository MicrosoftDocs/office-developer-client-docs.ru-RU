---
title: Каноническое свойство PidLidTaskStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidTaskStatus
api_type:
- COM
ms.assetid: 809776b7-ff00-4a52-84b9-8b5fb5f5c3e3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d058b42ad7d1a1b8387aa5b9a1a65ea160d90b02
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316669"
---
# <a name="pidlidtaskstatus-canonical-property"></a>Каноническое свойство PidLidTaskStatus

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Указывает состояние выполнения пользователем задачи.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidTaskStatus  <br/> |
|Набор свойств:  <br/> |PSETID_Task  <br/> |
|Long ID (LID):  <br/> |0x00008101  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Значение этого свойства должно быть установлено в одном из следующих значений.
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000000  <br/> |Пользователь еще не приступил к работе над задачей. Если это значение установлено, **значение dispidPercentComplete** [(PidLidPercentComplete)](pidlidpercentcomplete-canonical-property.md)должно быть 0,0.  <br/> |
|0x00000001  <br/> |Работа пользователя над этой задачей продолжается. Если это значение установлено, **значение dispidPercentComplete** должно быть больше 0,0 и менее 1,0.  <br/> |
|0x00000002  <br/> |Работа пользователя над этой задачей завершена. Если это значение заданной, **dispidPercentComplete** должно быть 1.0, **dispidTaskDateCompleted** [(PidLidTaskDateCompleted)](pidlidtaskdatecompleted-canonical-property.md)должно быть актуальной датой, а **dispidTaskComplete** [(PidLidTaskComplete)](pidlidtaskcomplete-canonical-property.md)должно быть TRUE.  <br/> |
|0x00000003  <br/> |Пользователь ждет другого пользователя.  <br/> |
|0x00000004  <br/> |Пользователь отложил работу над задачей.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOTASK]](https://msdn.microsoft.com/library/55600ec0-6195-4730-8436-59c7931ef27e%28Office.15%29.aspx)
  
> Определяет несколько объектов, которые моделируют электронный эквивалент задач, назначений задач и обновлений задач.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных конвенций электронной почты в объекты сообщений.
    
[[MS-OXCICAL]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразования между объектами IETF RFC2445, RFC2446 и RFC2447, а также объектами назначения и собраний.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidLidPercentComplete](pidlidpercentcomplete-canonical-property.md)
  
[Каноническое свойство PidLidTaskDateCompleted](pidlidtaskdatecompleted-canonical-property.md)
  
[Каноническое свойство PidLidTaskComplete](pidlidtaskcomplete-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

