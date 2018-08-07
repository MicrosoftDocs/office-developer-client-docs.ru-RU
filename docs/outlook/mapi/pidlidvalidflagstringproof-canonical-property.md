---
title: Каноническое свойство PidLidValidFlagStringProof
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidValidFlagStringProof
api_type:
- COM
ms.assetid: e5a94968-7e84-4faf-8104-9ea36d35fa1a
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 90f16f33e7e116e124384f9988c0c7dddaad2da5
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810667"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Каноническое свойство PidLidValidFlagStringProof

  
  
**Относится к**: Outlook 
  
Проверяет, является ли было задано значение свойства **dispidRequest** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) по агенту, который знала, значение свойства **PR_MESSAGE_DELIVERY_TIME** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidValidFlagStringProof  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x000085BF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Task  <br/> |
   
## <a name="remarks"></a>Замечания

Не отправляемого объектов (полученной почты и не содержащие почту объекты) клиенты должны присвойте этому параметру значение значение **PR_MESSAGE_DELIVERY_TIME** при изменении **dispidRequest**.
  
Так как значение **PR_MESSAGE_DELIVERY_TIME** непредсказуемым образом отправителем, если значение этого свойства равно значению **PR_MESSAGE_DELIVERY_TIME**, это уверенность, что значение **dispidRequest** не поступают от отправителя сообщения. Клиент может решить, как бы представить значение **dispidRequest** конечного пользователя, на основе результатов этого сравнения в соответствии с политикой безопасности клиента. Если значение **dispidRequest** игнорируется из-за наличия значение для **dispidFlagStringEnum** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), это свойство должны игнорироваться.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOFLAG]](http://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с флагов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

