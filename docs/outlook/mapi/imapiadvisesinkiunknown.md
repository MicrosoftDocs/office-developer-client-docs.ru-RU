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
ms.openlocfilehash: c6e352288f0bf5b0a3f284441bffc522bf00b9f7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19808809"
---
# <a name="imapiadvisesink--iunknown"></a><span data-ttu-id="11f8b-103">IMAPIAdviseSink : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11f8b-103">IMAPIAdviseSink : IUnknown</span></span>

  
  
<span data-ttu-id="11f8b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="11f8b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="11f8b-105">Реализует объект приемника уведомлений для обработки уведомлений.</span><span class="sxs-lookup"><span data-stu-id="11f8b-105">Implements an advise sink object for handling notification.</span></span> <span data-ttu-id="11f8b-106">В вызове метода **уведомлений** поставщика услуг, механизм, используемый для регистрации уведомления передается указатель на объект приемник уведомлений.</span><span class="sxs-lookup"><span data-stu-id="11f8b-106">A pointer to an advise sink object is passed in a call to a service provider's **Advise** method, the mechanism used to register for notification.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="11f8b-107">Файл заголовка:</span><span class="sxs-lookup"><span data-stu-id="11f8b-107">Header file:</span></span>  <br/> |<span data-ttu-id="11f8b-108">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="11f8b-108">Mapidefs.h</span></span>  <br/> |
|<span data-ttu-id="11f8b-109">Предоставляемые:</span><span class="sxs-lookup"><span data-stu-id="11f8b-109">Exposed by:</span></span>  <br/> |<span data-ttu-id="11f8b-110">Уведомить объектов приемника</span><span class="sxs-lookup"><span data-stu-id="11f8b-110">Advise sink objects</span></span>  <br/> |
|<span data-ttu-id="11f8b-111">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="11f8b-111">Implemented by:</span></span>  <br/> |<span data-ttu-id="11f8b-112">Клиентские приложения и MAPI</span><span class="sxs-lookup"><span data-stu-id="11f8b-112">Client applications and MAPI</span></span>  <br/> |
|<span data-ttu-id="11f8b-113">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="11f8b-113">Called by:</span></span>  <br/> |<span data-ttu-id="11f8b-114">Поставщиков услуг и MAPI</span><span class="sxs-lookup"><span data-stu-id="11f8b-114">Service providers and MAPI</span></span>  <br/> |
|<span data-ttu-id="11f8b-115">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="11f8b-115">Interface identifier:</span></span>  <br/> |<span data-ttu-id="11f8b-116">IID_IMAPIAdviseSink</span><span class="sxs-lookup"><span data-stu-id="11f8b-116">IID_IMAPIAdviseSink</span></span>  <br/> |
|<span data-ttu-id="11f8b-117">Тип указателя:</span><span class="sxs-lookup"><span data-stu-id="11f8b-117">Pointer type:</span></span>  <br/> |<span data-ttu-id="11f8b-118">LPMAPIADVISESINK</span><span class="sxs-lookup"><span data-stu-id="11f8b-118">LPMAPIADVISESINK</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="11f8b-119">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="11f8b-119">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="11f8b-120">OnNotify</span><span class="sxs-lookup"><span data-stu-id="11f8b-120">OnNotify</span></span>](imapiadvisesink-onnotify.md) <br/> |<span data-ttu-id="11f8b-121">Отвечает на уведомление при выполнении одного или нескольких задач.</span><span class="sxs-lookup"><span data-stu-id="11f8b-121">Responds to a notification by performing one or more tasks.</span></span> <span data-ttu-id="11f8b-122">Задачи, выполняемые зависят от типа события и объект, который создает уведомления.</span><span class="sxs-lookup"><span data-stu-id="11f8b-122">The tasks performed depend on the type of event and the object that generates the notification.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11f8b-123">См. также</span><span class="sxs-lookup"><span data-stu-id="11f8b-123">See also</span></span>



[<span data-ttu-id="11f8b-124">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="11f8b-124">MAPI Interfaces</span></span>](mapi-interfaces.md)

