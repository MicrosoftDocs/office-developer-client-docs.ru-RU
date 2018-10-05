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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25394904"
---
# <a name="pidtagresolvemethod-canonical-property"></a>Каноническое свойство PidTagResolveMethod

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит значение разрешения конфликтов папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RESOLVE_METHOD  <br/> |
|Идентификатор:  <br/> |0x3FE7  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Данное свойство для папки, содержащей сообщение разрешения конфликтов будет указано, как разрешить конфликт. Это свойство не требуется. Тем не менее если оно установлено, не должно присутствует флаги, кроме следующих:
  
|||
|:-----|:-----|
|RESOLVE_METHOD_DEFAULT (0X00000000)  <br/> |Устраните конфликт сообщение будет создан.  <br/> |
|RESOLVE_METHOD_LAST_WRITER_WINS (0X00000001)  <br/> |Перезаписать текущие изменения применяются конечного сообщения.  <br/> |
|RESOLVE_NO_CONFLICT_NOTIFICATION (0X00000002)  <br/> |Не отправлять сообщения с уведомлением о конфликте, когда формирование конфликта разрешить сообщение в общую папку.  <br/> |
   
Клиент или сервер должен создает сообщение устранением конфликтов для связанного сообщения. Эти сообщения должны быть разрешены с помощью семантики **RESOLVE_METHOD_LAST_WRITER_WINS** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXCSYNC]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Обрабатывает синхронизации обмена сообщениями объект данных между сервером и клиентом.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет структуры основных данных, которые используются для удаленных операций.
    
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

