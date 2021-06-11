---
title: Каноническое свойство PidTagResolveMethod
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagResolveMethod
api_type:
- COM
ms.assetid: 30d23c19-e0da-4511-9361-761153259216
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 14bb31ae9aebbb6441948b5756b426508107c9f0
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32331404"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Каноническое свойство PidTagResolveMethod

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит значение разрешения конфликтов в папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Идентификатор:  <br/> |0x3FE7  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство в папке, содержащей сообщение о разрешении конфликтов, указывает, как разрешить конфликт. Это свойство не требуется. Однако, если она установлена, флаги, кроме следующих, не должны присутствовать:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0x00000000)  <br/> |Сообщение о разрешении конфликтов должно быть сгенерировано.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0x00000001)  <br/> |Переописывание целевого сообщения с текущими изменениями.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0x00000002)  <br/> |Не отправлять сообщение уведомления о конфликте при создании сообщения о разрешении конфликтов в общедоступных папках.  <br/> |
   
Клиент или сервер не должны создавать сообщение о разрешении конфликтов для связанных сообщений. Эти сообщения должны быть разрешены с помощью **RESOLVE_METHOD_LAST_WRITER_WINS** семантики. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объектов обмена сообщениями между сервером и клиентом.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

