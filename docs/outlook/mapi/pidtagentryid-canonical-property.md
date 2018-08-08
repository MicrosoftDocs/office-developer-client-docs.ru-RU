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
ms.openlocfilehash: 971462b9e85878677b57ec7b53fe46aa64db6dba
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811121"
---
# <a name="pidtagentryid-canonical-property"></a>Каноническое свойство PidTagEntryId

  
  
**Относится к**: Outlook 
  
Содержит идентификатор запись MAPI, используемый для открытия и изменения свойств конкретного объекта MAPI. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x0FFF  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Идентификатор свойства  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство определяет объект для **OpenEntry** для создания экземпляра и предоставляет доступ ко всем его свойства через соответствующие производного интерфейса **IMAPIProp**. 
  
Это свойство является одним из свойств базовый адрес для всех пользователей, обмена мгновенными сообщениями. 
  
Это свойство может содержать долгосрочные или краткосрочной идентификатор. Краткосрочные идентификаторы, проще и быстрее конструкции, но не могут быть длиннее в области действия и длительность, обычно для текущего сеанса и рабочей станции. Они обычно используется для объектов временные характера, например строк таблицы или элементами диалогового окна и затем заброшены пользователями. Долгосрочные идентификаторы используются для объектов более широкие и длительный характер. 
  
Это свойство всегда доступен через метод [IMAPIProp::GetProps](imapiprop-getprops.md) после первого вызова метода [IMAPIProp::SaveChanges](imapiprop-savechanges.md) . Некоторые поставщики услуг можно сделать его доступным сразу же после создания экземпляра. Поставщик всегда должен возвращать долгосрочного идентификатор записи из **GetProps**. Таким образом, чтобы преобразовать идентификатор краткосрочных долгосрочного, просто откройте объект и получите его это свойство через **GetProps**. 
  
В следующей таблице представлены важные различия между это свойство **PR_RECORD_KEY** ([PidTagRecordKey](pidtagrecordkey-canonical-property.md)) и **PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md)). 
  
|**Характеристики**|**PR_ENTRYID**|**PR_RECORD_KEY**|**PR_SEARCH_KEY**|
|:-----|:-----|:-----|:-----|
|Требуется на объекты вложения  <br/> |Нет  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на объектов папок  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на объектов хранилища сообщений  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Требуется на состояние объектов  <br/> |Да  <br/> |Нет  <br/> |Нет  <br/> |
|Созданные клиента  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Доступные до вызова **SaveChanges** <br/> |Зависит от реализации поставщика  <br/> |Зависит от реализации поставщика  <br/> |Для сообщений, Да. Для других пользователей зависит от реализации поставщика.  <br/> |
|Изменения в операцию копирования  <br/> |Да  <br/> |Да  <br/> |Нет  <br/> |
|Механизм клиента после копирования  <br/> |Нет  <br/> |Нет  <br/> |Да  <br/> |
|Уникальным в рамках  <br/> |Весь мир  <br/> |Экземпляр поставщика  <br/> |Весь мир  <br/> |
|Двоичный сравнимые (как с memcmp)  <br/> |Не используйте [IMAPISupport:: CompareEntryIDs](imapisupport-compareentryids.md) <br/> |Да  <br/> |Да  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCMSG]](http://msdn.microsoft.com/library/7fd7ec40-deec-4c06-9493-1bc06b349682%28Office.15%29.aspx)
  
> Обрабатывает объекты сообщения и вложения.
    
[[MS-OXOABK]](http://msdn.microsoft.com/library/f4cf9b4c-9232-4506-9e71-2270de217614%28Office.15%29.aspx)
  
> Задает свойства и операции для списков пользователей, контактов, групп и ресурсов.
    
[[MS-OXCMAIL]](http://msdn.microsoft.com/library/b60d48db-183f-4bf5-a908-f584e62cb2d4%28Office.15%29.aspx)
  
> Преобразование conventions стандартных электронной почты Интернета объекты сообщений.
    
[[MS-OXCFXICS]](http://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и поток для передачи данных между клиентом и сервером.
    
[[MS-OXCPERM]](http://msdn.microsoft.com/library/944ddb65-6249-4c34-a46e-363fcd37195e%28Office.15%29.aspx)
  
> Обрабатывает извлечения списков разрешений папки, которые хранятся на сервере.
    
[[MS-OXODLGT]](http://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Указывает методы для подключений и настройки почтовых ящиков как делегаты и взаимодействия с объектами сообщений и календаря, когда они действовать от имени другого пользователя.
    
[[MS-OXWAVLS]](http://msdn.microsoft.com/library/69a276d8-5fc3-40ba-acd0-31cf42e6af58%28Office.15%29.aspx)
  
> Указывает схему и методы, которые используются для запроса сведений о доступности для пользователей и ресурсов.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Каноническое свойство PidTagStoreEntryId](pidtagstoreentryid-canonical-property.md)


[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

