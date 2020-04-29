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
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** — отображаемое имя для службы сообщений и столбец ключа сортировки по умолчанию. 
  
 **PR_INSTANCE_KEY** выступает в качестве столбца индекса для таблицы, уникальным образом идентифицирующего строку. 
  
 **PR_RESOURCE_FLAGS** рассказывается о возможностях службы сообщений. 
  
 **PR_SERVICE_DLL_NAME** — это имя библиотеки DLL, которая содержит реализацию службы сообщений. 
  
 **PR_SERVICE_ENTRY_NAME** — это имя функции точки входа службы сообщений, которая соответствует прототипу [мсгсервицеентри](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** является обязательной записью в разделе **[Services]** in Mapisvc. INF. Значение этого свойства никогда не будет изменено или локализовано. **PR_SERVICE_NAME** можно использовать для программного определения службы сообщений. 
  
 **PR_SERVICE_SUPPORT_FILES** — это список файлов, которые необходимо установить вместе со службой сообщений. 
  
 **PR_SERVICE_UID** — это уникальный идентификатор службы сообщений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

