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
# <a name="mapioffline_adviseinfo"></a><span data-ttu-id="3d513-103">MAPIOFFLINE_ADVISEINFO</span><span class="sxs-lookup"><span data-stu-id="3d513-103">MAPIOFFLINE_ADVISEINFO</span></span>
 
<span data-ttu-id="3d513-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3d513-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3d513-105">Предоставляет сведения **[для IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** для регистрации вызова для автономного объекта.</span><span class="sxs-lookup"><span data-stu-id="3d513-105">Provides information to **[IMAPIOfflineMgr::Advise](imapiofflinemgr-advise.md)** to register callback for an offline object.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="3d513-106">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="3d513-106">Quick info</span></span>

<span data-ttu-id="3d513-107">См. **IMAPIOfflineMgr::Advise**.</span><span class="sxs-lookup"><span data-stu-id="3d513-107">See **IMAPIOfflineMgr::Advise**.</span></span> 
  
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

## <a name="members"></a><span data-ttu-id="3d513-108">"Участники"</span><span class="sxs-lookup"><span data-stu-id="3d513-108">Members</span></span>

<span data-ttu-id="3d513-109">_ulSize_: размер **MAPIOFFLINE_ADVISEINFO**.</span><span class="sxs-lookup"><span data-stu-id="3d513-109">_ulSize_: The size of **MAPIOFFLINE_ADVISEINFO**.</span></span> 
    
<span data-ttu-id="3d513-110">_ulClientToken_: маркер, определенный клиентом о вызове.</span><span class="sxs-lookup"><span data-stu-id="3d513-110">_ulClientToken_: A token defined by the client about a callback.</span></span> <span data-ttu-id="3d513-111">Это член *ulClientToken* структуры **[](mapioffline_notify.md)** MAPIOFFLINE_NOTIFY, переданной **[IMAPIOfflineNotify::Notify.](imapiofflinenotify-notify.md)**</span><span class="sxs-lookup"><span data-stu-id="3d513-111">It is the *ulClientToken* member of the **[MAPIOFFLINE_NOTIFY](mapioffline_notify.md)** structure passed to **[IMAPIOfflineNotify::Notify](imapiofflinenotify-notify.md)**.</span></span> 
    
<span data-ttu-id="3d513-112">_CallbackType_: тип вызываемого вызова.</span><span class="sxs-lookup"><span data-stu-id="3d513-112">_CallbackType_: Type of callback to make.</span></span>
    
   -  <span data-ttu-id="3d513-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span><span class="sxs-lookup"><span data-stu-id="3d513-113">MAPIOFFLINE_CALLBACK_TYPE_NOTIFY</span></span> 
    
   - <span data-ttu-id="3d513-114">Тип вызова по уведомлению.</span><span class="sxs-lookup"><span data-stu-id="3d513-114">The type of callback is by notification.</span></span> <span data-ttu-id="3d513-115">Это единственный поддерживаемый тип вызова.</span><span class="sxs-lookup"><span data-stu-id="3d513-115">This is the only supported type of callback.</span></span>  <span data-ttu-id="3d513-116">*pCallback* должен указывать интерфейс **[IMAPIOfflineNotify.](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="3d513-116">*pCallback*  must indicate the interface **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="3d513-117">_pCallback_: интерфейс для использования для вызова.</span><span class="sxs-lookup"><span data-stu-id="3d513-117">_pCallback_: Interface to use for callback.</span></span> <span data-ttu-id="3d513-118">Это реализация **[IMAPIOfflineNotify клиента.](imapiofflinenotifyiunknown.md)**</span><span class="sxs-lookup"><span data-stu-id="3d513-118">This is the client's implementation of **[IMAPIOfflineNotify](imapiofflinenotifyiunknown.md)**.</span></span> 
    
<span data-ttu-id="3d513-119">_ulAdviseTypes_: типы консультаций, определенные условием для рекомендации.</span><span class="sxs-lookup"><span data-stu-id="3d513-119">_ulAdviseTypes_: The types of advise, as identified by the condition for advising.</span></span> <span data-ttu-id="3d513-120">Единственный поддерживаемый тип — MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span><span class="sxs-lookup"><span data-stu-id="3d513-120">The only supported type is MAPIOFFLINE_ADVISE_TYPE_STATECHANGE.</span></span>
    
<span data-ttu-id="3d513-121">_ulStateMask_: единственным поддерживаемым состоянием является MAPIOFFLINE_STATE_ALL.</span><span class="sxs-lookup"><span data-stu-id="3d513-121">_ulStateMask_: The only supported state is MAPIOFFLINE_STATE_ALL.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="3d513-122">См. также</span><span class="sxs-lookup"><span data-stu-id="3d513-122">See also</span></span>

- [<span data-ttu-id="3d513-123">IMAPIOfflineMgr::Advise</span><span class="sxs-lookup"><span data-stu-id="3d513-123">IMAPIOfflineMgr::Advise</span></span>](imapiofflinemgr-advise.md)
- [<span data-ttu-id="3d513-124">Об API автономного режима</span><span class="sxs-lookup"><span data-stu-id="3d513-124">About the Offline State API</span></span>](about-the-offline-state-api.md) 
- [<span data-ttu-id="3d513-125">��������� MAPI</span><span class="sxs-lookup"><span data-stu-id="3d513-125">MAPI Constants</span></span>](mapi-constants.md) 
- [<span data-ttu-id="3d513-126">MAPIOFFLINE_CALLBACK_TYPE</span><span class="sxs-lookup"><span data-stu-id="3d513-126">MAPIOFFLINE_CALLBACK_TYPE</span></span>](mapioffline_callback_type.md)

