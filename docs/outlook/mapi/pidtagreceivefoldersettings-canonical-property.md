---
title: Каноническое свойство PidTagReceiveFolderSettings
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagReceiveFolderSettings
api_type:
- COM
ms.assetid: 2f0b1679-05b0-4580-b6d2-474fe3f9d012
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 8590e357252089aaa49a71d443037b9b9ed77ee4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415056"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Каноническое свойство PidTagReceiveFolderSettings

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу параметров получения папки для хранилища сообщений.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Идентификатор:  <br/> |0x3415  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Хранилище сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations. Как свойство типа PT_OBJECT, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) GetProperty. к его содержимому должен обращаться метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , который запрашивает интерфейс с идентификатором IID_IMAPITable. Поставщики услуг должны сообщить об этом в метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан. 
  
Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [IMsgStore:: жетрецеивефолдертабле](imsgstore-getreceivefoldertable.md) . Дополнительные сведения [см.](receive-folder-tables.md)
  
Это свойство содержит таблицу сопоставлений папок получения для хранилища сообщений. Вызов **опенпроперти** для этого свойства эквивалентен вызову **жетрецеивефолдертабле** в хранилище сообщений. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="header-files"></a>Файлы заголовков

MAPIDEFS. h
  
> Содержит определения типов данных.
    
Мапитагс. h
  
> Содержит определения свойств, перечисленных как альтернативные имена.
    
## <a name="see-also"></a>См. также



[Свойства MAPI](mapi-properties.md)
  
[Каноническое свойство MAPI](mapi-canonical-properties.md)
  
[Сопоставление имен канонических свойств с именами MAPI](mapping-canonical-property-names-to-mapi-names.md)
  
[Сопоставление имен MAPI с именами канонических свойств](mapping-mapi-names-to-canonical-property-names.md)

