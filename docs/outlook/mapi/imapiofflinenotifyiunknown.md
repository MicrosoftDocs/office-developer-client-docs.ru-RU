---
title: IMAPIOfflineNotify IUnknown
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIOfflineNotify
api_type:
- COM
ms.assetid: a593d2a1-29f8-7e23-85bf-02fa3cfebe1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: adcb8e78d4e85e19d4102795aa4d43f06a7f86ba
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568149"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="52a7b-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="52a7b-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="52a7b-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52a7b-105">Отправка уведомлений обратных вызовов в клиент поддерживает Microsoft Outlook 2010 и Microsoft Outlook 2013.</span><span class="sxs-lookup"><span data-stu-id="52a7b-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52a7b-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="52a7b-106">Provided by:</span></span>  <br/> |<span data-ttu-id="52a7b-107">Клиент</span><span class="sxs-lookup"><span data-stu-id="52a7b-107">Client</span></span>  <br/> |
|<span data-ttu-id="52a7b-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="52a7b-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="52a7b-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="52a7b-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="52a7b-110">Порядке vtable</span><span class="sxs-lookup"><span data-stu-id="52a7b-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="52a7b-111">Уведомления</span><span class="sxs-lookup"><span data-stu-id="52a7b-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="52a7b-112">Отправляет уведомления об изменениях в состоянии подключения к клиенту.</span><span class="sxs-lookup"><span data-stu-id="52a7b-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52a7b-113">Замечания</span><span class="sxs-lookup"><span data-stu-id="52a7b-113">Remarks</span></span>

<span data-ttu-id="52a7b-114">Клиент должен реализовывать этот интерфейс и передать указатель на него в качестве члена группы в **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** при настройке обратных вызовов с помощью **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="52a7b-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="52a7b-115">Следовательно Outlook 2010 или Outlook 2013 могут использовать этот интерфейс для отправки уведомлений обратных вызовов для клиента.</span><span class="sxs-lookup"><span data-stu-id="52a7b-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="52a7b-116">См. также</span><span class="sxs-lookup"><span data-stu-id="52a7b-116">See also</span></span>



[<span data-ttu-id="52a7b-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="52a7b-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="52a7b-118">Сведения об API автономного состояния</span><span class="sxs-lookup"><span data-stu-id="52a7b-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="52a7b-119">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="52a7b-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="52a7b-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="52a7b-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

