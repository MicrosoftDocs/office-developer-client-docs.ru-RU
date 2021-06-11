---
title: IPSTX IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IPSTX
api_type:
- COM
ms.assetid: 73752f57-6fbc-0201-bf95-0e75c56c04e6
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 4c758ecd0134ca11ced6f771303896bd885a22c4
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436225"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="5468a-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5468a-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="5468a-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5468a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5468a-105">Этот интерфейс предоставляет функции помощника при выполнении репликации с помощью **[интерфейса IOSTX.](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="5468a-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="5468a-106">Предоставлено</span><span class="sxs-lookup"><span data-stu-id="5468a-106">Provided by</span></span>  <br/> |<span data-ttu-id="5468a-107">Запрос в [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="5468a-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="5468a-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="5468a-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="5468a-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="5468a-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="5468a-110">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="5468a-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="5468a-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="5468a-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="5468a-112">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="5468a-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="5468a-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="5468a-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="5468a-114">Получает связанный **[интерфейс IOSTX.](iostxiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="5468a-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="5468a-115">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-116">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-117">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-118">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-119">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-120">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-121">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-122">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="5468a-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="5468a-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="5468a-124">Задает локальный магазин, чтобы подражать диспетчеру Outlook протоколов, чтобы перенаправление исходяющих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="5468a-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="5468a-125">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-126">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-127">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-128">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-129">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-130">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-131">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-132">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="5468a-133">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="5468a-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="5468a-134">*Не поддерживается или не документируется.*</span><span class="sxs-lookup"><span data-stu-id="5468a-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5468a-135">См. также</span><span class="sxs-lookup"><span data-stu-id="5468a-135">See also</span></span>



[<span data-ttu-id="5468a-136">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="5468a-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="5468a-137">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="5468a-137">MAPI Constants</span></span>](mapi-constants.md)

