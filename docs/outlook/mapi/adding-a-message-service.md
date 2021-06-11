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
ms.openlocfilehash: 30cbe49eae7b4a232efb544c7a508a36b326c6b5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33407237"
---
# <a name="adding-a-message-service"></a><span data-ttu-id="7c03f-103">Добавление службы сообщений</span><span class="sxs-lookup"><span data-stu-id="7c03f-103">Adding a Message Service</span></span>

  
  
<span data-ttu-id="7c03f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c03f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="7c03f-105">**Добавление новой службы сообщений в профиль и доступ к новой службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="7c03f-105">**To add a new message service to a profile and access the new message service**</span></span>
  
<span data-ttu-id="7c03f-106">Вызов [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span><span class="sxs-lookup"><span data-stu-id="7c03f-106">Call [IMsgServiceAdmin2::CreateMsgServiceEx](imsgserviceadmin2-createmsgserviceex.md).</span></span> <span data-ttu-id="7c03f-107">**CreateMsgServiceEx выполняет** следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="7c03f-107">**CreateMsgServiceEx** performs the following tasks:</span></span> 
  
1. <span data-ttu-id="7c03f-108">Копирует всю соответствующую информацию для службы сообщений, которая находится в MAPISVC. Файл INF, создав раздел профилей для каждого раздела поставщика.</span><span class="sxs-lookup"><span data-stu-id="7c03f-108">Copies all of the relevant information for the message service that is in the MAPISVC.INF file, creating a profile section for every provider section.</span></span>
    
2. <span data-ttu-id="7c03f-109">Вызывает функцию точки входа службы сообщений **MSGSERVICEENTRY** с параметром  _ulContext,_ заданным MSG_SERVICE_CREATE.</span><span class="sxs-lookup"><span data-stu-id="7c03f-109">Calls the message service's entry point function, **MSGSERVICEENTRY**, with the  _ulContext_ parameter set to MSG_SERVICE_CREATE.</span></span> 
    
3. <span data-ttu-id="7c03f-110">Задает и извлекает свойство PR_SERVICE_UID **службы** сообщений [(PidTagServiceUid).](pidtagserviceuid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="7c03f-110">Sets and retrieves the message service's **PR_SERVICE_UID** ([PidTagServiceUid](pidtagserviceuid-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="7c03f-111">**Доступ к новой службе сообщений**</span><span class="sxs-lookup"><span data-stu-id="7c03f-111">**To access any newly added message service**</span></span>
  
1. <span data-ttu-id="7c03f-112">Позвоните [в службу IMsgServiceAdmin::GetMsgServiceTable,](imsgserviceadmin-getmsgservicetable.md) чтобы получить таблицу службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7c03f-112">Call [IMsgServiceAdmin::GetMsgServiceTable](imsgserviceadmin-getmsgservicetable.md) to retrieve the message service table.</span></span> 
    
2. <span data-ttu-id="7c03f-113">Вызов метода [IMAPITable::Advise](imapitable-advise.md) таблицы службы сообщений для регистрации уведомлений таблицы.</span><span class="sxs-lookup"><span data-stu-id="7c03f-113">Call the message service table's [IMAPITable::Advise](imapitable-advise.md) method to register for table notifications.</span></span> 
    
3. <span data-ttu-id="7c03f-114">При отправке уведомления TABLE_ROW_ADDED MAPI найдите идентификатор записи недавно добавленной службы сообщений в структуре [SRow,](srow.md) [включенной в структуру TABLE_NOTIFICATION.](table_notification.md)</span><span class="sxs-lookup"><span data-stu-id="7c03f-114">When MAPI sends a TABLE_ROW_ADDED notification, locate the entry identifier of the newly added message service in the [SRow](srow.md) structure included in the [TABLE_NOTIFICATION](table_notification.md) structure.</span></span> 
    

