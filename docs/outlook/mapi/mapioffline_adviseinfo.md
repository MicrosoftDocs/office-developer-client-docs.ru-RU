---
title: MAPIOFFLINE_ADVISEINFO
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 20a46c69-d6ae-7d17-f8af-12952867d342
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3cb110fdcbbd88e494c44ba2ed73cc26674638ca
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420026"
---
# <a name="mapioffline_adviseinfo"></a><span data-ttu-id="53fc4-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="53fc4-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="53fc4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="53fc4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="53fc4-105">Предоставляет сведения для **[имапиоффлинемгр:: Advise](imapiofflinemgr-advise.md)** для регистрации обратного вызова для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="53fc4-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="53fc4-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="53fc4-106">Quick info</span></span>

<span data-ttu-id="53fc4-107">Обратитесь к разделу **имапиоффлинемгр:: Advise**.</span><span class="sxs-lookup"><span data-stu-id="53fc4-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
```cpp
typedef struct 
{ 
      ULONG                   ulSize; 
      ULONG                   ulClientToken; 
      MAPIOFFLINE_CALLBACK_TYPE     CallbackType; 
      IUnknown*               pCallback; 
      ULONG                   ulAdviseTypes; 
      ULONG                   ulStateMask; 
} MAPIOFFLINE_ADVISEINFO;
```

## <a name="members"></a><span data-ttu-id="53fc4-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="53fc4-108">Members</span></span>

<span data-ttu-id="53fc4-109">_улсизе_: размер **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="53fc4-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="53fc4-110">_улклиенттокен_: маркер, определяемый клиентом для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="53fc4-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="53fc4-111">Это член *улклиенттокен* структуры **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** , переданный в **[имапиоффлиненотифи:: notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="53fc4-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="53fc4-112">_Каллбакктипе_: тип обратного вызова, который требуется выполнить.</span><span class="sxs-lookup"><span data-stu-id="53fc4-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="53fc4-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="53fc4-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="53fc4-114">Тип обратного вызова — уведомление.</span><span class="sxs-lookup"><span data-stu-id="53fc4-114">The type of callback is by notification.</span></span> <span data-ttu-id="53fc4-115">Это единственный поддерживаемый тип обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="53fc4-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="53fc4-116">*пкаллбакк* должен указывать на интерфейс **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="53fc4-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="53fc4-117">_пкаллбакк_: интерфейс, используемый для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="53fc4-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="53fc4-118">Это реализация **[имапиоффлиненотифи](imapiofflinenotifyiunknown.md)** клиентом.</span><span class="sxs-lookup"><span data-stu-id="53fc4-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="53fc4-119">_уладвисетипес_: типы уведомлений, определяемые условием для рекомендации.</span><span class="sxs-lookup"><span data-stu-id="53fc4-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="53fc4-120">Единственный поддерживаемый тип MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="53fc4-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="53fc4-121">_улстатемаск_: единственное поддерживаемое состояние: MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="53fc4-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="53fc4-122">См. также</span><span class="sxs-lookup"><span data-stu-id="53fc4-122">See also</span></span>

- [<span data-ttu-id="53fc4-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="53fc4-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="53fc4-124">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="53fc4-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="53fc4-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="53fc4-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="53fc4-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="53fc4-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

