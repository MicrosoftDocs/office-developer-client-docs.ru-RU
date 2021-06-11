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
ms.openlocfilehash: e1c670cd566e838104ae3d5480c2297f8632d899
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428503"
---
# <a name="pidtagrulestable-canonical-property"></a>Каноническое свойство PidTagRulesTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу со всеми правилами, применяемыми к папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RULES_TABLE  <br/> |
|Идентификатор:  <br/> |0x3FE1  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Правила стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство присутствует во всех объектах папок на Exchange Server с правилами. Значения, включенные в это свойство, используются для чтения и изменения правил. Вы можете использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором **IID_IExchangeModifyTable** интерфейса для получения [интерфейса IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) к таблице правил в папке. Этот интерфейс можно использовать для чтения и изменения этих правил. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

