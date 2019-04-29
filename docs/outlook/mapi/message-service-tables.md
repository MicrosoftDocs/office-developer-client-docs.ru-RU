---
title: Таблицы службы сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c644e89511033234aa45c5f82738e4c471ef646d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422497"
---
# <a name="message-service-tables"></a>Таблицы службы сообщений

  
  
**Относится к**: Outlook 2013 | Outlook 2016 
  
Таблица служба сообщений содержит сведения о службах сообщений в текущем профиле. Для каждого сеанса MAPI существует одна таблица службы сообщений, реализованная MAPI и используемая клиентскими приложениями специального назначения, которые обеспечивают поддержку конфигурации. 
  
Таблица службы сообщений — это статическая таблица.
  
Клиенты получают доступ к таблице службы сообщений, вызывая метод [имсгсервицеадмин:: жетмсгсервицетабле](imsgserviceadmin-getmsgservicetable.md) . 
  
Следующие свойства составляют обязательный набор столбцов в таблице службы сообщений:
  
|||
|:-----|:-----|
|**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**Пр_ресаурце_флагс** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**Пр_сервице_длл_наме** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**Пр_сервице_ентри_наме** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**Пр_сервице_наме** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**Пр_сервице_суппорт_филес** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**Пр_сервице_уид** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **Пр_дисплай_наме** — отображаемое имя для службы сообщений и столбец ключа сортировки по умолчанию. 
  
 **Пр_инстанце_кэй** служит в качестве столбца индекса для таблицы, уникально определяющий строку. 
  
 **Пр_ресаурце_флагс** описывает возможности службы сообщений. 
  
 **Пр_сервице_длл_наме** это имя библиотеки DLL, которая содержит реализацию службы сообщений. 
  
 **Пр_сервице_ентри_наме** — это имя функции точки входа службы сообщений, которая соответствует прототипу [мсгсервицеентри](msgserviceentry.md) . 
  
 **Пр_сервице_наме** — обязательная запись в разделе **[Services]** in Mapisvc. INF. Значение этого свойства никогда не будет изменено или локализовано. **Пр_сервице_наме** можно использовать для программного определения службы сообщений. 
  
 **Пр_сервице_суппорт_филес** — это список файлов, которые необходимо установить вместе со службой сообщений. 
  
 **Пр_сервице_уид** — это уникальный идентификатор службы сообщений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

