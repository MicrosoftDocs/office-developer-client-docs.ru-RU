---
title: ИПСТКС IUnknown
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32278801"
---
# <a name="ipstx--iunknown"></a><span data-ttu-id="9db65-103">IPSTX : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9db65-103">IPSTX : IUnknown</span></span>

  
  
<span data-ttu-id="9db65-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9db65-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9db65-105">Этот интерфейс предоставляет вспомогательные функциональные возможности при выполнении репликации с помощью интерфейса **[иосткс](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="9db65-105">This interface provides helper functionality when performing replication through the **[IOSTX](iostxiunknown.md)** interface.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="9db65-106">Предоставлено</span><span class="sxs-lookup"><span data-stu-id="9db65-106">Provided by</span></span>  <br/> |<span data-ttu-id="9db65-107">Запрос на [IMsgStore](imsgstoreimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="9db65-107">Query on [IMsgStore](imsgstoreimapiprop.md)</span></span> <br/> |
|<span data-ttu-id="9db65-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="9db65-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="9db65-109">ИИД_ИПСТКС</span><span class="sxs-lookup"><span data-stu-id="9db65-109">IID_IPSTX</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="9db65-110">Заказ vtable</span><span class="sxs-lookup"><span data-stu-id="9db65-110">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="9db65-111">**[GetLastError](ipstx-getlasterror.md)**</span><span class="sxs-lookup"><span data-stu-id="9db65-111">**[GetLastError](ipstx-getlasterror.md)**</span></span> <br/> |<span data-ttu-id="9db65-112">Получает расширенные сведения о последней ошибке.</span><span class="sxs-lookup"><span data-stu-id="9db65-112">Gets extended information about the last error.</span></span>  <br/> |
|<span data-ttu-id="9db65-113">**[Жетсинкобжект](ipstx-getsyncobject.md)**</span><span class="sxs-lookup"><span data-stu-id="9db65-113">**[GetSyncObject](ipstx-getsyncobject.md)**</span></span> <br/> |<span data-ttu-id="9db65-114">Получает связанный интерфейс **[иосткс](iostxiunknown.md)** .</span><span class="sxs-lookup"><span data-stu-id="9db65-114">Gets the associated **[IOSTX](iostxiunknown.md)** interface.</span></span>  <br/> |
| <span data-ttu-id="9db65-115">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-115">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-116">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-116">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-117">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-117">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-118">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-118">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-119">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-119">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-120">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-120">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-121">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-121">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-122">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-122">*Not supported or documented.*</span></span>  <br/> |
|<span data-ttu-id="9db65-123">**[Емулатеспулер](ipstx-emulatespooler.md)**</span><span class="sxs-lookup"><span data-stu-id="9db65-123">**[EmulateSpooler](ipstx-emulatespooler.md)**</span></span> <br/> |<span data-ttu-id="9db65-124">Задает локальное хранилище для эмуляции диспетчера протокола Outlook для постановки в очередь исходящих сообщений на сервер.</span><span class="sxs-lookup"><span data-stu-id="9db65-124">Sets a local store to emulate the Outlook Protocol Manager to spool outgoing messages to a server.</span></span>  <br/> |
| <span data-ttu-id="9db65-125">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-125">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-126">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-126">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-127">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-127">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-128">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-128">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-129">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-129">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-130">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-130">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-131">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-131">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-132">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-132">*Not supported or documented.*</span></span>  <br/> |
| <span data-ttu-id="9db65-133">*Элемент PlaceHolder*</span><span class="sxs-lookup"><span data-stu-id="9db65-133">*Placeholder member*</span></span>  <br/> | <span data-ttu-id="9db65-134">*Не поддерживается или не задокументировано.*</span><span class="sxs-lookup"><span data-stu-id="9db65-134">*Not supported or documented.*</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9db65-135">См. также</span><span class="sxs-lookup"><span data-stu-id="9db65-135">See also</span></span>



[<span data-ttu-id="9db65-136">Сведения об API репликации</span><span class="sxs-lookup"><span data-stu-id="9db65-136">About the Replication API</span></span>](about-the-replication-api.md)
  
[<span data-ttu-id="9db65-137">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="9db65-137">MAPI Constants</span></span>](mapi-constants.md)

