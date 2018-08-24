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
ms.openlocfilehash: 90fe316bfd11d712f02187b6a569450b747a6409
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22587931"
---
# <a name="imapigetsession--iunknown"></a><span data-ttu-id="88061-103">IMAPIGetSession : IUnknown</span><span class="sxs-lookup"><span data-stu-id="88061-103">IMAPIGetSession : IUnknown</span></span>

  
  
<span data-ttu-id="88061-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="88061-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="88061-105">Предоставляет доступ к текущему сеансу MAPI, связанного с объектом поддержки.</span><span class="sxs-lookup"><span data-stu-id="88061-105">Provides access to the current MAPI session associated with the support object.</span></span> <span data-ttu-id="88061-106">Поставщики MAPI могут запрашивать их поддержка объект MAPI для этого интерфейса.</span><span class="sxs-lookup"><span data-stu-id="88061-106">MAPI Providers can query their MAPI Support Object for this interface.</span></span> <span data-ttu-id="88061-107">Дополнительные сведения о поддержке объекты см [поддержки объектов](support-object-overview.md).</span><span class="sxs-lookup"><span data-stu-id="88061-107">For more information on support objects, see [Support Object Overview](support-object-overview.md).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="88061-108">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="88061-108">Implemented by:</span></span>  <br/> |<span data-ttu-id="88061-109">MAPI</span><span class="sxs-lookup"><span data-stu-id="88061-109">MAPI</span></span>  <br/> |
|<span data-ttu-id="88061-110">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="88061-110">Called by:</span></span>  <br/> |<span data-ttu-id="88061-111">Поставщики MAPI</span><span class="sxs-lookup"><span data-stu-id="88061-111">MAPI Providers</span></span>  <br/> |
|<span data-ttu-id="88061-112">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="88061-112">Interface identifier:</span></span>  <br/> |<span data-ttu-id="88061-113">IID_IMAPIGetSession</span><span class="sxs-lookup"><span data-stu-id="88061-113">IID_IMAPIGetSession</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="88061-114">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="88061-114">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="88061-115">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="88061-115">GetMAPISession</span></span>](imapigetsession-getmapisession.md) <br/> |<span data-ttu-id="88061-116">Вызывается, чтобы получить указатель текущего сеанса MAPI.</span><span class="sxs-lookup"><span data-stu-id="88061-116">Called to obtain a pointer to the current MAPI session.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="88061-117">См. также</span><span class="sxs-lookup"><span data-stu-id="88061-117">See also</span></span>



[<span data-ttu-id="88061-118">GetMAPISession</span><span class="sxs-lookup"><span data-stu-id="88061-118">GetMAPISession</span></span>](imapigetsession-getmapisession.md)
  
[<span data-ttu-id="88061-119">IMAPISupport</span><span class="sxs-lookup"><span data-stu-id="88061-119">IMAPISupport</span></span>](imapisupportiunknown.md)


[<span data-ttu-id="88061-120">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="88061-120">MAPI Interfaces</span></span>](mapi-interfaces.md)
  
[<span data-ttu-id="88061-121">Обзор поддержки объектов</span><span class="sxs-lookup"><span data-stu-id="88061-121">Support Object Overview</span></span>](support-object-overview.md)

