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
ms.openlocfilehash: dfe3b57c246e247eda365bed46af2e0f35f0e54b
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32315388"
---
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Каноническое свойство PidLidValidFlagStringProof

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет, было ли значение свойства **диспидрекуест** ([PidLidFlagRequest](pidlidflagrequest-canonical-property.md)) задано агентом, который знал значение свойства **пр_мессаже_деливери_тиме** ([PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)).
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидвалидфлагстрингпруф  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x000085BF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Замечания

Для объектов, не относящихся к отправке (получены почтовые сообщения и объекты, не являющиеся сообщениями), при изменении **диспидрекуест**клиенты должны задать для этого параметра значение **пр_мессаже_деливери_тиме** .
  
Так как значение **пр_мессаже_деливери_тиме** не может быть предсказано отправителем, если значение этого свойства равно значению **пр_мессаже_деливери_тиме**, то разумно убедиться, что значение **диспидрекуест** не исходит от отправителя сообщения. Клиент может принять решение о том, как предоставить конечному пользователю значение **диспидрекуест** на основании результатов этого сравнения в соответствии с определенной политикой безопасности клиента. Если значение **диспидрекуест** игнорируется из-за наличия значения для **диспидфлагстринженум** ([PidLidFlagString](pidlidflagstring-canonical-property.md)), это свойство необходимо игнорировать.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.
    
[[MS — ОКСОФЛАГ]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Задает свойства и операции, связанные с пометкой.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

