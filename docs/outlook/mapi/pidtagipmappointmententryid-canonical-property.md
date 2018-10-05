---
title: Каноническое свойство PidTagIpmAppointmentEntryId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagIpmAppointmentEntryId
api_type:
- HeaderDef
ms.assetid: a6e8c8fb-b76a-4a73-b112-6399e4d94233
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d27506edf6eb40f6b244733336b8b381ea941442
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384761"
---
# <a name="pidtagipmappointmententryid-canonical-property"></a>Каноническое свойство PidTagIpmAppointmentEntryId

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит **идентификатор записи** папки календаря Outlook. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_IPM_APPOINTMENT_ENTRYID  <br/> |
|Идентификатор:  <br/> |0x36D0  <br/> |
|Тип данных:  <br/> |PT_BINARY  <br/> |
|Область:  <br/> |Folder  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство хранится в папке "Входящие" и в корневую папку хранилища сообщений. Доступ к свойству для хранилища определенное сообщение, выполните следующие действия. 
  
1. Во-первых найдите свойство в папке "Входящие". Используйте [IMsgStore::GetReceiveFolder](imsgstore-getreceivefolder.md) для получения ссылки на **Код записи** для папки "Входящие". 
    
2. Если **IMsgStore::GetReceiveFolder** выполнена успешно, используйте ссылку на файл **EntryID** для папки "Входящие" и [IMsgStore::OpenEntry](imsgstore-openentry.md) для открытия папки «Входящие» и получить ссылку на объект **IMAPIFolder** . 
    
3. Если **IMsgStore::OpenEntry** выполнена успешно, затем используйте возвращенный ссылку на объект **IMAPIFolder** и [IMAPIProp::GetProps](imapiprop-getprops.md) для получения нужное свойство. 
    
4. Если не удается выполнить шаг 1, 2 или 3, найдите свойство в корневой папке. Для этого используйте **IMsgStore::OpenEntry**, указание NULL для **lpEntryID**, чтобы открыть корневую папку хранилища сообщений и получить ссылку на объект **IMAPIFolder** . 
    
5. При успешном открытии в корневой папке затем используйте возвращенный ссылку на объект **IMAPIFolder** и **IMAPIProp::GetProps** для получения нужное свойство. 
    
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXOSFLD]](https://msdn.microsoft.com/library/a60e9c16-2ba8-424b-b60c-385a8a2837cb%28Office.15%29.aspx)
  
> Задает свойства и операции по созданию и поиск специальные папки в почтовом ящике.
    
### <a name="header-files"></a>Файлы заголовков

Mapidefs.h
  
> Содержит определения типов данных.
    
Mapitags.h
  
> Содержит определения свойства в списке альтернативных имен.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойства MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

