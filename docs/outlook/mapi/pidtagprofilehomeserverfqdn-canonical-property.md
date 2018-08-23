---
title: Каноническое свойство PidTagProfileHomeServerFQDN
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 80273b50-bc16-4be2-8471-1a127b6786bb
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b02a55f7b87bef6a4304d006f79472bcf21c811e
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581876"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Каноническое свойство PidTagProfileHomeServerFQDN

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
Включение проверки подлинности Kerberos для настройки профилей.
  
****

|||
|:-----|:-----|
|Связанные свойства:  <br/> |PR_PROFILE_HOME_SERVER_FQDN  <br/> |
|Идентификатор:  <br/> |0x662A001F  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Настройки профилей MAPI  <br/> |
   
## <a name="remarks"></a>Замечания

Установка для этого свойства доменное имя сервера каталогов пользователя позволяет прямое подключение к домена Контроллера, который требуется для профиля, который был настроен для использования проверки подлинности Kerberos с Microsoft Exchange Server 2007 и более ранних версий, задав **RPC_C_AUTHN_GSS_KERBEROS** в **PR_PROFILE_AUTH_PACKAGE**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 и Exchange Server 2013 обрабатывать адресной книги вызовах на сервер клиентского доступа по-разному от того, в котором сервер Exchange Server 2007 и более ранних версий их обработки. Процесс DSProxy больше не используется, поэтому может завершиться без ошибок проверки подлинности Kerberos. Тем не менее, клиент будет по-прежнему связи с Exchange server, а не непосредственно с контроллера домена, который не может потребоваться: параметр позволяет избежать **PR_PROFILE_HOME_SERVER_FQDN** это. 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на связанные спецификаций протокола Exchange Server.
    
[[MS-OXCSTOR]](http://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для базовых объектов хранилища сообщений.
    
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

