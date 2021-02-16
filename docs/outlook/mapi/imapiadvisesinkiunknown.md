---
title: IMAPIAdviseSink IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIAdviseSink
api_type:
- COM
ms.assetid: f598fc57-75d3-473b-8eb0-9d8a3b92e9f2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: d537184f427b2ef240dd2a9a59ab2f624f8f75d0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409568"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="8dc3e-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8dc3e-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="8dc3e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8dc3e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8dc3e-105">Реализует объект-замещение для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="8dc3e-106">Указатель на объект приемника рекомендации передается в вызове метода **Advise** поставщика услуг, механизма, используемого для регистрации для уведомления.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="8dc3e-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-107">Header file:</span></span>  <br/> |<span data-ttu-id="8dc3e-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="8dc3e-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="8dc3e-109">Выставим:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="8dc3e-110">Рекомендуемые объекты-висяки</span><span class="sxs-lookup"><span data-stu-id="8dc3e-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="8dc3e-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="8dc3e-112">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="8dc3e-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="8dc3e-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-113">Called by:</span></span>  <br/> |<span data-ttu-id="8dc3e-114">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="8dc3e-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="8dc3e-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="8dc3e-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="8dc3e-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="8dc3e-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="8dc3e-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="8dc3e-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="8dc3e-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="8dc3e-119">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="8dc3e-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="8dc3e-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="8dc3e-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="8dc3e-121">Отвечает на уведомление, выполняя одну или несколько задач.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="8dc3e-122">Выполняемые задачи зависят от типа события и объекта, который создает уведомление.</span><span class="sxs-lookup"><span data-stu-id="8dc3e-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8dc3e-123">См. также</span><span class="sxs-lookup"><span data-stu-id="8dc3e-123">See also</span></span>



[<span data-ttu-id="8dc3e-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="8dc3e-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

