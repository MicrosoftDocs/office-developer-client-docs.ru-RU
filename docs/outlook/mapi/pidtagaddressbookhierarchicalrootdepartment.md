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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32326126"
---
# <a name="pidtagaddressbookhierarchicalrootdepartment"></a>Каноническое свойство PidTagAddressBookHierarchicalRootDepartment

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
 Содержит отличительное имя (DN) иерархического корневого адреса (HAB). 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EMS_AB_HAB_ROOT_DEPARTMENT, PR_EMS_AB_HAB_ROOT_DEPARTMENT_A  <br/> |
|Набор свойств:  <br/> |Адресная книга  <br/> |
|Long ID (LID):  <br/> |0x8C98  <br/> |
|Тип данных:  <br/> |PT_STRING8  <br/> |
|Область:  <br/> |Адресная книга Exchange  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство в глобальном контейнере адресов (GAL) и представляет собой отличительное имя корневого иерархического адреса. Это свойство присутствует только в автономной адресной книге и никогда не находится в службе домена Active Directory (AD DS). Звонителям следует MAPI_CACHE_ONLY вызов GetProps, чтобы избежать удаленного вызова процедуры. Если этого нет, для поиска корневого отдела PR_EMS_AB_HAB_ROOT_DEPARTMENT, который имеет тип PT_OBJECT. 
  
После того как корневой отдел будет получен, он может иметь тип объекта MAPI_MAILUSER или MAPI_DISTLIST. Если тип объекта MAPI_DISTLIST, используется новая схема. Если тип объекта MAPI_MAILUSER, используется предыдущая схема. 
  
- Microsoft Office Outlook 2007 Пакет обновления 2 поддерживает обе схемы. 
    
- Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 поддерживают новую схему.
    
В новой схеме все отделские группы также являются списками рассылки и имеют тип MAPI_DISTLIST. Члены ведомствальных групп и отделов в ведомстве получаются с помощью PR_EMS_AB_MEMBER, точно так же, как члены списка рассылки.
  
После того как корневой отдел будет получен, он может иметь тип объекта MAPI_MAILUSER или MAPI_DISTLIST. Если тип объекта MAPI_DISTLIST, используется новая схема. Если тип объекта MAPI_MAILUSER, используется старая схема. 
  
В новой схеме все отдельные группы также являются DLs и имеют тип MAPI_DISTLIST.
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Microsoft Exchange Server протоколы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

