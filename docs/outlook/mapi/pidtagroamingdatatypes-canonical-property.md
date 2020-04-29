---
title: Каноническое свойство PidTagRoamingDatatypes
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRoamingDatatypes
api_type:
- COM
ms.assetid: a3336b61-01b6-47a7-9498-0a03878e91cb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fe5528f7605412d0cfd4b4b914e9b221c715e1b1
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359558"
---
# <a name="pidtagroamingdatatypes-canonical-property"></a>Каноническое свойство PidTagRoamingDatatypes

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовую маску, указывающую, какие свойства потока существуют для сообщения.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Идентификатор:  <br/> |0x7C06  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Настройка  <br/> |
   
## <a name="remarks"></a>Примечания

Для этого свойства необходимо задать одно или несколько из следующих значений:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000002  <br/> |Указывает, что сообщение связанной информации о папке (ФАИ) должно содержать поток словаря, сериализованный в фиксированную схему XML и хранящийся в свойстве **PR_ROAMING_DICTIONARY** ([PidTagRoamingDictionary](pidtagroamingdictionary-canonical-property.md)). Если сообщение ФАИ не содержит поток словаря, приложение должно считать словарь без записей.  <br/> |
|0x00000004  <br/> |Указывает, что сообщение ФАИ должно содержать XML-поток, хранящийся в свойстве **PR_ROAMING_XMLSTREAM** ([PidTagRoamingXmlStream](pidtagroamingxmlstream-canonical-property.md)), использующей произвольную XML-схему.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОКФГ]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Задает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

