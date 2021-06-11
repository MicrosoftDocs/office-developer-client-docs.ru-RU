---
title: Каноническое свойство PidLidValidFlagStringStringProof
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
# <a name="pidlidvalidflagstringproof-canonical-property"></a>Каноническое свойство PidLidValidFlagStringStringProof

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Проверяет, было ли значение свойства **dispidRequest** [(PidLidFlagRequest)](pidlidflagrequest-canonical-property.md)агентом, который знал значение свойства [PR_MESSAGE_DELIVERY_TIME (PidTagMessageDeliveryTime).](pidtagmessagedeliverytime-canonical-property.md) 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |dispidValidFlagStringProof  <br/> |
|Набор свойств:  <br/> |PSETID_Common  <br/> |
|Long ID (LID):  <br/> |0x000085BF  <br/> |
|Тип данных:  <br/> |PT_SYSTIME  <br/> |
|Область:  <br/> |Задача  <br/> |
   
## <a name="remarks"></a>Примечания

Для неоправляемых объектов (полученных объектов почты и не почты) клиенты должны задать это значение значению PR_MESSAGE_DELIVERY_TIME при изменении **dispidRequest**. 
  
Так как значение **PR_MESSAGE_DELIVERY_TIME** не может быть предсказано отправителю, если значение этого свойства равно значению **PR_MESSAGE_DELIVERY_TIME,** то вполне возможно, что значение **dispidRequest** не было исходят от отправитель сообщения. Клиент может решить, как представить значение **dispidRequest** конечному пользователю на основе результатов этого сравнения в соответствии с определенной политикой безопасности клиента. Если значение **dispidRequest** игнорируется из-за наличия значения **для dispidFlagStringEnum** [(PidLidFlagString),](pidlidflagstring-canonical-property.md)это свойство должно быть проигнорировано.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOFLAG]](https://msdn.microsoft.com/library/f1e50be4-ed30-4c2a-b5cb-8ff3aaaf9b91%28Office.15%29.aspx)
  
> Указывает свойства и операции, связанные с маркировкой.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagMessageDeliveryTime](pidtagmessagedeliverytime-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

