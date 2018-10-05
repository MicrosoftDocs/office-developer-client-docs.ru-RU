---
title: Каноническое свойство PidTagRuleSequence
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRuleSequence
api_type:
- COM
ms.assetid: c42f2539-f7d6-464a-a82c-f0ac51823168
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 70e7a20a69b7467c1d8c31469273dcc28ce219ae
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382633"
---
# <a name="pidtagrulesequence-canonical-property"></a>Каноническое свойство PidTagRuleSequence

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Значение, используемое для определения порядка, в котором правила проверяются и выполняются. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULE_SEQUENCE  <br/> |
|Идентификатор:  <br/> |0x6676  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Правила со стороны сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Правила оцениваются в последовательности в порядке возрастания это значение. Порядок вычисления для правил, которые имеют одинаковые значения в этом свойстве не определен.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXORULE]](https://msdn.microsoft.com/library/70ac9436-501e-43e2-9163-20d2b546b886%28Office.15%29.aspx)
  
> Управляет входящие сообщения электронной почты на сервере.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с элементами календаря и сообщения, когда они действовать от имени другого пользователя.
    
[[MS-OXCTABL]](https://msdn.microsoft.com/library/d33612dc-36a8-4623-8a26-c156cf8aae4b%28Office.15%29.aspx)
  
> Включает в себя разрешенных операций для базовых объектов в таблице.
    
[[MS-OXCSTOR]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для базовых объектов хранилища сообщений.
    
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

