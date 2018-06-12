---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет категоризации после отправки почтового элемента на основании его PidTagConversationId.
ms.openlocfilehash: efecfc2d0d865428cb958fc15a858bbc7807c5d1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807708"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="12207-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="12207-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="12207-104">Выполняет категоризации после отправки почтового элемента на основании его [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="12207-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="12207-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="12207-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="12207-106">Экспортировать с:</span><span class="sxs-lookup"><span data-stu-id="12207-106">Exported by:</span></span>  <br/> |<span data-ttu-id="12207-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="12207-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="12207-108">Вызывается:</span><span class="sxs-lookup"><span data-stu-id="12207-108">Called by:</span></span>  <br/> |<span data-ttu-id="12207-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="12207-109">Client</span></span>  <br/> |
|<span data-ttu-id="12207-110">Реализованный:</span><span class="sxs-lookup"><span data-stu-id="12207-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="12207-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="12207-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="12207-112">Parameters</span><span class="sxs-lookup"><span data-stu-id="12207-112">Parameters</span></span>

<span data-ttu-id="12207-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="12207-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="12207-114">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) хранилище или [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) из почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="12207-114">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](http://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="12207-115">Не может быть NULL или недопустимые.</span><span class="sxs-lookup"><span data-stu-id="12207-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="12207-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="12207-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="12207-117">[in] [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="12207-117">[in] The [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="12207-118">Не может быть NULL или недопустимые.</span><span class="sxs-lookup"><span data-stu-id="12207-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="12207-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="12207-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="12207-120">[in] [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="12207-120">[in] The [PidTagConversationId](http://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="12207-121">Не может быть NULL или недопустимые.</span><span class="sxs-lookup"><span data-stu-id="12207-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="12207-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="12207-122">_dwFlags_</span></span>
  
> <span data-ttu-id="12207-123">[in] Битовая маска, которая указывает Дополнительные сведения о вызове метода.</span><span class="sxs-lookup"><span data-stu-id="12207-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="12207-124">0 — Дополнительные параметры не используются в вызове этого метода.</span><span class="sxs-lookup"><span data-stu-id="12207-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="12207-125">Это рекомендуемое значение.</span><span class="sxs-lookup"><span data-stu-id="12207-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="12207-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ — это фактически [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения.</span><span class="sxs-lookup"><span data-stu-id="12207-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](http://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="12207-127">С помощью **PidTagSearchKey** интенсивно и следует избегать при наличии [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="12207-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](http://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="12207-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="12207-128">Return values</span></span>

|<span data-ttu-id="12207-129">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="12207-129">**HRESULT**</span></span>|<span data-ttu-id="12207-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="12207-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="12207-131">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="12207-131">S_OK</span></span>  <br/> |<span data-ttu-id="12207-132">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="12207-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="12207-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="12207-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="12207-134">_dwFlags_ содержит неизвестное флаг.</span><span class="sxs-lookup"><span data-stu-id="12207-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="12207-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="12207-135">Remarks</span></span>

<span data-ttu-id="12207-136">Категории считаются персональные данные и не будут передаваться за пределами почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="12207-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="12207-137">Таким образом не вызывать **HrProcessConvActionForSentItem** неотправленные почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="12207-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="12207-138">Вместо этого отправить элемент, а затем вызвать **HrProcessConvActionForSentItem** на резервной копии.</span><span class="sxs-lookup"><span data-stu-id="12207-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="12207-139">Архивные копии могут храниться в папке «Отправленные» или соответствующее место.</span><span class="sxs-lookup"><span data-stu-id="12207-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="12207-140">Ваше приложение не должно содержать в работе с Outlook.exe, например, из надстройки COM, чтобы вызвать **HrProcessConvActionForSentItem**.</span><span class="sxs-lookup"><span data-stu-id="12207-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="12207-141">При попытке вызова **HrProcessConvActionForSentItem** ожидания процесс **HrProcessConvActionForSentItem** вызовет исключение нарушение прав доступа.</span><span class="sxs-lookup"><span data-stu-id="12207-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

