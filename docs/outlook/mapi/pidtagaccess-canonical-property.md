---
title: Каноническое свойство PidTagAccess
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
ms.assetid: 8c8a882e-62c1-4c57-8c63-ee5849f656b0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b453a7b0cfa04dd94da01089573427a931fb4d4f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316515"
---
# <a name="pidtagaccess-canonical-property"></a>Каноническое свойство PidTagAccess

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит битмаску флагов с указанием операций, доступных клиенту для объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACCESS  <br/> |
|Идентификатор:  <br/> |0x0FF4  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Свойства управления доступом  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство является только для чтения для клиента. Оно должно быть немного **или** равно нулю или более значениям из следующей таблицы. 
  
|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Запись  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Чтение  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Удалить  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Создание подмастерей в иерархии папок  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Создание сообщений контента  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Создание связанных сообщений контента  <br/> |
   
Флаги MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY и MAPI_ACCESS_READ находятся на объектах папок и сообщений, а также в столбце PR_ACCESS в таблицах содержимого и связанных таблицах контента.  Флаги MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS и MAPI_ACCESS_CREATE_HIERARCHY только на объектах папок. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
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

