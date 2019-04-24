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
  
Содержит значение разрешения конфликтов для папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РЕСОЛВЕ_МЕСОД  <br/> |
|Идентификатор:  <br/> |0x3FE7  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Состояние MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство папки, содержащей сообщение о разрешении конфликтов, указывает, как устранить конфликт. Это свойство не является обязательным. Тем не менее, если он задан, не должны присутствовать флаги, отличные от следующих:
  
|||
|:-----|:-----|
|РЕСОЛВЕ_МЕСОД_ДЕФАУЛТ (0x00000000)  <br/> |Необходимо создать сообщение о разрешении конфликтов.  <br/> |
|РЕСОЛВЕ_МЕСОД_ЛАСТ_ВРИТЕР_ВИНС (0x00000001)  <br/> |Перезаписать целевое сообщение с применением текущих изменений.  <br/> |
|РЕСОЛВЕ_НО_КОНФЛИКТ_НОТИФИКАТИОН (0x00000002)  <br/> |Не отправлять уведомление о конфликте при создании сообщения с разрешением конфликтов в общедоступной папке.  <br/> |
   
Клиент или сервер не должен создавать сообщение об ошибке разрешения конфликтов для связанных сообщений. Эти сообщения необходимо разрешить с помощью семантики **ресолве_месод_ласт_вритер_винс** . 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСКСИНК]](https://msdn.microsoft.com/library/fd3e23ef-341a-4a8c-a0e9-6afecbb11c40%28Office.15%29.aspx)
  
> Обрабатывает синхронизацию данных объекта обмена данными между сервером и клиентом.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Определяет основные структуры данных, используемые в удаленных операциях.
    
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

