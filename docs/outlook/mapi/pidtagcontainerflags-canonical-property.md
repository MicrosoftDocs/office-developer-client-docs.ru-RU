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

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит битовуюmass флагов, описывающих возможности контейнера адресной книги. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_CONTAINER_FLAGS  <br/> |
|Идентификатор:  <br/> |0x3600  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Адресная книга  <br/> |
   
## <a name="remarks"></a>Примечания

Для битовойmask можно установить один или несколько из следующих флагов:
  
AB_FIND_ON_OPEN 
  
> Отображает диалоговое окно для запроса ограничения перед отображением содержимого контейнера. 
    
AB_MODIFIABLE 
  
> Записи можно добавлять в контейнер и удалять из него. Этот флаг не указывает, можно ли изменять какие-либо записи в контейнере.
    
AB_RECIPIENTS 
  
> Контейнер может удерживать получателей. Этот флаг не указывает, присутствуют ли в контейнере какие-либо получатели или могут ли они быть добавлены или удалены. 
    
AB_SUBCONTAINERS 
  
> Контейнер может вметь в себя все контейнеры. Этот флаг не указывает, присутствуют ли в контейнере какие-либо подподдержки и могут ли они быть добавлены или удалены. AB_SUBCONTAINERS необходимо настроить для контейнера поддержку [IMAPIContainer::GetHierarchyTable](imapicontainer-gethierarchytable.md). 
    
AB_UNMODIFIABLE 
  
> Записи нельзя добавлять в контейнер или удалять из него. Этот флаг не указывает, можно ли изменять какие-либо записи в контейнере. 
    
Флаг AB_FIND_ON_OPEN рекомендуется для контейнеров, используемых с веб-службами или при медленных подключениях к серверам. Когда откроется контейнер с AB_FIND_ON_OPEN, пользователю  будет отобрато диалоговое окно "Найти", чтобы ограничить отображаемую систему обмена сообщениями. Даже частичная спецификация, ограничивающая пользователей сообщений, может существенно ускорить отображение содержимого. 
  
Необходимо установить AB_MODIFIABLE или AB_UNMODIFIABLE флага. Оба флага могут указывать на то, что контейнеру не известно, можно ли его изменить, например, если изменение зависит от прав доступа пользователя. В этом случае клиентские приложения должны попытаться вызвать и изучить код возврата, чтобы определить возможности контейнера. Клиент обычно начинает с проверки AB_MODIFIABLE. Если он установлен, клиент совершает вызов, который пытается изменить контейнер и проверяет возвращаемого значения. 
  
Флаг AB_MODIFIABLE не указывает, какие типы записей можно добавить в контейнер. Чтобы определить это, клиент должен использовать соответствующий метод [OpenProperty,](imapiprop-openproperty.md) чтобы открыть **свойство PR_CREATE_TEMPLATES** контейнера [(PidTagCreateTemplates).](pidtagcreatetemplates-canonical-property.md) Открытие **PR_CREATE_TEMPLATES** приводит к возврату одностолковой таблицы контейнера с описанием типов записей, которые можно создать в контейнере. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-NSPI]](https://msdn.microsoft.com/library/6dd0a3ea-b4d4-4a73-a857-add03a89a543%28Office.15%29.aspx)
  
> Обрабатывает взаимодействие клиента с сервером интерфейса поставщика службы имен (NSPI).
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных как связанные свойства.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

