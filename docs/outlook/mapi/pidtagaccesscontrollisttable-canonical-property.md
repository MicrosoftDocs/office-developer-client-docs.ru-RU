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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332006"
---
# <a name="pidtagaccesscontrollisttable-canonical-property"></a>Каноническое свойство PidTagAccessControlListTable

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу, состоящую из всех системных списков управления доступом (SACL), применяемых к папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_АКЛ_ТАБЛЕ  <br/> |
|Идентификатор:  <br/> |0x3FE0  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Управление доступом  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство присутствует для всех объектов Folder на сервере Exchange. Значения, включенные в это свойство, используются для чтения и изменения списков управления доступом (ACL) в папках. Вы можете использовать метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) с идентификатором интерфейса **иид_иексчанжемодифитабле** для получения интерфейса [ИЕКСЧАНЖЕМОДИФИТАБЛЕ: IUnknown](iexchangemodifytableiunknown.md) для таблицы ACL в папке. Этот интерфейс можно использовать для чтения и изменения этих списков управления доступом. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

