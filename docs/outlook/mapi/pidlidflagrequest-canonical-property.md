---
title: Каноническое свойство PidLidFlagRequest
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidFlagRequest
api_type:
- COM
ms.assetid: 38981f07-14b8-47c2-93df-e6aed91896e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ddcf32df716fe2b0a02655278ff0cd8d821de1f4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357808"
---
# <a name="pidlidflagrequest-canonical-property"></a>Каноническое свойство PidLidFlagRequest

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Представляет состояние приглашения на собрание.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |Диспидрекуест  <br/> |
|Набор свойств:  <br/> |Псетид_коммон  <br/> |
|Длинный идентификатор (крышка):  <br/> |0x00008530  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Пометка  <br/> |
   
## <a name="remarks"></a>Примечания

В Microsoft Office Outlook приглашение на собрание является элементом встречи.
  
Это свойство содержит определяемый пользователем текст, который необходимо связать с флагом и должен быть задан, если объект сообщения помечен или завершен, но не должен существовать для объекта, связанного с собранием. Клиенты могут отказаться от поддержки этого свойства и всегда записывать "к исполнению" (при необходимости он преобразуется на язык пользователя) в качестве значения строки, когда это свойство должно быть задано. Это свойство должно игнорироваться условно в зависимости от значений свойств **диспидфлагстринженум** ([PidLidFlagString](pidlidflagstring-canonical-property.md)) и **диспидвалидфлагстрингпруф** ([PidLidValidFlagStringProof](pidlidvalidflagstringproof-canonical-property.md)).
  
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



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

