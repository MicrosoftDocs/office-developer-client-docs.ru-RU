---
title: IMAPIGetSession IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIGetSession
api_type:
- COM
ms.assetid: d1b662e2-1516-46b2-ba94-4092d79b5a39
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0b861a11b6bc1d590225a0c99b20f8be38edfd2b
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436652"
---
# <a name="imapigetsession--iunknown"></a><span data-ttu-id="11072-103">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="11072-103">IMAPIGetSession : IUnknown</span></span>

  
  
<span data-ttu-id="11072-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="11072-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="11072-105">Предоставляет доступ к текущему сеансу MAPI, связанному с объектом поддержки.</span><span class="sxs-lookup"><span data-stu-id="11072-105">Provides access to the current MAPI session associated with the support object.</span></span> <span data-ttu-id="11072-106">Поставщики MAPI могут запрашивать объект поддержки MAPI для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="11072-106">MAPI Providers can query their MAPI Support Object for this interface.</span></span> <span data-ttu-id="11072-107">Дополнительные сведения об объектах поддержки см. в [обзоре объектов поддержки.](support-object-overview.md)</span><span class="sxs-lookup"><span data-stu-id="11072-107">For more information on support objects, see [Support Object Overview](support-object-overview.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="11072-108">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="11072-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="11072-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="11072-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="11072-110">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="11072-110">Called by:</span></span>  <br/> |<span data-ttu-id="11072-111">Поставщики MAPI</span><span class="sxs-lookup"><span data-stu-id="11072-111">MAPI Providers</span></span>  <br/> |
|<span data-ttu-id="11072-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="11072-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="11072-113">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="11072-113">IID_IMAPIGetSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="11072-114">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="11072-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="11072-115">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="11072-115">GetMAPISession</span></span>](imapigetsession-getmapisession.md) <br/> |<span data-ttu-id="11072-116">Вызвано для получения указателя на текущий сеанс MAPI.</span><span class="sxs-lookup"><span data-stu-id="11072-116">Called to obtain a pointer to the current MAPI session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="11072-117">См. также</span><span class="sxs-lookup"><span data-stu-id="11072-117">See also</span></span>



[<span data-ttu-id="11072-118">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="11072-118">GetMAPISession</span></span>](imapigetsession-getmapisession.md)
  
[<span data-ttu-id="11072-119">IMAPISupport</span><span class="sxs-lookup"><span data-stu-id="11072-119">IMAPISupport</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="11072-120">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="11072-120">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="11072-121">Обзор объектов поддержки</span><span class="sxs-lookup"><span data-stu-id="11072-121">Support Object Overview</span></span>](support-object-overview.md)

