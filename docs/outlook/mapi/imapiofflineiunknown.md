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
# <a name="imapioffline--iunknown"></a><span data-ttu-id="545fc-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="545fc-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="545fc-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="545fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="545fc-105">Предоставляет сведения для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="545fc-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="545fc-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="545fc-106">Provided by:</span></span>  <br/> |<span data-ttu-id="545fc-107">Запрос [на IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="545fc-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="545fc-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="545fc-108">Called by:</span></span>  <br/> |<span data-ttu-id="545fc-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="545fc-109">Client</span></span>  <br/> |
|<span data-ttu-id="545fc-110">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="545fc-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="545fc-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="545fc-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="545fc-112">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="545fc-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="545fc-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="545fc-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="545fc-114">Задает текущее состояние автономного объекта в режиме online или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="545fc-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="545fc-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="545fc-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="545fc-116">Получает условия, для которых вызовы поддерживаются автономным объектом.</span><span class="sxs-lookup"><span data-stu-id="545fc-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="545fc-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="545fc-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="545fc-118">Получает текущее состояние автономного объекта в Интернете или автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="545fc-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="545fc-119">*Член placeholder*</span><span class="sxs-lookup"><span data-stu-id="545fc-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="545fc-120">Этот член является задатщиком и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="545fc-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="545fc-121">Примечания</span><span class="sxs-lookup"><span data-stu-id="545fc-121">Remarks</span></span>

<span data-ttu-id="545fc-122">Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получения автономного объекта, поддерживаюшего **IMAPIOfflineMgr.**</span><span class="sxs-lookup"><span data-stu-id="545fc-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="545fc-123">Поскольку **IMAPIOfflineMgr** наследует [IUnknown,](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx)клиент может запрашивать этот интерфейс (с помощью [IUnknown::QueryInterface),](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)чтобы получить указатель на указатель интерфейса **для IMAPIOffline** для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="545fc-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="545fc-124">Клиент может получить или установить текущее состояние объекта или узнать о возможностях вызова объекта (позвонив **по IMAPIOffline::GetCapabilities)** и выбрать возможность настроить вызовы с помощью **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="545fc-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="545fc-125">Член этого интерфейса — это местообладатель, зарезервированный для внутреннего Microsoft Outlook 2013 и подлежит изменениям.</span><span class="sxs-lookup"><span data-stu-id="545fc-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="545fc-126">Другие участники этого интерфейса должны использоваться только в качестве документированных документов.</span><span class="sxs-lookup"><span data-stu-id="545fc-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="545fc-127">См. также</span><span class="sxs-lookup"><span data-stu-id="545fc-127">See also</span></span>



[<span data-ttu-id="545fc-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="545fc-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="545fc-129">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="545fc-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="545fc-130">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="545fc-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="545fc-131">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="545fc-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

