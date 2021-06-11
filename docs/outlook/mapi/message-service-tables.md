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

  
  
**Область применения**: Outlook 2013 | Outlook 2016 
  
В таблице службы сообщений содержатся сведения о службах сообщений в текущем профиле. Существует одна таблица службы сообщений для каждого сеанса MAPI, реализованного MAPI и используемого клиентских приложений специального назначения, которые обеспечивают поддержку конфигурации. 
  
Таблица службы сообщений — это статическая таблица.
  
Клиенты получают доступ к таблице службы сообщений, позвонив по [методу IMsgServiceAdmin::GetMsgServiceTable.](imsgserviceadmin-getmsgservicetable.md) 
  
Следующие свойства составляют необходимый столбец в таблице службы сообщений:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)  <br/> |**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)  <br/> |
|**PR_RESOURCE_FLAGS** [(PidTagResourceFlags)](pidtagresourceflags-canonical-property.md)  <br/> |**PR_SERVICE_DLL_NAME** [(PidTagServiceDllName)](pidtagservicedllname-canonical-property.md)  <br/> |
|**PR_SERVICE_ENTRY_NAME** [(PidTagServiceEntryName)](pidtagserviceentryname-canonical-property.md)  <br/> |**PR_SERVICE_NAME** [(PidTagServiceName)](pidtagservicename-canonical-property.md)  <br/> |
|**PR_SERVICE_SUPPORT_FILES** [(PidTagServiceSupportFiles)](pidtagservicesupportfiles-canonical-property.md)  <br/> |**PR_SERVICE_UID** [(PidTagServiceUid)](pidtagserviceuid-canonical-property.md)  <br/> |
   
 **PR_DISPLAY_NAME** является отображаемым именем службы сообщений и столбца ключа сортировки по умолчанию. 
  
 **PR_INSTANCE_KEY** в качестве столбца индекса для таблицы, уникально идентифицируя строку. 
  
 **PR_RESOURCE_FLAGS** описывает возможности службы сообщений. 
  
 **PR_SERVICE_DLL_NAME** это имя DLL, которое содержит реализацию службы сообщений. 
  
 **PR_SERVICE_ENTRY_NAME** является именем функции точки входа службы сообщений, соответствующей прототипу [MSGSERVICEENTRY.](msgserviceentry.md) 
  
 **PR_SERVICE_NAME** является обязательной записью в **разделе [Services]** в MAPISVC.INF. Значение этого свойства никогда не будет изменено или локализовано. **PR_SERVICE_NAME** можно использовать для программного определения службы сообщений. 
  
 **PR_SERVICE_SUPPORT_FILES** список файлов, которые необходимо установить в службе сообщений. 
  
 **PR_SERVICE_UID** является уникальным идентификатором для службы сообщений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

