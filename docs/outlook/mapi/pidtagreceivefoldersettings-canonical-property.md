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
ms.openlocfilehash: c8bd8c7fb2ff5a030cd96e4c3ac2bbb4b6b16ce5
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571460"
---
# <a name="pidtagreceivefoldersettings-canonical-property"></a>Каноническое свойство PidTagReceiveFolderSettings

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Содержит таблицы сообщения магазина принимать параметры папки.
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_RECEIVE_FOLDER_SETTINGS  <br/> |
|Идентификатор:  <br/> |0x3415  <br/> |
|Тип данных:  <br/> |PT_OBJECT  <br/> |
|Область:  <br/> |Хранение сообщений MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Это свойство можно в операциях [IMAPIProp::CopyTo](imapiprop-copyto.md) для включения или исключения в [IMAPIProp::CopyProps](imapiprop-copyprops.md) операции. Как свойство типа PT_OBJECT не может быть отменен успешно с помощью метода [IMAPIProp::GetProps](imapiprop-getprops.md) ; его содержимое должен осуществляться с помощью метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) , запрашивающий интерфейс с идентификатором IID_IMAPITable. Поставщиков услуг должен сообщить о его в метод [IMAPIProp::GetPropList](imapiprop-getproplist.md) если он имеет значение, но при необходимости можно сообщить или не в том случае, если он не установлен. 
  
Чтобы извлечь содержимое таблицы, клиентское приложение следует вызовите метод [IMsgStore::GetReceiveFolderTable](imsgstore-getreceivefoldertable.md) . Для получения дополнительных сведений см [получают папки](receive-folder-tables.md).
  
Это свойство содержит таблицу сопоставления для получения папок для хранения сообщений. Вызов **OpenProperty** на это свойство эквивалентно вызову **GetReceiveFolderTable** хранилища сообщений. 
  
## <a name="related-resources"></a>Связанные ресурсы

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

