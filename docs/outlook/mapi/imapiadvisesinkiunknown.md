---
title: Имапиадвисесинк IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350920"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="e87dd-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e87dd-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="e87dd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e87dd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e87dd-105">Реализует объект приемника уведомлений для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e87dd-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="e87dd-106">Указатель на объект приемника уведомлений передается при вызове метода **advise** поставщика услуг, механизм, используемый для регистрации уведомлений.</span><span class="sxs-lookup"><span data-stu-id="e87dd-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e87dd-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="e87dd-107">Header file:</span></span>  <br/> |<span data-ttu-id="e87dd-108">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="e87dd-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="e87dd-109">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="e87dd-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="e87dd-110">Объекты приемника уведомлений</span><span class="sxs-lookup"><span data-stu-id="e87dd-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="e87dd-111">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="e87dd-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="e87dd-112">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="e87dd-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="e87dd-113">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="e87dd-113">Called by:</span></span>  <br/> |<span data-ttu-id="e87dd-114">Поставщики услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="e87dd-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="e87dd-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e87dd-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e87dd-116">Иид_имапиадвисесинк</span><span class="sxs-lookup"><span data-stu-id="e87dd-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="e87dd-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="e87dd-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="e87dd-118">ЛПМАПИАДВИСЕСИНК</span><span class="sxs-lookup"><span data-stu-id="e87dd-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e87dd-119">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="e87dd-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="e87dd-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="e87dd-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="e87dd-121">Реагирует на уведомление, выполняя одну или несколько задач.</span><span class="sxs-lookup"><span data-stu-id="e87dd-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="e87dd-122">Выполняемые задачи зависят от типа события и объекта, который создает уведомление.</span><span class="sxs-lookup"><span data-stu-id="e87dd-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e87dd-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e87dd-123">See also</span></span>



[<span data-ttu-id="e87dd-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="e87dd-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

