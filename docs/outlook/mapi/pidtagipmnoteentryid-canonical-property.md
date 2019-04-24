---
title: Каноническое свойство PidTagIpmNoteEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmNoteEntryId
api_type:
- HeaderDef
ms.assetid: c003f7b9-b0cd-4656-98fa-3466fda6832c
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3d465bfeb30d4f2964254b1d1f524f964fde7239
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32327876"
---
# <a name="pidtagipmnoteentryid-canonical-property"></a>Каноническое свойство PidTagIpmNoteEntryId

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит **EntryID** для папки заметок Outlook. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ИПМ_НОТЕ_ЕНТРИД  <br/> |
|Идентификатор:  <br/> |0x36D3  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство хранится в папке "Входящие", а также в корневой папке хранилища сообщений. Чтобы получить доступ к свойству в определенном хранилище сообщений, выполните следующие действия: 
  
1. Сначала найдите свойство в папке "Входящие". Используйте [IMsgStore:: жетрецеивефолдер](imsgstore-getreceivefolder.md) , чтобы получить ссылку на **EntryID** для папки "Входящие". 
    
2. Если * * IMsgStore:: Жетрецеивефолдер * * является успешным, используйте ссылку на идентификатор **EntryID** папки "Входящие" и [IMsgStore:: OpenEntry](imsgstore-openentry.md) , чтобы открыть папку "Входящие" и получить ссылку на объект **IMAPIFolder** . 
    
3. Если **IMsgStore:: OpenEntry** — успешно, используйте возвращенную ссылку на объект **IMAPIFolder** и [IMAPIProp::](imapiprop-getprops.md) -Props, чтобы получить нужное свойство. 
    
4. Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке. Для этого используйте **IMsgStore:: OpenEntry**, УКАЗАВ значение NULL для **лпентрид**, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** . 
    
5. При успешном открытии корневой папки используйте возвращенную ссылку на объект **IMAPIFolder** и **IMAPIProp::** -Props, чтобы получить нужное свойство. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСОСФЛД]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции для создания и поиска специальных папок в почтовом ящике.
    
[[MS — ОКСОДЛГТ]](https://msdn.microsoft.com/library/01a89b11-9c43-4c40-b147-8f6a1ef5a44f%28Office.15%29.aspx)
  
> Задает методы для подключения и настройки почтовых ящиков в качестве делегатов и взаимодействия с объектами Message и Calendar, когда они действуют от имени другого пользователя.
    
### <a name="header-files"></a>Файлы заГоловков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

