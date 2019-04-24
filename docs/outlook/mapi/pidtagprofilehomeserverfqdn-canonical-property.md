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
ms.openlocfilehash: aef4a932da35f3c4955bc2f4b265b146775c6d87
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32341596"
---
# <a name="pidtagprofilehomeserverfqdn-canonical-property"></a>Каноническое свойство PidTagProfileHomeServerFQDN

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
Включает проверку подлинности Kerberos для конфигурации профиля.
  
****

|||
|:-----|:-----|
|Связанные свойства:  <br/> |ПР_ПРОФИЛЕ_ХОМЕ_СЕРВЕР_ФКДН  <br/> |
|Идентификатор:  <br/> |0x662A001F  <br/> |
|Тип данных:  <br/> |PT_UNICODE  <br/> |
|Область:  <br/> |Конфигурация профиля MAPI  <br/> |
   
## <a name="remarks"></a>Комментарии

Задание этого свойства для доменного имени сервера каталогов пользователя позволяет напрямую подключиться к контроллеру домена (DC), который необходим для профиля, настроенного для использования проверки подлинности Kerberos в Microsoft Exchange Server 2007 и более ранние версии, устанавливая **рпк_к_аусн_гсс_керберос** в **пр_профиле_аус_паккаже**.
  
> [!NOTE]
> Microsoft Exchange Server 2010 и Exchange Server 2013 обрабатывают вызовы адресных книг, выполняемые на сервере клиентского доступа, так же, как Exchange Server 2007 и более ранние версии обрабатывают их. Процесс DSProxy больше не используется, поэтому проверка подлинности Kerberos может быть успешной. Однако клиент по-прежнему будет взаимодействовать с сервером Exchange Server, а не с КОНТРОЛЛЕРом домена, что может быть нежелательным. **** 
  
## <a name="related-resources"></a>Связанные ресурсы

### <a name="protocol-specifications"></a>Спецификации протокола

[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)
  
> Содержит ссылки на соответствующие спецификации протоколов Exchange Server.
    
[[MS — ОКСКСТОР]](https://msdn.microsoft.com/library/d42ed1e0-3e77-4264-bd59-7afc583510e2%28Office.15%29.aspx)
  
> Указывает допустимые операции для основных объектов хранилища сообщений.
    
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

