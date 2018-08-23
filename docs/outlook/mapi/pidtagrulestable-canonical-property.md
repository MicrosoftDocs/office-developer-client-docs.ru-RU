---
title: Каноническое свойство PidTagRulesTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fc520720-8190-4dff-8f6c-1bebf7080b57
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4b4b60084b8cb53a0a245b502b8fe70241fb4eb7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22591691"
---
# <a name="pidtagrulestable-canonical-property"></a>Каноническое свойство PidTagRulesTable

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу со всех правил, применяемых в папку.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULES_TABLE  <br/> |
|Идентификатор:  <br/> |0x3FE1  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Правила со стороны сервера  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство присутствует на всех объектов папок на сервере Exchange, которые имеют правила. Значения, включенные в этом свойстве используются для чтения и изменения правил. Можно использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** для получения [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейс к таблице правил для папки. Этот интерфейс можно использовать для чтения и изменения этих правил. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

