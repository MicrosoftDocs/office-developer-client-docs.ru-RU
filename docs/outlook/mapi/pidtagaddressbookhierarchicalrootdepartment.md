---
title: Каноническое свойство PidTagAddressBookHierarchicalRootDepartment
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAddressBookHierarchicalRootDepartment
api_type:
- HeaderDef
ms.assetid: c611640b-1a70-4a76-b7ff-c8ad8d320892
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 22a1a62f4ee6ff492f36eb18e2d92c8d70febd72
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25382612"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>Каноническое свойство PidTagAddressBookHierarchicalRootDepartment

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
 Содержит различающееся имя (DN) корневого иерархических адресных (иерархической адресной книги). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Набор свойств:  <br/> |Адресная книга  <br/> |
|Длинный идентификатор (КРЫШКА):  <br/> |0x8C98  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Адресная книга Exchange  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство для контейнера глобального списка адресов, представляет различающееся имя корневого иерархических адресных. Это свойство присутствует только в автономной адресной книги и никогда не в доменных службах Active Directory (AD DS). Вызывающие MAPI_CACHE_ONLY передать GetProps звонок во избежание удаленного вызова процедуры. Если это не указан, абонентов следует использовать PR_EMS_AB_HAB_ROOT_DEPARTMENT, который имеет тип PT_OBJECT, поиск корневого отдела. 
  
После получения отдела корневой он может иметь тип объекта MAPI_MAILUSER или MAPI_DISTLIST. Если тип объекта MAPI_DISTLIST, новые схемы работает. Если тип объекта MAPI_MAILUSER, предыдущей схеме работает. 
  
- Пакет обновления 2 для Microsoft Office Outlook 2007 поддерживает обеих схем. 
    
- Microsoft Outlook 2010 и Microsoft Outlook 2013 поддерживает новую схему.
    
На новой схемой всех отделов групп, также списки рассылки и типа MAPI_DISTLIST. Члены отдела групп и подразделений внутри отдела групп можно получить с помощью PR_EMS_AB_MEMBER, так же, как членов списка рассылки.
  
После получения отдела корневой он может иметь тип объекта MAPI_MAILUSER или MAPI_DISTLIST. Если тип объекта MAPI_DISTLIST, используется новой схемой. Если тип объекта MAPI_MAILUSER, используется со старой схемой. 
  
На новой схемой всех отделов групп, также списки рассылки и типа MAPI_DISTLIST.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Microsoft Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

