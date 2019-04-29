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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу со всеми правилами, примененными к папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_РУЛЕС_ТАБЛЕ  <br/> |
|Идентификатор:  <br/> |0x3FE1  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Правила на стороне сервера  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство присутствует во всех объектах папки на сервере Exchange с правилами. Значения, включенные в это свойство, используются для чтения и изменения правил. Вы можете использовать метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с идентификатором интерфейса **иид_иексчанжемодифитабле** , чтобы получить интерфейс [IUnknown иексчанжемодифитабле:](iexchangemodifytableiunknown.md) для таблицы Rules в папке. Вы можете использовать этот интерфейс для чтения и изменения этих правил. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства. 
    
## <a name="see-also"></a>См. также



[IExchangeModifyTable : IUnknown](iexchangemodifytableiunknown.md)
  
[IMAPIProp::OpenProperty](imapiprop-openproperty.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

