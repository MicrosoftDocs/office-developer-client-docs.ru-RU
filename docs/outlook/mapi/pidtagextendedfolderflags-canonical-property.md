---
title: Каноническое свойство PidTagExtendedFolderFlags
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagExtendedFolderFlags
api_type:
- HeaderDef
ms.assetid: e0c04f98-3d66-4ab5-ba05-69f9df539fcf
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fe14f6ca101e6a546f99989ecc87b0c516ee5df4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32316354"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Каноническое свойство PidTagExtendedFolderFlags
 
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит расширенные флаги о папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Идентификатор:  <br/> |0x36DA  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство — двоичный поток, содержащий закодированные свойства для папки. Она форматирована как серия элементов подгруппы переменной длины. Первые 8 битов элемента подгруппы — это поле ID, которое указывает, какой флаг представляет подгруппа. Вторые 8 битов — это количество побочных данных, которые следуют за ними.
  
Возможные значения ID:
  
- Invalid
    
   Не используйте это значение
    
- ExtendedFlags
    
   Данные — это значение из четырех byte, отформатированные как:
    
   |**Биты**|**Описание**|
   |:-----|:-----|
   |0-1  <br/> |Зарезервировано.  <br/> |
   |2  <br/> |Установите 0, если приложение должно показывать описание политики.  <br/> |
   |3-5  <br/> |Зарезервировано.  <br/> |
   |6-7  <br/> |Управляет отображением количества сообщений в папке.  <br/> 0 . Использование параметра по умолчанию  <br/> 1 . Использование количества непрочитанные сообщения  <br/> 3. Использование общего числа сообщений  <br/> |
   |8-31  <br/> |Зарезервировано.  <br/> |
   
Зарезервированные элементы можно игнорировать, но существующие значения необходимо сохранить.
    
- SearchFolderID
    
   Поле данных — это поле 16-byte. Когда приложение создает постоянную папку поиска, оно должно установить это поле в папке с таким же значением, как **и PR_WB_SF_TAG** [(PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)двоичное свойство в сообщении папки поиска.
    
- ToDoFolderVersion
    
   Поле данных — это поле 4-byte. Когда приложение создает папку поиска для работы, она должна задать значение этого поля в папке с небольшим значением "integer" 0x000c0000":
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXOCFG]](https://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства данных конфигурации клиента и сервера, например списки общих категорий и рабочие часы.
    
[[MS-OXOSRCH]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Указывает свойства и операции для управления конфигурацией списка папки поиска.
    
### <a name="header-files"></a>Файлы заголовки

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также

- [Свойства MAPI](mapi-properties.md)
- [Канонические свойства MAPI](mapi-canonical-properties.md)
- [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

