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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360776"
---
# <a name="pidtagdisplaytypeex-canonical-property"></a>Каноническое свойство PidTagDisplayTypeEx

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит тип записи в отношении того, как она должна отображаться в строке таблицы глобального списка адресов. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_DISPLAY_TYPE_EX  <br/> |
|Идентификатор:  <br/> |0x3905  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство указывает тип записи в отношении того, как она должна отображаться в глобальном списке адресов. Он предоставляет дополнительные сведения, которые не могут быть представлены **в** PR_DISPLAY_TYPE ([PidTagDisplayType).](pidtagdisplaytype-canonical-property.md)
  
> [!NOTE]
> Значения обоих  PR_DISPLAY_TYPE и этого свойства начинаются с "DT_" и определяются в Mapitags.h. Все значения, не задокументированные, зарезервированы для MAPI. Клиентские приложения не должны определять новые значения и должны быть готовы к обращению с недокументным значением. 
  
Существуют некоторые макросы, которые могут помочь определить атрибуты объекта, например локальный, удаленный или контролируемый безопасностью. К этим макросам относятся: 
  
|**Macro**|**Значение**|
|:-----|:-----|
|DTE_FLAG_REMOTE_VALID  <br/> |0x80000000)  <br/> |
|DTE_FLAG_ACL_CAPABLE  <br/> |0x40000000  <br/> |
|DTE_MASK_REMOTE  <br/> |0x0000ff00  <br/> |
|DTE_MASK_LOCAL  <br/> |0x000000ff  <br/> |
|DTE_IS_REMOTE_VALID(v)  <br/> |(!! ((v) &amp; DTE_FLAG_REMOTE_VALID)  <br/> |
|DTE_IS_ACL_CAPABLE(v)  <br/> |(!! ((v) &amp; DTE_FLAG_ACL_CAPABLE))  <br/> |
|DTE_REMOTE(v)  <br/> |(((v) &amp; DTE_MASK_REMOTE) \> \> 8)  <br/> |
|DTE_LOCAL(v)  <br/> |((v) &amp; DTE_MASK_LOCAL)  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |
   
Ниже приводится несколько заметок о том, как использовать эти макрос. 
  
- Чтобы проверить, является ли запись удаленной записью в другом лесу, применив макрос DTE_IS_REMOTE_VALID к значению этого свойства, чтобы проверить, установлен ли флаг DTE_FLAG_REMOTE_VALID в записи. Если это удаленная запись, можно узнать тип удаленной записи с помощью макроса DTE_REMOTE. 
    
- В конфигурациях с одним и межлесным лесом, **если PR_DISPLAY_TYPE** имеет значение DT_DISTLIST, а DTE_IS_REMOTE_VALID — false, применение макроса DTE_LOCAL к значению этого свойства позволит дополнительно определить тип объекта как DT_DISTLIST (список рассылки) или DT_SEC_DISTLIST (список рассылки безопасности). 
    
- Если применить макрос DTE_LOCAL к значению PR_DISPLAY_TYPE_EX и он возвращает тип DT_REMOTE_MAILUSER, то запись является удаленной записью.  
    
- В конфигурации с одним лесом или в конфигурации между лесами, где репликацией управляет список управления доступом (ACL), можно использовать макрос DTE_IS_ACL_CAPABLE, чтобы определить, является ли запись участников безопасности.
    
В конфигурации между **лесами** PR_DISPLAY_TYPE имеет значение DT_REMOTE_MAILUSER. Применение макроса DTE_REMOTE к значению этого свойства может позволить получить тип удаленной записи. Возможные типы удаленной записи: 
  
|**Тип удаленной записи**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|DT_AGENT  <br/> |((ULONG) 0x00000003)  <br/> |Динамический список рассылки.  <br/> |
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Список рассылки.  <br/> |
|DT_EQUIPMENT  <br/> |((ULONG) 0x00000008)  <br/> |Оборудование, например принтер или проектор.  <br/> |
|DT_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Пользователь с почтовым ящиком.  <br/> |
|DT_REMOTE_MAILUSER  <br/> |((ULONG) 0x00000000)  <br/> |Запись списка адресов в глобальном списке адресов.  <br/> |
|DT_ROOM  <br/> |((ULONG) 0x00000007)  <br/> |Конференц-зал.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Список рассылки безопасности.  <br/> |
   
Если в конфигурации с одним лесом  и между лесами PR_DISPLAY_TYPE имеет значение DT_DISTLIST, а DTE_IS_REMOTE_VALID — false, применение макроса DTE_LOCAL к значению этого свойства позволит получить тип списка рассылки. Возможные типы списка рассылки: 
  
|**Тип списка рассылки**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|DT_DISTLIST  <br/> |((ULONG) 0x00000001)  <br/> |Список рассылки.  <br/> |
|DT_SEC_DISTLIST  <br/> |((ULONG) 0x00000009)  <br/> |Список рассылки безопасности.  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

