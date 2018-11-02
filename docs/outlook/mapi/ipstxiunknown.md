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
ms.openlocfilehash: 98c3f33c5f9b4745787d6acb55d7afb230e23518
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564243"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="e0557-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="e0557-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="e0557-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0557-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0557-105">Этот интерфейс предоставляет функциональные возможности модуля поддержки при выполнении репликации с помощью интерфейса **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="e0557-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="e0557-106">Автор</span><span class="sxs-lookup"><span data-stu-id="e0557-106">Provided by</span></span>  <br/> |<span data-ttu-id="e0557-107">Запрос на [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="e0557-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="e0557-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="e0557-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="e0557-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="e0557-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="e0557-110">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="e0557-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="e0557-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="e0557-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="e0557-112">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="e0557-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="e0557-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="e0557-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="e0557-114">Получает связанное интерфейс **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="e0557-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="e0557-115">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-116">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-117">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-118">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-119">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-120">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-121">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-122">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="e0557-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="e0557-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="e0557-124">Задает локальное хранилище для эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="e0557-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="e0557-125">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-126">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-127">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-128">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-129">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-130">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-131">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-132">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="e0557-133">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="e0557-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="e0557-134">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="e0557-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="e0557-135">См. также</span><span class="sxs-lookup"><span data-stu-id="e0557-135">See also</span></span>



[<span data-ttu-id="e0557-136">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="e0557-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="e0557-137">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="e0557-137">MAPI Constants</span></span>](mapi-constants.md)

