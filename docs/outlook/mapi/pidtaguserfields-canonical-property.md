---
title: Каноническое свойство PidTagUserFields
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: db3a6947-f640-43e8-a2df-71e96560fd81
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 680c9dd9db2743c031de7cda4673d7044ec533e8
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25397431"
---
# <a name="pidtaguserfields-canonical-property"></a>Каноническое свойство PidTagUserFields

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит имя, тип данных и другие сведения о пользовательских полей.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_USERFIELDS  <br/> |
|Идентификатор:  <br/> |0x36E3  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Папки MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Для каждого элемента Outlook хранятся определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего объекта **IMessage** . Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известных как [Определение свойства](propertydefinition-stream-structure.md), который содержит определения полей. Дополнительные сведения о потоке структуры для определения полей можно [Структур потока](stream-structures.md).
  
Для каждой папки Outlook хранятся определения всех пользовательских полей в эту папку в свойстве **PidTagUserFields** сообщения связанный класс сообщения IPC.MS. REN. USERFIELDS - каждой папки, которые, как содержать не более одной сообщение в таблице связанное содержимое этого класса. 
  
> [!NOTE]
> Набор пользовательских полей в папке могут не соответствовать обязательно наборы пользовательских полей в каждой из его элементы. 
  
Набор пользовательских полей в папке отображается в разных местах пользовательского интерфейса Outlook, такие как Выбор поля адреса папки. Свойство **PidTagUserFields** сообщение содержит двоичный поток **FolderUserFields**, который содержит определения полей папки. Дополнительные сведения о структуре потока для определения полей папки можно [Потока структуры папок полей](folder-fields-stream-structures.md) и [Пример FolderUserFields потока](folderuserfields-stream-sample.md).
  
## <a name="section-heading"></a>Заголовок раздела

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Поля и элементы Outlook](outlook-items-and-fields.md)
  
[Добавление определения для нового пользовательского поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

