---
title: Настройка службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: d68892e3-7c87-4b3a-a691-bff92f83ed00
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2b170037bc51a7848154c12acbfe700a0142ef8f
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564110"
---
# <a name="configuring-a-message-service"></a>Настройка службы сообщений

  
  
**Применимо к**: Outlook 2013 | Outlook 2016 
  
 **Для настройки всех поставщиков услуг службы сообщений**
  
- Вызов [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Если все данные, необходимые для настройки программным способом, можно ли пользовательского интерфейса. Тем не менее если некоторые сведения для одного или нескольких поставщиков недоступна, убедитесь в том, что значение флага SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS. Запрет пользовательского интерфейса, когда данные требуемой конфигурации недоступен результаты в службе не настроенные сообщения.
    
 **Чтобы настроить отдельный поставщик услуг службы сообщений**
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к объекту состояние поставщика услуг. 
    
2. Вызовите [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , чтобы открыть окно свойств поставщика услуг. 
    
Дополнительные сведения об использовании объектов состояния см в [таблице состояния и состояния объектов](status-table-and-status-objects.md).
  

