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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32360741"
---
# <a name="pidtaguserfields-canonical-property"></a>Каноническое свойство PidTagUserFields

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит имя, тип данных и другие сведения о поле, определенном пользователем.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_USERFIELDS  <br/> |
|Идентификатор:  <br/> |0x36E3  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Папка MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Для каждого элемента Outlook определения всех пользовательских полей в свойстве [PidLidPropertyDefinitionStream](pidlidpropertydefinitionstream-canonical-property.md) соответствующего **объекта IMessage.** Свойство **PidLidPropertyDefinitionStream** содержит двоичный поток, известный как [PropertyDefinition,](propertydefinition-stream-structure.md)который содержит определения полей. Дополнительные сведения о структурах потоков для определений полей см. в [руб.](stream-structures.md)
  
Для каждой папки Outlook определения всех определенных пользователем полей в этой папке в свойстве **PidTagUserFields** связанного сообщения класса IPC.MS. REN. USERFIELDS — каждая папка, как предполагается, содержит не более одного сообщения этого класса в связанной таблице содержимого. 
  
> [!NOTE]
> Набор пользовательских полей в папке не обязательно совпадает с наборами определенных пользователем полей в каждом из элементов. 
  
Набор пользовательских полей в папке отображается в разных Outlook пользовательского интерфейса, например в поле выбора папки. Свойство **PidTagUserFields** сообщения содержит двоичный поток **FolderUserFields,** содержащий определения полей папок. Дополнительные сведения о структурах потока для определений полей папок см. в примере [Folder Fields Stream Structures](folder-fields-stream-structures.md) и [folderUserFields Stream Sample.](folderuserfields-stream-sample.md)
  
## <a name="section-heading"></a>Заголовок раздела

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Outlook Элементы и поля](outlook-items-and-fields.md)
  
[Добавление определения для нового User-Defined поля](how-to-add-a-definition-for-a-new-user-defined-field.md)
  
[Пример потока PropertyDefinition](propertydefinition-stream-sample.md)
  
[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

