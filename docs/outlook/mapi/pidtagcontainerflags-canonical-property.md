---
title: Каноническое свойство PidTagContainerFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerFlags
api_type:
- HeaderDef
ms.assetid: 66b8d333-227e-464d-8cf9-cd8a5ff15efb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c9c446097213e5b743a47ec32db17ec0afe63b78
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32357549"
---
# <a name="pidtagcontainerflags-canonical-property"></a>Каноническое свойство PidTagContainerFlags

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битмаску флагов, описывающих возможности контейнера адресной книги. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3600  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Для bitmask можно установить один или несколько следующих флагов:
  
AB_FIND_ON_OPEN 
  
> Отображает диалоговое окно для запроса ограничения перед отображением любого содержимого контейнера. 
    
AB_MODIFIABLE 
  
> Записи можно добавлять и удалять из контейнера. Этот флаг не указывает, можно ли изменять любые записи в контейнере.
    
AB_RECIPIENTS 
  
> Контейнер может удерживать получателей. Этот флаг не указывает, действительно ли получатели присутствуют в контейнере и могут ли они быть добавлены или удалены. 
    
AB_SUBCONTAINERS 
  
> Контейнер может вметь детские контейнеры. Этот флаг не указывает, присутствуют ли какие-либо подконтейеры в контейнере, а также могут ли они быть добавлены или удалены. AB_SUBCONTAINERS должен быть установлен для контейнера для [поддержки IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Записи не могут быть добавлены или удалены из контейнера. Этот флаг не указывает, можно ли изменять любые записи в контейнере. 
    
Флаг AB_FIND_ON_OPEN рекомендуется использовать для контейнеров, используемых с онлайн-службами или с медленным подключением к серверам. При открываемом контейнере с AB_FIND_ON_OPEN установлен диалоговое окно **Find** представляется пользователю для ограничения отображаемого пользователя обмена сообщениями. Даже частичная спецификация, ограничивающая пользователей обмена сообщениями, может значительно ускорить отображение содержимого. 
  
Должен быть AB_MODIFIABLE или AB_UNMODIFIABLE флаг. Оба флага могут указывать на то, что контейнер не знает, можно ли его изменить или нет, например, если изменение зависит от прав пользователя на доступ. В этом случае клиентские приложения должны попытаться вызвать и изучить код возврата, чтобы определить возможности контейнера. Клиент обычно начинает с изучения AB_MODIFIABLE. Если она установлена, клиент совершает вызов, который пытается изменить контейнер и проверяет возвращаемого значения. 
  
Флаг AB_MODIFIABLE не указывает, какие типы записей можно добавить в контейнер. Чтобы определить это, клиент должен использовать соответствующий метод [OpenProperty,](imapiprop-openproperty.md) чтобы открыть свойство[PR_CREATE_TEMPLATES (PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md)  Открытие **PR_CREATE_TEMPLATES** возвращает разовую таблицу контейнера, перечисляя типы записей, которые можно создать в контейнере. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Обрабатывает сообщения клиента с сервером интерфейса поставщика служб имени (NSPI).
    
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

