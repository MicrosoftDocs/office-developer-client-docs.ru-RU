---
title: Каноническое свойство PidTagDisplayTypeEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagDisplayTypeEx
api_type:
- HeaderDef
ms.assetid: 23074402-6ac1-47f1-8a49-b8909f98a26e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 6eea30188543cb06545a9efad705f5593d4227a7
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25393245"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Каноническое свойство PidTagDisplayTypeEx

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип записи, в отношении как операция должно отображаться на строку в таблице для глобального списка адресов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Идентификатор:  <br/> |0x3905  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет тип записи, в отношении как должны отображаться в глобальном списке адресов. Они предоставляют дополнительную информацию, которая не может быть представлена в **PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)).
  
> [!NOTE]
> Значения **PR_DISPLAY_TYPE** и это свойство начинаются с «DT_» и определяются в Mapitags.h. Все значения не задокументирован зарезервированы для MAPI. Клиентские приложения не должны определить все новые значения и должны быть готовы для смягчения последствий недокументированного значения. 
  
Существуют некоторые макросы, которые могут помочь определить атрибуты объекта, например, будет ли это локального, удаленного или контролем безопасности. Эти макросы включают: 
  
|**Макрос**|**Значение**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000FF00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |
   
Ниже приведены некоторые примечания об использовании этих макросов. 
  
- Чтобы проверить, является ли запись удаленного запись в другом лесу, относятся к значение этого свойства, чтобы проверить, установлен ли флажок DTE_FLAG_REMOTE_VALID в запись макроса DTE_IS_REMOTE_VALID. Если удаленный запись, чтобы затем узнать тип удаленные записи с помощью макроса DTE_REMOTE. 
    
- В конфигурациях с одним лесом и между лесами когда **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST и DTE_IS_REMOTE_VALID присвоено значение false, применение макрос DTE_LOCAL значение этого свойства может позволяют затем определить тип объекта как DT_DISTLIST (список рассылки) или DT_SEC_DISTLIST (список рассылки безопасности). 
    
- Если применить макрос DTE_LOCAL значение **PR_DISPLAY_TYPE_EX** , он возвращает тип DT_REMOTE_MAILUSER запись является записью удаленного. 
    
- В одном лесу или в конфигурации между лесами, где репликации, контролируются с списка управления доступом (ACL) макрос DTE_IS_ACL_CAPABLE можно использовать для определения, является ли запись участника безопасности.
    
В конфигурации между лесами **PR_DISPLAY_TYPE** имеет значение DT_REMOTE_MAILUSER. Применение макрос DTE_REMOTE значение этого свойства позволяет получить тип удаленные записи. Ниже представлены возможные типы удаленного элемента. 
  
|**Тип записи удаленного**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0X00000003)  <br/> |Список динамических рассылки.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Список рассылки.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0X00000008)  <br/> |Оборудование, например, принтера или проектор.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |Пользователь с почтовым ящиком.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0X00000000)  <br/> |Запись списка адресов в глобальном списке адресов.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0X00000007)  <br/> |Конференц-зала.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Список рассылки безопасности.  <br/> |
   
В одном лесу и между лесами конфигурации, когда **PR_DISPLAY_TYPE** имеет значение DT_DISTLIST и DTE_IS_REMOTE_VALID имеет значение false, применение макрос DTE_LOCAL значение этого свойства может позволяют получить тип списка рассылки . Ниже представлены возможные типы списков рассылки. 
  
|**Тип списка рассылки**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0X00000001)  <br/> |Список рассылки.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0X00000009)  <br/> |Список рассылки безопасности.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
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

