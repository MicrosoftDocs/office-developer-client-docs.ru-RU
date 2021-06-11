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
ms.openlocfilehash: 4c3d30c7111e7b26886cbfb069ec2822d2ee0234
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33434510"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="e84cd-103">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="e84cd-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="e84cd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e84cd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="e84cd-105">**Настройка всех поставщиков услуг в службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="e84cd-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="e84cd-106">Вызов [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="e84cd-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="e84cd-107">Если все данные, необходимые для настройки, доступны программным образом, вы можете выбрать, следует ли отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="e84cd-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="e84cd-108">Однако, если некоторые сведения для одного или нескольких поставщиков недоступны, убедитесь, что вы установите флаг SERVICE_UI_ALLOWED или SERVICE_UI_ALWAYS.</span><span class="sxs-lookup"><span data-stu-id="e84cd-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="e84cd-109">Подавление пользовательского интерфейса при недоступности необходимых данных конфигурации приводит к неконфигурации службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e84cd-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="e84cd-110">**Настройка единого поставщика услуг в службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="e84cd-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="e84cd-111">Вызов [IMAPISession::GetStatusTable,](imapisession-getstatustable.md) чтобы получить доступ к объекту состояния поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e84cd-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="e84cd-112">Вызов [IMAPIStatus::SettingsDialog,](imapistatus-settingsdialog.md) чтобы отобразить лист свойств поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="e84cd-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="e84cd-113">Дополнительные сведения об использовании объектов состояния см. в [таблице status Table и Status Objects.](status-table-and-status-objects.md)</span><span class="sxs-lookup"><span data-stu-id="e84cd-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

