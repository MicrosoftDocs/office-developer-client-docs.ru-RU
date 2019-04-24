---
title: Каноническое свойство PidTagSearchRecipientEmailBcc
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: d9561d13-8d52-500c-5369-15a2cf5c92c3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 5b0db4b3bc7903aae74fa7275d3e27e22d628514
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32359159"
---
# <a name="pidtagsearchrecipientemailbcc-canonical-property"></a>Каноническое свойство PidTagSearchRecipientEmailBcc

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Содержит строку Юникода, которая запрашивается в списке адресов электронной почты или отображает имена получателей, указанных в строке **"СК"** неотправленных сообщений в магазине. 
  
## 

|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_СЕАРЧ_РЕЦИП_ЕМАИЛ_БКК_В  <br/> |
|Идентификатор:  <br/> |0x0EA8  <br/> |
|Тип свойства:  <br/> |PT_UNICODE  <br/> |
|Обращения  <br/> |Поиск  <br/> |
   
## <a name="remarks"></a>Примечания

Это свойство относится только к сообщениям в хранилище, которые не были отправлены, так как отправленные и полученные сообщения не содержат сведений о СКРЫТой копии.
  
> [!NOTE]
> Этот тег ограничения MAPI используется при поиске адресов электронной почты или отображаемых имен, в которые сообщение будет отправлено в виде скрытой копии, может не быть определено в файле заголовков, которые есть у вас в данный момент. Вы можете добавить его в код с помощью следующего значения: _Гт_`#define PR_SEARCH_RECIP_EMAIL_BCC_W PROP_TAG(PT_UNICODE, 0x0EA8)`
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Microsoft Exchange Server.
    
[[MS — ОКСОСРЧ]](https://msdn.microsoft.com/library/c72e49b8-78c7-4483-ad65-e46e9133673b%28Office.15%29.aspx)
  
> Задает свойства и операции для управления конфигурацией списка папок поиска.
    
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

