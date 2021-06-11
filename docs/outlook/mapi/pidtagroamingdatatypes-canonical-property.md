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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битмаску, которая указывает, какие свойства потока существуют в сообщении.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ROAMING_DATATYPES  <br/> |
|Идентификатор:  <br/> |0x7C06  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Конфигурация  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство должно быть заданной для одного или более из следующих значений:
  
|**Значение**|**Описание**|
|:-----|:-----|
|0x00000002  <br/> |Указывает на то, что сообщение о связанной с папкой информации (FAI) должно содержать поток  словарей, сериализованный в фиксированную схему XML и хранимый в свойстве[PR_ROAMING_DICTIONARY (PidTagRoamingDictionary).](pidtagroamingdictionary-canonical-property.md) Если сообщение FAI не содержит потока Словарь, приложение должно рассматривать словарь как не имеющий записей.  <br/> |
|0x00000004  <br/> |Указывает, что сообщение FAI должно содержать поток **XML,** хранимый в свойстве [PR_ROAMING_XMLSTREAM (PidTagRoamingXmlStream),](pidtagroamingxmlstream-canonical-property.md)который использует произвольную схему XML.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

