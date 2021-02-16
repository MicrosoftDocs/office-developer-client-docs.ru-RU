---
title: Каноническое свойство PidTagEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagEntryId
api_type:
- HeaderDef
ms.assetid: ca02e873-c2d2-4d58-8df8-c05fbcdc8fba
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: feb34cdbf8ba917936c3272bcaaf6eff040ddc3a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328590"
---
# <a name="pidtagentryid-canonical-property"></a>Каноническое свойство PidTagEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит идентификатор записи MAPI, используемый для открытия и изменения свойств определенного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0FFF  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Свойства ID  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство идентифицирует объект **для openEntry,** который создается, и предоставляет доступ ко всем его свойствам с помощью соответствующего производного интерфейса **IMAPIProp.** 
  
Это свойство является одним из базовых свойств адреса для всех пользователей обмена сообщениями. 
  
Это свойство может содержать долгосрочный или краткосрочный идентификатор. Краткосрочные идентификаторы проще и быстрее создавать, но ограничены по своей области и продолжительности, как правило, для текущего сеанса и рабочей станции. Обычно они используются для объектов временного характера, таких как строки таблиц или записи диалоговых окной, а затем отбрасыются. Долгосрочные идентификаторы используются для объектов более широкого и долгосрочного характера. 
  
Это свойство всегда доступно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges.](imapiprop-savechanges.md) Некоторые поставщики услуг могут сделать его доступным сразу же после его искомой работы. Поставщик всегда должен возвращать долгосрочный идентификатор записи из **GetProps.** Таким образом, чтобы преобразовать краткосрочный идентификатор в долгосрочный, просто откройте объект и получите его это свойство с помощью **GetProps.** 
  
В следующей таблице скомбинирована важная разница между этим **свойством: PR_RECORD_KEY** ([PidTagRecordKey)](pidtagrecordkey-canonical-property.md)и **PR_SEARCH_KEY** ([PidTagSearchKey).](pidtagsearchkey-canonical-property.md) 
  
|**Характеристика**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Требуется для объектов вложений  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов папок  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов, хранимых в сообщениях  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется для объектов состояния  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Создано клиентом  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступно перед вызовом **SaveChanges** <br/> |Зависит от реализации поставщика  <br/> |Зависит от реализации поставщика  <br/> |Да, для сообщений. Для других зависит от реализации поставщика.  <br/> |
|Изменено в операции копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Может изменяться клиентом после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальный в пределах  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Двоичное сравнимое (как с memcmp)  <br/> |Отсутствие использования [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCMSG]](https://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщений и вложений.
    
[[MS-OXOABK]](https://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Указывает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](https://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразуется из стандартных интернет-соглашений электронной почты в объекты сообщений.
    
[[MS-OXCFXICS]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток передачи данных между клиентом и сервером.
    
[[MS-OXCPERM]](https://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает и получить списки разрешений папок, хранимые на сервере.
    
[[MS-OXODLGT]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы подключения и настройки почтовых ящиков в качестве делегатов, а также взаимодействия с объектами сообщений и календаря, когда они действуют от имени другого пользователя.
    
[[MS-OXWAVLS]](https://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Указывает схему и методы, используемые для запроса сведений о доступности для пользователей и ресурсов.
    
### <a name="header-files"></a>Файлы заголовок

Mapidefs.h
  
> Предоставляет определения типов данных.
    
Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

