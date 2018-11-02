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
ms.openlocfilehash: 82869fa479ebe8a4d7b1881cec5d5c243b7d7957
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22565097"
---
# <a name="mapiofflineadviseinfo"></a><span data-ttu-id="fb2b8-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="fb2b8-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="fb2b8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fb2b8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fb2b8-105">Предоставляет сведения о **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** для регистрации обратного вызова для объекта в автономном режиме.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="fb2b8-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="fb2b8-106">Quick info</span></span>

<span data-ttu-id="fb2b8-107">В разделе **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="fb2b8-108">Элементы</span><span class="sxs-lookup"><span data-stu-id="fb2b8-108">Members</span></span>

<span data-ttu-id="fb2b8-109">_ulSize_: размер **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="fb2b8-110">_ulClientToken_: маркер, определенные в клиента о обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="fb2b8-111">Это член *ulClientToken* структуры **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** , переданной в **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="fb2b8-112">_CallbackType_: тип обратного вызова, чтобы сделать.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="fb2b8-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="fb2b8-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="fb2b8-114">Тип обратного вызова является уведомлений.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-114">The type of callback is by notification.</span></span> <span data-ttu-id="fb2b8-115">Это единственный поддерживаемый тип обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="fb2b8-116">*pCallback* необходимо указать интерфейс **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="fb2b8-117">_pCallback_: интерфейс для обратного вызова.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="fb2b8-118">Это реализация клиента **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="fb2b8-119">_ulAdviseTypes_: типы уведомлений, которые определяются условие с уведомлением о том.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="fb2b8-120">Единственным поддерживаемым типом является MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="fb2b8-121">_ulStateMask_: MAPIOFFLINE_STATE_ALL — это единственный поддерживаемый состояние.</span><span class="sxs-lookup"><span data-stu-id="fb2b8-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fb2b8-122">См. также</span><span class="sxs-lookup"><span data-stu-id="fb2b8-122">See also</span></span>

- [<span data-ttu-id="fb2b8-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="fb2b8-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="fb2b8-124">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="fb2b8-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="fb2b8-125">Константы MAPI</span><span class="sxs-lookup"><span data-stu-id="fb2b8-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="fb2b8-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="fb2b8-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

