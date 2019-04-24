---
title: Каноническое свойство PidTagMessageRecipients
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagMessageRecipients
api_type:
- HeaderDef
ms.assetid: 7f8b0d96-99d6-4f1c-8ac4-4dbb83626382
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d30088ba7398669228a18be825323afa800ec536
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32355687"
---
# <a name="pidtagmessagerecipients-canonical-property"></a>Каноническое свойство PidTagMessageRecipients

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит таблицу ограничений, которые можно применить к таблице содержимого, чтобы найти все сообщения, содержащие вложенные объекты получателей, соответствующие ограничениям. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_МЕССАЖЕ_РЕЦИПИЕНТС  <br/> |
|Идентификатор:  <br/> |0x0E12  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Общий обмен сообщениями  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations. Как свойство типа **пт_обжект**, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) . К его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса **иид_имапитабле** . Поставщики услуг должны сообщить о ней методу [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан. 
  
Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [iMessage:: жетреЦипиенттабле](imessage-getrecipienttable.md) . 
  
Это свойство можно использовать для ограничения подобъекта, указав его в структуре [ссубрестриктион](ssubrestriction.md) . Это позволяет клиенту ограничить представление контейнера сообщениями, получателями которых удовлетворяют заданные условия. Сообщение просматривается в том случае, если в таблице получателей по крайней мере одна строка, то есть один получатель удовлетворяет ограничению этого подобъекта. 
  
 **Note (Примечание** ) Использование результатов ограничения для подобъектов эквивалентно вызову [IMAPISession:: OpenEntry](imapisession-openentry.md) для каждого сообщения в таблице. В зависимости от клиентского приложения и количества сообщений, в которых выполняется поиск, это может повлиять на производительность. 
  
Свойство **пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md)) и это свойство похожи в использовании. Несколько свойств MAPI предоставляют доступ к таблицам: 
  
|**Property**|**Table**|
|:-----|:-----|
|**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Таблица содержимого  <br/> |
|**Пр_контаинер_хиерарчи** ([PidTagContainerHierarchy](pidtagcontainerhierarchy-canonical-property.md))  <br/> |Таблица иерархии  <br/> |
|**Пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Связанная таблица содержимого  <br/> |
|**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Таблица вложений  <br/> |
|ПР_МЕССАЖЕ_РЕЦИПИЕНТС  <br/> |Таблица получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
[[MS — ОКСКСПАМ]](https://msdn.microsoft.com/library/522f8587-4aed-4cd6-831b-40bd87862189%28Office.15%29.aspx)
  
> Разрешает обработку списков разрешений и блокировок, а также определение нежелательных сообщений электронной почты.
    
[[MS — ОКСТНЕФ]](https://msdn.microsoft.com/library/1f0544d7-30b7-4194-b58f-adc82f3763bb%28Office.15%29.aspx)
  
> Кодирует и декодирует объекты сообщений и вложений в эффективное потоковое представление.
    
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

