---
title: Каноническое свойство PidTagAdditionalRenEntryIdsEx
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagAdditionalRenEntryIdsEx
api_type:
- HeaderDef
ms.assetid: b5e896e7-c0c6-4ad1-bf91-9daba3a1e4d4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 57ab68d4c53693c769a4aadf8737f57ef5e73fcd
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335205"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Каноническое свойство PidTagAdditionalRenEntryIdsEx

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит специальные ИД записи папок для объекта магазина. Каждая запись в этом многомерном свойстве может быть соедино одному или нескольким ИД записи, то есть существует связь между записью и связанными с ней ID-данными.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Идентификатор:  <br/> |0x36D9  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Outlook приложение  <br/> |
   
## <a name="remarks"></a>Примечания

Если это свойство используется, он содержит массив блоков, которые задают ID записи для папок. Блоки следуют формату, указанному в следующих четырех таблицах.
  
**Блок PersistData**

|**Имя**|**Тип**|**Размер**|**Описание**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Значение идентификатора типа для этой **записи PersistData.** Список допустимого значения см. в таблице "Значения PersistBlockType".  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Размер поля **DataElements** в bytes.  <br/> |
|**DataElements** <br/> |массив блоков **PersistElement**  <br/> |переменная  <br/> |Указывает, сколько **записей PersistElement** существует для магазина. См. таблицу "PersistElement Block" для формата этой структуры.  <br/> |
   
**Значения PersistBlockType**

|**Name**|**Value**|**Описание**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Указывает, что больше не будут обрабатываться блоки **PersistData.**  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Указывает, что этот блок содержит данные для папки подписки RSS.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Указывает, что этот блок содержит данные для папки Tracked Mail Processing.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Указывает, что этот блок содержит данные для To-Do папки поиска.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Указывает, что этот блок содержит данные для папки Параметры действий.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Это значение зарезервировано.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Указывает, что этот блок содержит данные для папки "Предложенные контакты".  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Указывает, что этот блок содержит данные для папки Поиска контактов.  <br/> Используется только Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Указывает, что этот блок содержит данные для папки списков контактов мгновенных сообщений (IM). Эталонная папка содержит персональные списки рассылки (PDLs), представляющие каждую группу в списке контактов по мгновенным данным.  <br/> Используется как Outlook, так и Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Указывает, что этот блок содержит данные для папки контактов с мгновенными доступами. Эталонная папка содержит отдельные контакты, на которые ссылается группа контактов im.  <br/> Используется как Outlook, так и Exchange.  <br/> |
   
Если значение **PersistBlockType** не является одним из определенных здесь, блок **PersistData** игнорируется и обработка продолжается до тех пор, пока не будет обработан PERSIST_SENTINEL **PersistID** или не будет достигнут конец потока. 
  
**PersistElementBlock**

|**Имя**|**Тип**|**Размер**|**Описание**|
|:-----|:-----|:-----|:-----|
|**ElementID** <br/> |WORD  <br/> |2  <br/> |Указывает значение идентификатора типа для этого блока **PersistElement.** Список допустимого значения см. в таблице "PersistElementType Values".  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Указывает размер в bytes поля **ElementData.**  <br/> |
|**ElementData** <br/> |массив двоичных данных  <br/> |переменная  <br/> |Содержит данные для этой **пары PersistID**  +  **ElementID.**  <br/> |
   
**Значения PersistElementType**

|**Name**|**Value**|**Значение ElementDataSize**|**Описание**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Указывает, что поле **ElementData этого** блока содержит значение DWORD Header. Интерпретация этого значения зависит от типа **PersistID** блока.  <br/> Для всех **типов PersistID,** указанных [в [MS-OXOSFLD],](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)это значение нулевое.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |переменная  <br/> |Указывает, что этот блок содержит **EntryID** папки, указанной **PersistID.**  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Указывает, что больше **блоки PersistElement** не будут обрабатываться.  <br/> |
   
Если значение **PersistElementType** не является одним из определенных здесь, блок **PersistElement** игнорируется и обработка продолжается до обработки ELEMENT_SENTINEL **ElementID** или окончания потока. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные Exchange Server протоколы.
    
[[MS-OXCSPAM]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списков разрешить или блокировать и определение нежелательных сообщений электронной почты.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Указывает свойства и операции для создания и размещения специальных папок в почтовом ящике.
    
[[MS-OXPHISH]](https://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Идентифицирует и отмечает сообщения электронной почты, предназначенные для обмана получателей в разглашать конфиденциальные сведения (например, пароли и другие личные данные) в ненадежный источник.
    
### <a name="header-files"></a>Файлы заголовки

Mapitags.h
  
> Содержит определения свойств, перечисленных в качестве связанных свойств.
    
Mapidefs.h
  
> Предоставляет определения типов данных.
    
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)
  
[Канонические свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с каноническими именами свойств](mapping-mapi-names-to-canonical-property-names.md)

