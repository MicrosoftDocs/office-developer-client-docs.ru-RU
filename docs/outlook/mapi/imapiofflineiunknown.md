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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401281"
---
# <a name="imapioffline--iunknown"></a><span data-ttu-id="ee0bd-103">IMAPIOffline : IUnknown</span><span class="sxs-lookup"><span data-stu-id="ee0bd-103">IMAPIOffline : IUnknown</span></span>

  
  
<span data-ttu-id="ee0bd-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ee0bd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ee0bd-105">Предоставляет сведения для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-105">Provides information for an offline object.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ee0bd-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="ee0bd-106">Provided by:</span></span>  <br/> |<span data-ttu-id="ee0bd-107">Запрос на [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span><span class="sxs-lookup"><span data-stu-id="ee0bd-107">Query on [IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)</span></span> <br/> |
|<span data-ttu-id="ee0bd-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="ee0bd-108">Called by:</span></span>  <br/> |<span data-ttu-id="ee0bd-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="ee0bd-109">Client</span></span>  <br/> |
|<span data-ttu-id="ee0bd-110">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="ee0bd-110">Interface identifier:</span></span>  <br/> |<span data-ttu-id="ee0bd-111">IID_IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="ee0bd-111">IID_IMAPIOffline</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="ee0bd-112">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="ee0bd-112">Vtable order</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="ee0bd-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="ee0bd-113">**[SetCurrentState](imapioffline-setcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="ee0bd-114">Задает текущее состояние автономной объекта в сети или в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-114">Sets the current state of an offline object to online or offline.</span></span>  <br/> |
|<span data-ttu-id="ee0bd-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span><span class="sxs-lookup"><span data-stu-id="ee0bd-115">**[GetCapabilities](imapioffline-getcapabilities.md)**</span></span> <br/> |<span data-ttu-id="ee0bd-116">Получает условия, для которых обратные вызовы поддерживаются автономной объектом.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-116">Gets the conditions for which callbacks are supported by an offline object.</span></span>  <br/> |
|<span data-ttu-id="ee0bd-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span><span class="sxs-lookup"><span data-stu-id="ee0bd-117">**[GetCurrentState](imapioffline-getcurrentstate.md)**</span></span> <br/> |<span data-ttu-id="ee0bd-118">Возвращает текущее состояние сетевым и автономным автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-118">Gets the current online or offline state of an offline object.</span></span>  <br/> |
| <span data-ttu-id="ee0bd-119">*Заполнитель члена*</span><span class="sxs-lookup"><span data-stu-id="ee0bd-119">*Placeholder member*</span></span>  <br/> |<span data-ttu-id="ee0bd-120">Этот член — это и не поддерживается.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-120">This member is a placeholder and is not supported.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ee0bd-121">Замечания</span><span class="sxs-lookup"><span data-stu-id="ee0bd-121">Remarks</span></span>

<span data-ttu-id="ee0bd-122">Клиент использует **[HrOpenOfflineObj](hropenofflineobj.md)** для открытия и получить автономного объекта, который поддерживает **IMAPIOfflineMgr**.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-122">A client uses **[HrOpenOfflineObj](hropenofflineobj.md)** to open and obtain an offline object that supports **IMAPIOfflineMgr**.</span></span> <span data-ttu-id="ee0bd-123">Поскольку **IMAPIOfflineMgr** наследуется от [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), клиент может запросить этот интерфейс (с помощью [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) для получения указателя на указатель интерфейса для **IMAPIOffline** для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-123">Because **IMAPIOfflineMgr** inherits from [IUnknown](https://msdn.microsoft.com/library/ms680509%28v=VS.85%29.aspx), the client can query this interface (by using [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx)) to obtain a pointer to the interface pointer for **IMAPIOffline** for the offline object.</span></span> <span data-ttu-id="ee0bd-124">Клиент затем можно получить или задать текущее состояние объекта, или узнать о возможностях обратного вызова объекта (путем вызова **IMAPIOffline::GetCapabilities** ) и выберите Настройка обратных вызовов с помощью **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-124">The client can then get or set the current state of the object, or find out about the callback capabilities of the object (by calling **IMAPIOffline::GetCapabilities** ) and choose to set up callbacks by using **[IMAPIOfflineMgr](imapiofflinemgrimapioffline.md)**.</span></span> 
  
<span data-ttu-id="ee0bd-125">Член этого интерфейса — это значение зарезервировано для внутреннего использования Microsoft Outlook 2013 и может быть изменен.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-125">A member in this interface is a placeholder reserved for the internal use of Microsoft Outlook 2013 and is subject to change.</span></span> <span data-ttu-id="ee0bd-126">Другие элементы в этот интерфейс должен использоваться только в документации.</span><span class="sxs-lookup"><span data-stu-id="ee0bd-126">Other members in this interface must be used only as documented.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="ee0bd-127">См. также</span><span class="sxs-lookup"><span data-stu-id="ee0bd-127">See also</span></span>



[<span data-ttu-id="ee0bd-128">IMAPIOfflineMgr : IMAPIOffline</span><span class="sxs-lookup"><span data-stu-id="ee0bd-128">IMAPIOfflineMgr : IMAPIOffline</span></span>](imapiofflinemgrimapioffline.md)


[<span data-ttu-id="ee0bd-129">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="ee0bd-129">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="ee0bd-130">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="ee0bd-130">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="ee0bd-131">Интерфейсы MAPI</span><span class="sxs-lookup"><span data-stu-id="ee0bd-131">MAPI Interfaces</span></span>](mapi-interfaces.md)

