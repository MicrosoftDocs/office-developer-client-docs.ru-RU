---
title: Каноническое свойство PidTagMessageClass
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageClass
api_type:
- HeaderDef
ms.assetid: 1e704023-1992-4b43-857e-0a7da7bc8e87
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7912a3831333ff8a464a12e567430eb5a3272172
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359266"
---
# <a name="pidtagmessageclass-canonical-property"></a>Каноническое свойство PidTagMessageClass

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит текстовую строку, определяющую класс сообщений, определенный отправителем, например IPM. Ноте. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МЕССАЖЕ_КЛАСС, ПР_МЕССАЖЕ_КЛАСС_А, ПР_МЕССАЖЕ_КЛАСС_В  <br/> |
|Идентификатор:  <br/> |0x001A  <br/> |
|Тип данных:  <br/> |ПТ_УНИКОДЕ, PT_STRING8  <br/> |
|Область:  <br/> |Распространенная  <br/> |
   
## <a name="remarks"></a>Примечания

Класс Message указывает тип сообщения. Он определяет набор свойств, определенных для сообщения, тип данных, которые передает сообщение, и способ обработки сообщения. 
  
Эти свойства содержат строки, Объединенные с точками. Каждая строка представляет уровень подклассов. Например, IPM. Note является подклассом IPM и суперклассом IPM. Note. Private. 
  
Эти свойства должны состоять из символов ASCII от 32 до 127 и не должны заканчиваться точкой (ASCII 46). Операции сортировки и сравнения должны рассматривать его как строку без учета регистра. Максимально допустимая длина составляет 255 символов, но чтобы разрешить комнате MAPI добавлять квалификаторы, рекомендуется хранить исходную длину в 128 символов. 
  
Для этих свойств требуется каждое сообщение. Как правило, клиентское приложение, создающее новое сообщение, задает его как можно быстрее, чем [IMAPIFolder:: CreateMessage](imapifolder-createmessage.md) возвращает успешно. Но если свойство не было задано, когда клиент вызывает [IMAPIProp:: SaveChanges](imapiprop-savechanges.md), в хранилище сообщений должно быть задано значение IPM. 
  
Для MAPI определены следующие значения: 
  
```cpp
IPM.Note for a standard interpersonal message 
REPORT.<subject message class>.DR for a delivery report 
REPORT.<subject message class>.NDR for a nondelivery report 
REPORT.<subject message class>.IPNRN for a read report 
REPORT.<subject message class>.IPNNRN for a nonread report 
 
```

IPM и IPC предназначены только для подклассов, а в сообщении должен быть по крайней мере один квалификатор подкласса, добавленный перед сохранением или отправкой. Более подробную информацию об использовании класса сообщений можно узнать в статье [классы сообщений](mapi-message-classes.md). Список обязательных и необязательных свойств для классов сообщений приведен в подразделах [о свойствах сообщений](message-properties-overview.md).
  
Настраиваемый класс сообщения может определять свойства в зарезервированном диапазоне для использования только с этим классом сообщения. Более подробную информацию можно узнать в статье [об идентификаторАх свойств](mapi-property-identifier-overview.md). 
  
Классы сообщений — это контроль над папкой, в которой хранится входящее сообщение. Дополнительные сведения см. в методе [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) . 
  
Для получения дополнительных сведений об использовании классов сообщений с формами и серверами форм, ознакомьтесь со статьей [Выбор класса сообщений](choosing-a-message-class.md). 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОМСГ]](https://msdn.microsoft.com/library/daa9120f-f325-4afb-a738-28f91049ab3c%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для объектов сообщений электронной почты.
    
[[MS — ОКСАУМ]](https://msdn.microsoft.com/library/2a0696c5-2caf-4f20-87fb-085db430afec%28Office.15%29.aspx)
  
> Задает свойства и операции, допустимые для представления голосовой почты и факсимильных сообщений.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

