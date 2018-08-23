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
# <a name="ipstx--iunknown"></a><span data-ttu-id="bb3df-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bb3df-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="bb3df-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bb3df-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bb3df-105">Этот интерфейс предоставляет функциональные возможности модуля поддержки при выполнении репликации с помощью интерфейса **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="bb3df-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="bb3df-106">Автор</span><span class="sxs-lookup"><span data-stu-id="bb3df-106">Provided by</span></span>  <br/> |<span data-ttu-id="bb3df-107">Запрос на [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="bb3df-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="bb3df-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="bb3df-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="bb3df-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="bb3df-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="bb3df-110">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="bb3df-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="bb3df-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="bb3df-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="bb3df-112">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="bb3df-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="bb3df-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="bb3df-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="bb3df-114">Получает связанное интерфейс **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="bb3df-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="bb3df-115">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-116">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-117">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-118">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-119">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-120">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-121">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-122">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="bb3df-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="bb3df-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="bb3df-124">Задает локальное хранилище для эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="bb3df-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="bb3df-125">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-126">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-127">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-128">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-129">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-130">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-131">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-132">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="bb3df-133">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="bb3df-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="bb3df-134">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="bb3df-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bb3df-135">См. также</span><span class="sxs-lookup"><span data-stu-id="bb3df-135">See also</span></span>



[<span data-ttu-id="bb3df-136">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="bb3df-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="bb3df-137">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="bb3df-137">MAPI Constants</span></span>](mapi-constants.md)

