---
title: Каноническое свойство PidTagAccessControlListTable
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAccess
api_type:
- HeaderDef
ms.assetid: 48667fda-ddc4-42ac-9231-761db0a4c1a9
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9c71a2b806b810906c13ea4750e5491b1544f640
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424506"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Каноническое свойство PidTagAccessControlListTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу, состоящую из всех списков управления доступом к системе (SACL), применяемых к папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACL_TABLE  <br/> |
|Идентификатор:  <br/> |0x3FE0  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство присутствует во всех объектах папки на Exchange Server. Значения, включенные в это свойство, используются для чтения и изменения списков управления доступом (ACLs) в папках. Вы можете использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором **IID_IExchangeModifyTable** интерфейса для получения [интерфейса IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) в таблице ACL в папке. Этот интерфейс можно использовать для чтения и изменения этих acLs. 
  
## <a name="related-resources"></a>Связанные ресурсы

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

