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
  
Таблица службы сообщений содержит сведения о службах сообщений в текущем профиле. Существует одна таблица службы сообщений для каждого сеанса MAPI, реализованная с помощью MAPI и используемая клиентских приложений специального назначения, которые обеспечивают поддержку конфигурации. 
  
Таблица службы сообщений является статической.
  
Клиенты получают доступ к таблице службы сообщений, вызывая метод [IMsgServiceAdmin::GetMsgServiceTable.](imsgserviceadmin-getmsgservicetable.md) 
  
Следующие свойства составляют необходимый набор столбцов в таблице службы сообщений:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles)](pidtagservicesupportfiles-canonical-property.md)  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid)](pidtagserviceuid-canonical-property.md)  <br/> |
   
 **PR_DISPLAY_NAME** это отображаемое имя службы сообщений и столбец ключа сортировки по умолчанию. 
  
 **PR_INSTANCE_KEY** в качестве столбца индекса для таблицы, уникально идентифицируя строку. 
  
 **PR_RESOURCE_FLAGS** описание возможностей службы сообщений. 
  
 **PR_SERVICE_DLL_NAME** имя DLL- и содержит реализацию службы сообщений. 
  
 **PR_SERVICE_ENTRY_NAME** имя функции точки входа службы сообщений, которая соответствует [прототипу MSGSERVICEENTRY.](msgserviceentry.md) 
  
 **PR_SERVICE_NAME** является обязательной записью в разделе **[Службы]** в MAPISVC.INF. Значение этого свойства никогда не будет изменено или локализовано. **PR_SERVICE_NAME** можно использовать для определения службы сообщений программным путем. 
  
 **PR_SERVICE_SUPPORT_FILES** список файлов, которые необходимо установить вместе со службой сообщений. 
  
 **PR_SERVICE_UID** это уникальный идентификатор службы сообщений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

