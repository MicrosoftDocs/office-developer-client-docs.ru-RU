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
ms.openlocfilehash: 4e7df570851aa515e07117d05103f7c0631c90f9
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809582"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="3f0da-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="3f0da-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="3f0da-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3f0da-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3f0da-105">Этот интерфейс предоставляет функциональные возможности модуля поддержки при выполнении репликации с помощью интерфейса **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="3f0da-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="3f0da-106">Автор</span><span class="sxs-lookup"><span data-stu-id="3f0da-106">Provided by</span></span>  <br/> |<span data-ttu-id="3f0da-107">Запрос на [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="3f0da-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="3f0da-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="3f0da-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="3f0da-109">IID_IPSTX</span><span class="sxs-lookup"><span data-stu-id="3f0da-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="3f0da-110">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="3f0da-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="3f0da-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0da-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="3f0da-112">Получает расширенные сведения о последней ошибки.</span><span class="sxs-lookup"><span data-stu-id="3f0da-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="3f0da-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0da-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="3f0da-114">Получает связанное интерфейс **[IOSTX](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="3f0da-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="3f0da-115">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-116">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-117">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-118">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-119">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-120">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-121">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-122">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="3f0da-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="3f0da-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="3f0da-124">Задает локальное хранилище для эмуляции диспетчера протокола Outlook очереди исходящих сообщений на сервере.</span><span class="sxs-lookup"><span data-stu-id="3f0da-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="3f0da-125">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-126">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-127">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-128">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-129">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-130">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-131">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-132">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="3f0da-133">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="3f0da-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="3f0da-134">*Не поддерживается, документированных.*</span><span class="sxs-lookup"><span data-stu-id="3f0da-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="3f0da-135">См. также</span><span class="sxs-lookup"><span data-stu-id="3f0da-135">See also</span></span>



[<span data-ttu-id="3f0da-136">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="3f0da-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="3f0da-137">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3f0da-137">MAPI Constants</span></span>](mapi-constants.md)

