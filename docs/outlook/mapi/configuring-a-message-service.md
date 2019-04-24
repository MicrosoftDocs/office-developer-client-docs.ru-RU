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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335114"
---
# <a name="configuring-a-message-service"></a><span data-ttu-id="8a5d6-103">Настройка службы сообщений</span><span class="sxs-lookup"><span data-stu-id="8a5d6-103">Configuring a Message Service</span></span>

  
  
<span data-ttu-id="8a5d6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a5d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="8a5d6-105">**Настройка всех поставщиков служб в службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="8a5d6-105">**To configure all the service providers in a message service**</span></span>
  
- <span data-ttu-id="8a5d6-106">Call [имсгсервицеадмин:: конфигуремсгсервице](imsgserviceadmin-configuremsgservice.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d6-106">Call [IMsgServiceAdmin::ConfigureMsgService](imsgserviceadmin-configuremsgservice.md).</span></span> <span data-ttu-id="8a5d6-107">Если все данные, необходимые для настройки, доступны программно, вы можете выбрать, следует ли отображать пользовательский интерфейс.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-107">If all of the data necessary for configuration is available programmatically, you can choose whether or not to display a user interface.</span></span> <span data-ttu-id="8a5d6-108">Тем не менее, если некоторые сведения для одного или нескольких поставщиков недоступны, убедитесь, что установлен флаг СЕРВИЦЕ_УИ_АЛЛОВЕД или СЕРВИЦЕ_УИ_АЛВАЙС.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-108">However, if some of the information for one or more providers is not available, make sure that you set the SERVICE_UI_ALLOWED or SERVICE_UI_ALWAYS flag.</span></span> <span data-ttu-id="8a5d6-109">Запрет доступа к пользовательскому интерфейсу при недоступности необходимых данных конфигурации приводит к ненастроенной службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-109">Suppressing a user interface when required configuration data is unavailable results in an unconfigured message service.</span></span>
    
 <span data-ttu-id="8a5d6-110">**Настройка одного поставщика услуг в службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="8a5d6-110">**To configure a single service provider in a message service**</span></span>
  
1. <span data-ttu-id="8a5d6-111">Call [IMAPISession:: жетстатустабле](imapisession-getstatustable.md) для доступа к объекту Status поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-111">Call [IMAPISession::GetStatusTable](imapisession-getstatustable.md) to access the service provider's status object.</span></span> 
    
2. <span data-ttu-id="8a5d6-112">Call [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) для отображения страницы свойств поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="8a5d6-112">Call [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) to display the service provider's property sheet.</span></span> 
    
<span data-ttu-id="8a5d6-113">Дополнительные сведения об использовании объектов Status приведены в статье [Status Table and Status Objects](status-table-and-status-objects.md).</span><span class="sxs-lookup"><span data-stu-id="8a5d6-113">For more information about using status objects, see [Status Table and Status Objects](status-table-and-status-objects.md).</span></span>
  

