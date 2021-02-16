---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет классификацию почтового элемента после отправки на основе его PidTagConversationId.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318902"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="00023-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="00023-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="00023-104">Выполняет категоризацию почтового элемента после отправки на основе [его PidTagConversationId.](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00023-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="00023-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="00023-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="00023-106">Экспортируется с помощью:</span><span class="sxs-lookup"><span data-stu-id="00023-106">Exported by:</span></span>  <br/> |<span data-ttu-id="00023-107">Outlook.exe</span><span class="sxs-lookup"><span data-stu-id="00023-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="00023-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="00023-108">Called by:</span></span>  <br/> |<span data-ttu-id="00023-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="00023-109">Client</span></span>  <br/> |
|<span data-ttu-id="00023-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="00023-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="00023-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="00023-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="00023-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="00023-112">Parameters</span></span>

<span data-ttu-id="00023-113">_pmbinStoreEid_</span><span class="sxs-lookup"><span data-stu-id="00023-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="00023-114">[in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) магазина или [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="00023-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="00023-115">Не может быть NULL или недопустимым.</span><span class="sxs-lookup"><span data-stu-id="00023-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="00023-116">_pmbinMsgEid_</span><span class="sxs-lookup"><span data-stu-id="00023-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="00023-117">[in] [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="00023-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="00023-118">Не может быть NULL или недопустимым.</span><span class="sxs-lookup"><span data-stu-id="00023-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="00023-119">_pmbinConvID_</span><span class="sxs-lookup"><span data-stu-id="00023-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="00023-120">[in] [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="00023-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="00023-121">Не может быть NULL или недопустимым.</span><span class="sxs-lookup"><span data-stu-id="00023-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="00023-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="00023-122">_dwFlags_</span></span>
  
> <span data-ttu-id="00023-123">[in] Битоваяmas, которая указывает дополнительные сведения о вызове метода.</span><span class="sxs-lookup"><span data-stu-id="00023-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="00023-124">0 — в этом вызове метода не используются дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="00023-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="00023-125">Это рекомендуемое значение.</span><span class="sxs-lookup"><span data-stu-id="00023-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="00023-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ фактически является [pidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения.</span><span class="sxs-lookup"><span data-stu-id="00023-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="00023-127">Использование **PidTagSearchKey** ресурсоемко, и его следует избегать, [если доступен PidTagEntryId.](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="00023-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="00023-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="00023-128">Return values</span></span>

|<span data-ttu-id="00023-129">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="00023-129">**HRESULT**</span></span>|<span data-ttu-id="00023-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="00023-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="00023-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="00023-131">S_OK</span></span>  <br/> |<span data-ttu-id="00023-132">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="00023-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="00023-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="00023-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="00023-134">_dwFlags содержит_ неизвестный флаг.</span><span class="sxs-lookup"><span data-stu-id="00023-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="00023-135">Примечания</span><span class="sxs-lookup"><span data-stu-id="00023-135">Remarks</span></span>

<span data-ttu-id="00023-136">Категории считаются персональными данными и не должны передаваться за пределы почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="00023-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="00023-137">Поэтому не вызывайте **HrProcessConvActionForSentItem** для элемента неподдерживаемой почты.</span><span class="sxs-lookup"><span data-stu-id="00023-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="00023-138">Вместо этого отправьте элемент, а затем вызовите **HrProcessConvActionForSentItem** в архивной копии.</span><span class="sxs-lookup"><span data-stu-id="00023-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="00023-139">Архивная копия может храниться в папке "Отправленные" или в эквивалентном расположении.</span><span class="sxs-lookup"><span data-stu-id="00023-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="00023-140">Для вызова **HrProcessConvActionForSentItem** приложение должно быть в процессе Outlook.exe, например из надстройки COM.</span><span class="sxs-lookup"><span data-stu-id="00023-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="00023-141">Если попытаться вызвать **HrProcessConvActionForSentItem** вне процесса, **HrProcessConvActionForSentItem выдает** исключение нарушения доступа.</span><span class="sxs-lookup"><span data-stu-id="00023-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

