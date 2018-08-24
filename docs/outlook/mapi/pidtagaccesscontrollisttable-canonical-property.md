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
ms.openlocfilehash: 40a2bc8a27ec3ce3df610b9c7364719c2b5ee750
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572790"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Каноническое свойство PidTagAccessControlListTable

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу, состоящую из всех системы списки управления доступом (SACL) применения к папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACL_TABLE  <br/> |
|Идентификатор:  <br/> |0x3FE0  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство присутствует на всех объектов папок на сервере Exchange. Значения, включенные в этом свойстве используются для чтения, и изменение управления доступом списков управления доступом к папкам. Можно использовать метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) с идентификатором интерфейса **IID_IExchangeModifyTable** для получения [IExchangeModifyTable: IUnknown](iexchangemodifytableiunknown.md) интерфейса в таблице списка управления Доступом на папку. Этот интерфейс можно использовать для чтения и изменения эти списки управления доступом. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

