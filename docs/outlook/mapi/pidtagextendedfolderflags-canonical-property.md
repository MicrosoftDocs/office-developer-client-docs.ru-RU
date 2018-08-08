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
ms.openlocfilehash: 4a4d3c940539c23be8ec212cb85e3dd4f3a04aab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811122"
---
# <a name="pidtagextendedfolderflags-canonical-property"></a>Каноническое свойство PidTagExtendedFolderFlags
 
**Относится к**: Outlook 
  
Содержит расширенные флаги о папке.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_EXTENDED_FOLDER_FLAGS  <br/> |
|Идентификатор:  <br/> |0x36DA  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Контейнер MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство соответствует двоичный поток, который содержит зашифрованный вложенные свойства папки. В формате задано в формате переменной длины вложенных элементов. Первые 8 бит элемент sub — это поле ID, который указывает, какие виды флаг представляет элемент sub. Второй 8 бит — это число байт данных, выполните.
  
Возможные значения ID:
  
- Invalid
    
   Это значение не используется
    
- ExtendedFlags
    
   Данные являются четыре байта в формате:
    
   |**Бит**|**Описание**|
   |:-----|:-----|
   |0-1  <br/> |Зарезервировано.  <br/> |
   |2  <br/> |Если приложение должно отобразиться описание политики значение 0.  <br/> |
   |3-5  <br/> |Зарезервировано.  <br/> |
   |6-7  <br/> |Определяет отображаемое количество сообщений в папке.  <br/> 0 — использовать по умолчанию  <br/> 1 — используйте количество непрочитанных сообщений  <br/> 3 - использовать общее число сообщений  <br/> |
   |8-31  <br/> |Зарезервировано.  <br/> |
   
Зарезервированные элементов можно пропустить, однако существующие значения, которые необходимо сохранить.
    
- SearchFolderID
    
   Поле данных является полем 16-битное. Когда приложение создает папку сохраняемого поиска, его необходимо установить это поле в общей папке для совпадает со значением **PR_WB_SF_TAG** ([PidTagSearchFolderId)](pidtagsearchfolderid-canonical-property.md)) двоичного свойства папки для поиска сообщения.
    
- ToDoFolderVersion
    
   Поле 4-байтных является поля данных. Когда приложение создает папку Поиск задачи, его необходимо задать значение этого поля в общей папке на прямом целое значение «0x000c0000»:
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOCFG]](http://msdn.microsoft.com/library/7d466dd5-c156-4da9-9a01-75c78e7e1a67%28Office.15%29.aspx)
  
> Указывает расположение и свойства клиентских и серверных данных конфигурации, такие как списки общие категории и рабочее время.
    
[[MS-OXOSRCH]](http://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Задает свойства и операции для управления конфигурации список папок поиска.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также

- [Свойства MAPI](mapi-properties.md)
- [Каноническое свойства MAPI](mapi-canonical-properties.md)
- [Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
- [Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

