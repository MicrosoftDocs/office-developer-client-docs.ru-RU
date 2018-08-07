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
ms.openlocfilehash: bb00d4e0e1437f9b3c13ac5e7d0a9dc4f3610d32
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810793"
---
# <a name="pidtagaccess-canonical-property"></a>Каноническое свойство PidTagAccess

  
  
**Относится к**: Outlook 
  
Содержит битовую маску флагов, указывающее, операции, которые доступны для клиента для объекта.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ACCESS  <br/> |
|Идентификатор:  <br/> |0x0FF4  <br/> |
|Тип данных:  <br/> |PT_LONG  <br/> |
|Область:  <br/> |Элемент управления доступа к свойствам  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство доступно только для чтения для клиента. Он должен быть побитовое **или** ноль или больше значений из следующей таблицы. 
  
|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|MAPI_ACCESS_MODIFY  <br/> |0x00000001  <br/> |Запись  <br/> |
|MAPI_ACCESS_READ  <br/> |0x00000002  <br/> |Чтение  <br/> |
|MAPI_ACCESS_DELETE  <br/> |0x00000004  <br/> |Delete  <br/> |
|MAPI_ACCESS_CREATE_HIERARCHY  <br/> |0x00000008  <br/> |Создание вложенных папок в иерархии папок  <br/> |
|MAPI_ACCESS_CREATE_CONTENTS  <br/> |0x00000010  <br/> |Создание сообщения  <br/> |
|MAPI_ACCESS_CREATE_ASSOCIATED  <br/> |0x00000020  <br/> |Создание связанного содержимого сообщений  <br/> |
   
Флаги MAPI_ACCESS_DELETE, MAPI_ACCESS_MODIFY и MAPI_ACCESS_READ находятся в папке и объекты сообщений и в столбце **PR_ACCESS** в содержимое и связанного содержимого таблицы. Флаги MAPI_ACCESS_CREATE_ASSOCIATED, MAPI_ACCESS_CREATE_CONTENTS и MAPI_ACCESS_CREATE_HIERARCHY находятся в папке объекты только. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
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

