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
ms.openlocfilehash: fd87d169cd5131c6e1c8ca45a35dded96a295c57
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808172"
---
# <a name="configuring-a-message-service"></a>Настройка службы сообщений

  
  
**Относится к**: Outlook 
  
 **Для настройки всех поставщиков услуг службы сообщений**
  
- Вызов [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md). Если все данные, необходимые для настройки программным способом, можно ли пользовательского интерфейса. Тем не менее если некоторые сведения для одного или нескольких поставщиков недоступна, убедитесь в том, что значение флага SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS. Запрет пользовательского интерфейса, когда данные требуемой конфигурации недоступен результаты в службе не настроенные сообщения.
    
 **Чтобы настроить отдельный поставщик услуг службы сообщений**
  
1. Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к объекту состояние поставщика услуг. 
    
2. Вызовите [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , чтобы открыть окно свойств поставщика услуг. 
    
Дополнительные сведения об использовании объектов состояния см в [таблице состояния и состояния объектов](status-table-and-status-objects.md).
  

