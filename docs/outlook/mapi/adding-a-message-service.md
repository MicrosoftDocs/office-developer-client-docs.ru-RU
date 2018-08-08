---
title: Добавление службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 1e626714-52dc-4141-9741-4d801f32d294
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a7735be5cfb8ff0716b6bd6eba4951563bb938ab
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808003"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="f22c5-103">Добавление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="f22c5-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="f22c5-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f22c5-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="f22c5-105">**Добавление новой службы сообщений в профиль и доступ к новой службы сообщений**</span><span class="sxs-lookup"><span data-stu-id="f22c5-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="f22c5-106">Вызов [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="f22c5-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="f22c5-107">**CreateMsgServiceEx** выполняет следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="f22c5-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="f22c5-108">Копирует все соответствующие сведения для службы сообщений, которая находится в файл Mapisvc.inf. INF-файл, создание раздела профиля для каждого раздела поставщика.</span><span class="sxs-lookup"><span data-stu-id="f22c5-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="f22c5-109">Вызывает функцию точки входа для службы сообщений, **MSGSERVICEENTRY**с параметром _ulContext_ , равным MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="f22c5-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="f22c5-110">Задает и получает свойство **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f22c5-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="f22c5-111">**Для доступа к службе любого добавленного сообщения**</span><span class="sxs-lookup"><span data-stu-id="f22c5-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="f22c5-112">Вызов [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) для получения таблицы службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f22c5-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="f22c5-113">Вызов метода [IMAPITable::Advise](imapitable-advise.md) таблицы службы сообщений для регистрации уведомлений в таблице.</span><span class="sxs-lookup"><span data-stu-id="f22c5-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="f22c5-114">Когда MAPI отправляет уведомление TABLE_ROW_ADDED, найдите идентификатор записи службы новые сообщения в структуре [SRow](srow.md) в структуре [TABLE_NOTIFICATION](table_notification.md) .</span><span class="sxs-lookup"><span data-stu-id="f22c5-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

