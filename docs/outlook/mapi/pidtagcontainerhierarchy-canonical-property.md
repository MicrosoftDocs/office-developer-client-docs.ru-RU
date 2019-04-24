---
title: Каноническое свойство PidTagContainerHierarchy
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagContainerHierarchy
api_type:
- HeaderDef
ms.assetid: 6917510d-ca1e-4049-9eab-09313753ecf0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: f009d7ce5cd1856ccff1e00953188c8edde7a6bc
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332860"
---
# <a name="pidtagcontainerhierarchy-canonical-property"></a>Каноническое свойство PidTagContainerHierarchy

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит внедренный объект таблицы иерархий, предоставляющий сведения о дочерних контейнерах. 
  
|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_КОНТАИНЕР_ХИЕРАРЧИ  <br/> |
|Идентификатор:  <br/> |0x360E  <br/> |
|Тип данных:  <br/> |ПТ_ОБЖЕКТ  <br/> |
|Область:  <br/> |Container  <br/> |
   
## <a name="remarks"></a>Комментарии

Это свойство можно исключить в [IMAPIProp:: операции CopyTo](imapiprop-copyto.md) или включено в [IMAPIProp:: копипропс](imapiprop-copyprops.md) Operations. Как свойство типа **пт_обжект**, оно не может быть успешно получено методом [IMAPIProp::](imapiprop-getprops.md) ; к его содержимому должен получать доступ метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) , запрашивающий идентификатор интерфейса иид_имапитабле. Поставщики услуг должны сообщить об этом в метод [IMAPIProp:: жетпроплист](imapiprop-getproplist.md) , если он задан, но при необходимости можно сообщить ему, если он не задан. 
  
Чтобы получить содержимое таблицы, клиентское приложение должно вызвать метод [IMAPIContainer:: жесиерарчитабле](imapicontainer-gethierarchytable.md) . Более подробную информацию можно [](hierarchy-tables.md)узнать в статье иерархия Tables. 
  
 **Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md)), **пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md)), и это свойство аналогично в использовании. Несколько свойств MAPI предоставляют доступ к таблицам: 
  
|**Property**|**Table**|
|:-----|:-----|
|**Пр_контаинер_контентс** ([PidTagContainerContents](pidtagcontainercontents-canonical-property.md))  <br/> |Таблица содержимого  <br/> |
|**ПР_КОНТАИНЕР_ХИЕРАРЧИ** <br/> |Таблица иерархии  <br/> |
|**Пр_фолдер_ассоЦиатед_контентс** ([PidTagFolderAssociatedContents](pidtagfolderassociatedcontents-canonical-property.md))  <br/> |Связанная таблица содержимого  <br/> |
|**Пр_мессаже_аттачментс** ([PidTagMessageAttachments](pidtagmessageattachments-canonical-property.md))  <br/> |Таблица вложений  <br/> |
|**Пр_мессаже_реЦипиентс** ([PidTagMessageRecipients](pidtagmessagerecipients-canonical-property.md))  <br/> |Таблица получателей  <br/> |
   
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКФКСИКС]](https://msdn.microsoft.com/library/b9752f3d-d50d-44b8-9e6b-608a117c8532%28Office.15%29.aspx)
  
> Обрабатывает порядок и потоки для передачи данных между клиентом и сервером.
    
[[MS — ОКСЦИКАЛ]](https://msdn.microsoft.com/library/a685a040-5b69-4c84-b084-795113fb4012%28Office.15%29.aspx)
  
> Преобразование между IETF RFC2445, RFC2446 и RFC2447, а объекты встреч и собраний.
    
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

