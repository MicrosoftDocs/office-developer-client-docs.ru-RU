---
title: Каноническое свойство PidTagSearchKey
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_type:
- COM
ms.assetid: fcab369a-a1f4-4425-a272-e35046914a4d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 9e6b9ddf37c1db8ea28ae2f82caed2a487e551e5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345467"
---
# <a name="pidtagsearchkey-canonical-property"></a>Каноническое свойство PidTagSearchKey

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит ключ, сравнимый с двоичным кодом, который определяет коррелированные объекты для поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x300B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства идентификатора  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство предоставляет трассировку для связанных объектов, таких как копии сообщений, и облегчает поиск нежелательных экземпляров, таких как повторяющиеся получатели.
  
MAPI использует определенные правила для создания ключей поиска для получателей сообщений. Ключ поиска формируется путем сцепления типа адреса (в верхнем регистре), знака двоеточия ":", адреса электронной почты в канонической форме и завершающего знака null. Каноническую форму это означает, что адреса с учетом регистра отображаются в правильном регистре, а адреса без учета регистра преобразуются в верхний регистр. Это важно для сохранения корреляции между сообщениями.
  
Для объектов Message это свойство доступно через метод [IMAPIProp::-PROPS](imapiprop-getprops.md) сразу после создания сообщения. Для других объектов он доступен после первого вызова метода [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) . Так как это свойство является изменяемым, его можно получить с помощью метода- **PROPS** до тех пор, пока вызов **SaveChanges** не зафиксирует какие-либо значения, установленные или измененные методом [IMAPIProp:: SetProps](imapiprop-setprops.md) . 
  
В случае профилей MAPI также послужит жестко закодированным разделом профиля с именем **MUID_PROFILE_INSTANCE**, в котором это свойство является одним свойством. Этот ключ гарантированно уникален среди всех созданных профилей и может быть более надежным, чем свойство **PR_PROFILE_NAME** ([PidTagProfileName](pidtagprofilename-canonical-property.md)), которое может быть, например, удалено и создано повторно с тем же именем.
  
В следующей таблице приведены важные различия между **PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)), **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и этим свойством.
  
|**Характеристика**|PR_ENTRYID * * * *|PR_RECORD_KEY * * * *|PR_SEARCH_KEY * * * *|
|:-----|:-----|:-----|:-----|
|Обязательный атрибут для объектов вложений  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Обязательный атрибут для объектов Folder  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Обязательный для объектов хранилища сообщений  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Обязательные для объектов Status  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Создаваемое клиентом  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступно перед **SaveChanges** <br/> |Зависит от реализации поставщика  <br/> |Зависит от реализации поставщика  <br/> |Для сообщений — да. Для других пользователей это зависит от реализации поставщика.  <br/> |
|Изменено в операции копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Изменение клиентом после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальный в пределах...  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Сравнение двоичных файлов (как и в случае с мемкмп)  <br/> |Нет — используйте [имаписуппорт:: метод compareentryids](imapisupport-compareentryids.md) <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКМСГ]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS — ОКСОАБК]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Каноническое свойство PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

