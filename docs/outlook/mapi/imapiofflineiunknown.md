---
title: IMAPIOffline IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOffline
api_type:
- COM
ms.assetid: 211281ff-3c22-1b51-4b72-ca1e313c7202
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 20d8c39765b0dbbfdde530361894d0a27876010a
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321268"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="55de4-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55de4-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="55de4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55de4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55de4-105">Предоставляет сведения для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="55de4-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="55de4-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="55de4-106">Provided by:</span></span>  <br/> |<span data-ttu-id="55de4-107">Запрос к [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="55de4-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="55de4-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="55de4-108">Called by:</span></span>  <br/> |<span data-ttu-id="55de4-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="55de4-109">Client</span></span>  <br/> |
|<span data-ttu-id="55de4-110">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="55de4-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="55de4-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="55de4-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="55de4-112">Порядок ветвей</span><span class="sxs-lookup"><span data-stu-id="55de4-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="55de4-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="55de4-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="55de4-114">Задает текущее состояние автономного объекта в сетевом или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="55de4-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="55de4-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="55de4-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="55de4-116">Получает условия, для которых автономный объект поддерживает вызовы.</span><span class="sxs-lookup"><span data-stu-id="55de4-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="55de4-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="55de4-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="55de4-118">Получает текущее сетевое или автономное состояние автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="55de4-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="55de4-119">*Член-заметель*</span><span class="sxs-lookup"><span data-stu-id="55de4-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="55de4-120">Этот член является местоимящиком и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="55de4-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="55de4-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="55de4-121">Remarks</span></span>

<span data-ttu-id="55de4-122">Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получения автономного объекта, который поддерживает **IMAPIOfflineMgr.**</span><span class="sxs-lookup"><span data-stu-id="55de4-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="55de4-123">Так как **IMAPIOfflineMgr** наследуется от [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)клиент может запросить этот интерфейс (с помощью [IUnknown::QueryInterface),](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)чтобы получить указатель на указатель интерфейса **для IMAPIOffline** для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="55de4-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="55de4-124">Затем клиент может получить или установить текущее состояние объекта или узнать о возможностях вызова объекта (путем вызова **IMAPIOffline::GetCapabilities)** и настроить функцию перезаписи вызовов с помощью **[IMAPIOfflineMgr.](imapiofflinemgrimapioffline.md)**</span><span class="sxs-lookup"><span data-stu-id="55de4-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="55de4-125">Член в этом интерфейсе — это замесерв, зарезервированный для внутреннего использования Microsoft Outlook 2013 и на который могут быть внося изменения.</span><span class="sxs-lookup"><span data-stu-id="55de4-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="55de4-126">Другие члены этого интерфейса должны использоваться только в документе.</span><span class="sxs-lookup"><span data-stu-id="55de4-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="55de4-127">См. также</span><span class="sxs-lookup"><span data-stu-id="55de4-127">See also</span></span>



[<span data-ttu-id="55de4-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="55de4-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="55de4-129">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="55de4-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="55de4-130">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="55de4-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="55de4-131">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="55de4-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

