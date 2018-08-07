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
# <a name="configuring-a-message-service"></a><span data-ttu-id="7745c-103">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="7745c-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="7745c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7745c-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="7745c-105">**Для настройки всех поставщиков услуг службы сообщений**</span><span class="sxs-lookup"><span data-stu-id="7745c-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="7745c-106">Вызов [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="7745c-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="7745c-107">Если все данные, необходимые для настройки программным способом, можно ли пользовательского интерфейса.</span><span class="sxs-lookup"><span data-stu-id="7745c-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="7745c-108">Тем не менее если некоторые сведения для одного или нескольких поставщиков недоступна, убедитесь в том, что значение флага SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="7745c-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="7745c-109">Запрет пользовательского интерфейса, когда данные требуемой конфигурации недоступен результаты в службе не настроенные сообщения.</span><span class="sxs-lookup"><span data-stu-id="7745c-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="7745c-110">**Чтобы настроить отдельный поставщик услуг службы сообщений**</span><span class="sxs-lookup"><span data-stu-id="7745c-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="7745c-111">Вызов [IMAPISession::GetStatusTable](imapisession-getstatustable.md) для доступа к объекту состояние поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="7745c-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="7745c-112">Вызовите [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) , чтобы открыть окно свойств поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="7745c-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="7745c-113">Дополнительные сведения об использовании объектов состояния см в [таблице состояния и состояния объектов](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="7745c-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

