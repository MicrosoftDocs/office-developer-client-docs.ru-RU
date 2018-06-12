---
title: Таблицы службы сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: b93ab837-3918-4427-b013-bedc6f5276e4
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: 81772115fcd4f081718dd560759f6ab93dc7c11c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810029"
---
# <a name="message-service-tables"></a>Таблицы службы сообщений

  
  
**Применимо к**: Outlook 
  
Таблица службы сообщение содержит сведения о службах сообщения текущего профиля. Для каждого сеанса MAPI, реализованный MAPI и используется особого назначения клиентских приложений, которые обеспечивают поддержку конфигурации имеется одна таблица службы сообщений. 
  
В таблице службы сообщений — это статическая таблица.
  
Для доступа клиентов к таблице службы сообщения путем вызова метода [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) . 
  
Следующие свойства составляют обязательный столбец, задайте в таблице служб сообщения:
  
|||
|:-----|:-----|
|**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))  <br/> |**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md))  <br/> |
|**PR_RESOURCE_FLAGS** ([PidTagResourceFlags](pidtagresourceflags-canonical-property.md))  <br/> |**PR_SERVICE_DLL_NAME** ([PidTagServiceDllName](pidtagservicedllname-canonical-property.md))  <br/> |
|**PR_SERVICE_ENTRY_NAME** ([PidTagServiceEntryName](pidtagserviceentryname-canonical-property.md))  <br/> |**PR_SERVICE_NAME** ([PidTagServiceName](pidtagservicename-canonical-property.md))  <br/> |
|**PR_SERVICE_SUPPORT_FILES** ([PidTagServiceSupportFiles](pidtagservicesupportfiles-canonical-property.md))  <br/> |**PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md))  <br/> |
   
 **PR_DISPLAY_NAME** — отображаемое имя для службы сообщений и столбце ключа сортировки по умолчанию. 
  
 **PR_INSTANCE_KEY** выступает в качестве столбца индекса для таблицы, уникально идентифицирующий строку. 
  
 **PR_RESOURCE_FLAGS** : описание возможностей службы сообщений. 
  
 **PR_SERVICE_DLL_NAME** — это имя библиотеки DLL, которая содержит реализации службы сообщений. 
  
 **PR_SERVICE_ENTRY_NAME** — это имя функции точки входа службы сообщений, который соответствует прототип [MSGSERVICEENTRY](msgserviceentry.md) . 
  
 **PR_SERVICE_NAME** является обязательным параметром в разделе **[Services]** в MAPISVC.INF. Значение для этого свойства никогда не будет изменен или локализованное. **PR_SERVICE_NAME** можно использовать для идентификации службы сообщений программными средствами. 
  
 **PR_SERVICE_SUPPORT_FILES** — это список файлов, которые должны быть установлены с помощью службы сообщений. 
  
 **PR_SERVICE_UID** — уникальный идентификатор для службы сообщений. 
  
## <a name="see-also"></a>См. также



[Таблицы MAPI](mapi-tables.md)

