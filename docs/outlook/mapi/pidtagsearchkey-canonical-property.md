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
  
Содержит схожий двоичный ключ, который идентифицирует связанные объекты для поиска.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_SEARCH_KEY  <br/> |
|Идентификатор:  <br/> |0x300B  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство обеспечивает трассировка связанных объектов, таких как копии сообщений, и упрощает поиск нежелательных вхождений, таких как дублирующиеся получатели.
  
MAPI использует определенные правила для создания ключей поиска для получателей сообщений. Ключ поиска формируется путем сбиения типа адреса (в верхнем регистре), двоеточия ":", адреса электронной почты в канонической форме и завершающего символа null. Каноническая форма здесь означает, что адреса с регистром отображаются в правильном случае, а адреса, не чувствительные к регистру, преобразуются в верхний регистр. Это важно для сохранения корреляций между сообщениями.
  
Для объектов сообщений это свойство доступно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) сразу после создания сообщения. Для других объектов он доступен после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Так как это свойство является изменяемым, его невозможно получить через **GetProps,** пока вызов **SaveChanges** не заблокировает значения, установленные или измененные методом [IMAPIProp::SetProps.](imapiprop-setprops.md) 
  
Для профилей MAPI также передает жестко заданная часть профиля с именем **MUID_PROFILE_INSTANCE**, с этим свойством в качестве одного свойства. Этот ключ гарантированно будет уникальным для всех когда-либо созданных профилей и может быть более надежным, чем **свойство PR_PROFILE_NAME** ([PidTagProfileName),](pidtagprofilename-canonical-property.md)которое может быть, например, удалено и повторно создано с тем же именем.
  
В следующей таблице водятся  важные различия между PR_ENTRYID [(PidTagEntryId),](pidtagentryid-canonical-property.md) **PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и этим свойством.
  
|**Характеристика**|PR_ENTRYID***|PR_RECORD_KEY***|PR_SEARCH_KEY***|
|:-----|:-----|:-----|:-----|
|Требуется для объектов вложений  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов папок  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов, хранимых в сообщениях  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов состояния  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Можно с помощью клиента  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступно до **SaveChanges** <br/> |Зависит от реализации поставщика  <br/> |Зависит от реализации поставщика  <br/> |Да, для сообщений. Для других это зависит от реализации поставщика.  <br/> |
|Изменено в операции копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Может изменяться клиентом после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальный в ...  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Двоичное сравнимое (как с memcmp)  <br/> |Нет — используйте [IMAPISupport::CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagResponsibility](pidtagresponsibility-canonical-property.md)
  
[Каноническое свойство PidTagStoreRecordKey](pidtagstorerecordkey-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

