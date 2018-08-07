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
ms.openlocfilehash: d3a8dc45bb131f5d2e7ff370617a10e3096a99f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810808"
---
# <a name="pidtagadditionalrenentryidsex-canonical-property"></a>Каноническое свойство PidTagAdditionalRenEntryIdsEx

  
  
**Относится к**: Outlook 
  
Содержит запись специальную папку идентификаторы для объекта хранилища. Каждая запись в этом многозначные свойства может быть сопоставлен один или несколько идентификаторов запись, то есть один ко многим взаимосвязь запись и ее связанный запись идентификаторы.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_ADDITIONAL_REN_ENTRYIDS_EX  <br/> |
|Идентификатор:  <br/> |0x36D9  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Приложения Outlook  <br/> |
   
## <a name="remarks"></a>Замечания

При использовании этого свойства содержит массив блоки, которое указывает запись идентификаторы папок. Блоки следуйте формата, заданного в следующих четырех таблиц.
  
**PersistData блокировки**

|**Имя**|**Тип**|**Size**|**Описание**|
|:-----|:-----|:-----|:-----|
|**PersistID** <br/> |WORD  <br/> |2  <br/> |Введите значение идентификатора для этой записи **PersistData** . В разделе таблицы «PersistBlockType значения» для списка допустимых значений.  <br/> |
|**DataElementsSize** <br/> |WORD  <br/> |2  <br/> |Размер, в байтах, поля **DataElements** .  <br/> |
|**DataElements** <br/> |Массив **PersistElement** блоки  <br/> |переменная  <br/> |Указывает, сколько записей **PersistElement** для хранилища. В разделе таблицы «PersistElement блок» для формата эту структуру.  <br/> |
   
**PersistBlockType значения**

|**Имя**|**Значение**|**Описание**|
|:-----|:-----|:-----|
|PERSIST_SENTINEL  <br/> |0x0000  <br/> |Указывает, обработки не несколько блоков **PersistData** .  <br/> |
|RSF_PID_RSS_SUBSCRIPTION  <br/> |0x8001  <br/> |Указывает, что этот блок содержит данные для подписки на RSS-канал папки.  <br/> |
|RSF_PID_SEND_AND_TRACK  <br/> |0x8002  <br/> |Указывает, что этот блок содержит данные для папки, отслеживаемых обработки почты.  <br/> |
|RSF_PID_TODO_SEARCH  <br/> |0x8004  <br/> |Указывает, что этот блок содержит данные для папки поиска задачи.  <br/> |
|RSF_PID_CONV_ACTIONS  <br/> |0x8006  <br/> |Указывает, что этот блок содержит данные для папки Настройка действия беседы.  <br/> |
|RSF_PID_COMBINED_ACTIONS  <br/> |0x8007  <br/> |Это значение зарезервировано.  <br/> |
|RSF_PID_SUGGESTED_CONTACTS  <br/> |0x8008  <br/> |Указывает, что этот блок содержит данные для папки предлагаемых контактов.  <br/> |
|RSF_PID_CONTACT_SEARCH  <br/> |0x8009  <br/> |Указывает, что этот блок содержит данные для папки поиска контактов.  <br/> Использовать только с Outlook.  <br/> |
|RSF_PID_BUDDYLIST_PDLS  <br/> |0x800A  <br/> |Указывает, что этот блок содержит данные для папки списки контактов мгновенного обмена Мгновенными сообщениями. Указанной папки содержит личные списки рассылки (PDLs) представляющее каждой группы в списке контактов мгновенных сообщений.  <br/> Используемый Outlook и Exchange.  <br/> |
|RSF_PID_BUDDYLIST_CONTACTS  <br/> |0x800B  <br/> |Указывает, что этот блок содержит данные для папки Контакты обмена мгновенными Сообщениями. Указанной папки содержит отдельные контакты, ссылается групп списка контактов обмена мгновенными Сообщениями.  <br/> Используемый Outlook и Exchange.  <br/> |
   
Если значение **PersistBlockType** не является одним из них, определенный здесь, блока **PersistData** игнорируется и обработка продолжается, пока обрабатывается PERSIST_SENTINEL **PersistID** или достигнут конец потока. 
  
**PersistElementBlock**

|**Имя**|**Тип**|**Size**|**Описание**|
|:-----|:-----|:-----|:-----|
|**Ид_элемента** <br/> |WORD  <br/> |2  <br/> |Указывает значение идентификатора типа для этого блока **PersistElement** . В разделе таблицы «PersistElementType значения» список допустимых значений.  <br/> |
|**ElementDataSize** <br/> |WORD  <br/> |2  <br/> |Указывает размер, в байтах, поля **ElementData** .  <br/> |
|**ElementData** <br/> |массив двоичных данных  <br/> |переменная  <br/> |Содержит данные для этой **PersistID** + **Ид_элемента** пары.  <br/> |
   
**PersistElementType значения**

|**Имя**|**Значение**|**Значение ElementDataSize**|**Описание**|
|:-----|:-----|:-----|:-----|
|RSF_ELID_HEADER  <br/> |0x0002  <br/> |0x0004  <br/> |Указывает, что этот блок **ElementData** поле содержит значение DWORD заголовка. Интерпретация это значение зависит от типа **PersistID** блока.  <br/> Для всех типов **PersistID** , указанных в [[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb.aspx)это значение равно нулю.  <br/> |
|RSF_ELID_ENTRYID  <br/> |0x0001  <br/> |переменная  <br/> |Указывает, что этот блок содержит **EntryID** папки, указанного идентификатором **PersistID**.  <br/> |
|ELEMENT_SENTINEL  <br/> |0x0000  <br/> |0x0000  <br/> |Указывает, обработки не несколько блоков **PersistElement** .  <br/> |
   
Если значение **PersistElementType** не является одним из них, определенный здесь, блока **PersistElement** игнорируется и обработка продолжается, пока обрабатывается ELEMENT_SENTINEL **Ид_элемента** или достигнут конец потока. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSPAM]](http://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Включает обработку списки разрешенных и запрещенных и определение нежелательных сообщений электронной почты.
    
[[MS-OXOSFLD]](http://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
[[MS-OXPHISH]](http://msdn.microsoft.com/library/ed49ab26-ba13-4d4c-8a94-98d4ceecd4b7%28Office.15%29.aspx)
  
> Идентифицирует и помечает сообщения электронной почты, которые предназначены для побудить получателей разглашение конфиденциальной информации (например, пароли и другие личные сведения) чтобы-надежного источника.
    
### <a name="header-files"></a>Файлы заголовков

Mapitags.h
  
> Содержит определения свойств указано, что связанными свойствами.
    
Mapidefs.h
  
> Содержит определения типов данных.
    
## <a name="see-also"></a>См. также



[Обзор свойств MAPI](mapi-property-overview.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

