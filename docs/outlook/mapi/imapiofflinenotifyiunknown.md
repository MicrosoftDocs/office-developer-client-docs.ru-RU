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
ms.openlocfilehash: 940cf0cf377f1b38071df5e3c300ccb7d685e5a2
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439879"
---
# <a name="imapiofflinenotify--iunknown"></a><span data-ttu-id="6df4f-103">IMAPIOfflineNotify : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6df4f-103">IMAPIOfflineNotify : IUnknown</span></span>

  
  
<span data-ttu-id="6df4f-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6df4f-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6df4f-105">Поддерживает Microsoft Outlook 2010, русская версия и Microsoft Outlook 2013 при отправке клиенту отзовов уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6df4f-105">Supports Microsoft Outlook 2010 and Microsoft Outlook 2013 in sending notification callbacks to a client.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6df4f-106">Предоставлено:</span><span class="sxs-lookup"><span data-stu-id="6df4f-106">Provided by:</span></span>  <br/> |<span data-ttu-id="6df4f-107">Клиент</span><span class="sxs-lookup"><span data-stu-id="6df4f-107">Client</span></span>  <br/> |
|<span data-ttu-id="6df4f-108">Идентификатор интерфейса:</span><span class="sxs-lookup"><span data-stu-id="6df4f-108">Interface identifier:</span></span>  <br/> |<span data-ttu-id="6df4f-109">IID_IMAPIOfflineNotify</span><span class="sxs-lookup"><span data-stu-id="6df4f-109">IID_IMAPIOfflineNotify</span></span>  <br/> |
   
## <a name="vtable-order"></a><span data-ttu-id="6df4f-110">Заказ Vtable</span><span class="sxs-lookup"><span data-stu-id="6df4f-110">Vtable order</span></span>

|||
|:-----|:-----|
|[<span data-ttu-id="6df4f-111">Уведомить</span><span class="sxs-lookup"><span data-stu-id="6df4f-111">Notify</span></span>](imapiofflinenotify-notify.md) <br/> |<span data-ttu-id="6df4f-112">Отправляет клиенту уведомления об изменениях в состоянии подключения.</span><span class="sxs-lookup"><span data-stu-id="6df4f-112">Sends notifications to a client about changes in connection state.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6df4f-113">Примечания</span><span class="sxs-lookup"><span data-stu-id="6df4f-113">Remarks</span></span>

<span data-ttu-id="6df4f-114">Клиент должен реализовать этот интерфейс и передать ему указатель в качестве участника в MAPIOFFLINE_ADVISEINFO при **[настройке](mapioffline_adviseinfo.md)** вызовов с помощью **[IMAPIOfflineMgr:::Advise](imapiofflinemgr-advise.md)**.</span><span class="sxs-lookup"><span data-stu-id="6df4f-114">The client must implement this interface and pass a pointer to it as a member in **[MAPIOFFLINE_ADVISEINFO](mapioffline_adviseinfo.md)** when setting up callbacks using **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)**.</span></span> <span data-ttu-id="6df4f-115">Впоследствии Outlook 2010 или Outlook 2013 г. сможет использовать этот интерфейс для отправки клиенту отзова уведомлений.</span><span class="sxs-lookup"><span data-stu-id="6df4f-115">Subsequently, Outlook 2010 or Outlook 2013 will be able to use this interface to send notification callbacks to the client.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="6df4f-116">См. также</span><span class="sxs-lookup"><span data-stu-id="6df4f-116">See also</span></span>



[<span data-ttu-id="6df4f-117">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="6df4f-117">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)


[<span data-ttu-id="6df4f-118">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="6df4f-118">About the Offline State API</span></span>](about-the-offline-state-api.md)
  
[<span data-ttu-id="6df4f-119">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="6df4f-119">MAPI Constants</span></span>](mapi-constants.md)
  
[<span data-ttu-id="6df4f-120">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="6df4f-120">MAPIOFFLINE_ADVISEINFO</span></span>](mapioffline_adviseinfo.md)

