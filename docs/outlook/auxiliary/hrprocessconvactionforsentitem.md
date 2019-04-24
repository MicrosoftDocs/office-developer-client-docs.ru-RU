---
title: HrProcessConvActionForSentItem
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: overview
localization_priority: Normal
ms.assetid: 08121e33-7820-4a31-b6da-06a4a54ec43f
description: Выполняет категоризацию после отправки для почтового элемента на основе его Пидтагконверсатионид.
ms.openlocfilehash: 675f308093eea30084271abc66c1fa66e2ad6828
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318902"
---
# <a name="hrprocessconvactionforsentitem"></a><span data-ttu-id="4edbe-103">HrProcessConvActionForSentItem</span><span class="sxs-lookup"><span data-stu-id="4edbe-103">HrProcessConvActionForSentItem</span></span>

<span data-ttu-id="4edbe-104">Выполняет категоризацию после отправки для почтового элемента на основе его [пидтагконверсатионид](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="4edbe-104">Performs post-send categorization on a mail item based on its [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx).</span></span>
  
## <a name="quick-info"></a><span data-ttu-id="4edbe-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4edbe-105">Quick info</span></span>

|||
|:-----|:-----|
|<span data-ttu-id="4edbe-106">Экспортировано:</span><span class="sxs-lookup"><span data-stu-id="4edbe-106">Exported by:</span></span>  <br/> |<span data-ttu-id="4edbe-107">Outlook. exe</span><span class="sxs-lookup"><span data-stu-id="4edbe-107">Outlook.exe</span></span>  <br/> |
|<span data-ttu-id="4edbe-108">Вызывающая сторона:</span><span class="sxs-lookup"><span data-stu-id="4edbe-108">Called by:</span></span>  <br/> |<span data-ttu-id="4edbe-109">Клиент</span><span class="sxs-lookup"><span data-stu-id="4edbe-109">Client</span></span>  <br/> |
|<span data-ttu-id="4edbe-110">Реализовано в:</span><span class="sxs-lookup"><span data-stu-id="4edbe-110">Implemented by:</span></span>  <br/> |<span data-ttu-id="4edbe-111">Outlook</span><span class="sxs-lookup"><span data-stu-id="4edbe-111">Outlook</span></span>  <br/> |
   
```cpp
HRESULT WINAPI HrProcessConvActionForSentItem( 
    SBinary const *pmbinStoreEid, 
    SBinary const *pmbinMsgEid, 
    SBinary const *pmbinConvID, 
    DWORD dwFlags)
```

## <a name="parameters"></a><span data-ttu-id="4edbe-112">Параметры</span><span class="sxs-lookup"><span data-stu-id="4edbe-112">Parameters</span></span>

<span data-ttu-id="4edbe-113">_Пмбинсториид_</span><span class="sxs-lookup"><span data-stu-id="4edbe-113">_pmbinStoreEid_</span></span>
  
> <span data-ttu-id="4edbe-114">возврата [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) хранилища или [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="4edbe-114">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the store, or the [PidTagStoreEntryId](https://msdn.microsoft.com/library/0d705667-19f4-4eda-a068-e65ea8f00d9b%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="4edbe-115">Не может иметь значение NULL или быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4edbe-115">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="4edbe-116">_Пмбинмсжеид_</span><span class="sxs-lookup"><span data-stu-id="4edbe-116">_pmbinMsgEid_</span></span>
  
> <span data-ttu-id="4edbe-117">возврата [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="4edbe-117">[in] The [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="4edbe-118">Не может иметь значение NULL или быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4edbe-118">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="4edbe-119">_Пмбинконвид_</span><span class="sxs-lookup"><span data-stu-id="4edbe-119">_pmbinConvID_</span></span>
  
> <span data-ttu-id="4edbe-120">возврата [Пидтагконверсатионид](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="4edbe-120">[in] The [PidTagConversationId](https://msdn.microsoft.com/library/f8e4a5fa-cb73-4eca-b174-72e1fda821a6%28Office.15%29.aspx) of the mail item.</span></span> <span data-ttu-id="4edbe-121">Не может иметь значение NULL или быть недопустимым.</span><span class="sxs-lookup"><span data-stu-id="4edbe-121">Cannot be NULL or invalid.</span></span> 
    
<span data-ttu-id="4edbe-122">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4edbe-122">_dwFlags_</span></span>
  
> <span data-ttu-id="4edbe-123">возврата Битовая маска, указывающая дополнительные сведения о вызове метода.</span><span class="sxs-lookup"><span data-stu-id="4edbe-123">[in] A bitmask that specifies additional information about the method call.</span></span>
    
   - <span data-ttu-id="4edbe-124">0 — в этом вызове метода не используются дополнительные параметры.</span><span class="sxs-lookup"><span data-stu-id="4edbe-124">0—No additional options are used in this method call.</span></span> <span data-ttu-id="4edbe-125">Это рекомендуемое значение.</span><span class="sxs-lookup"><span data-stu-id="4edbe-125">This is the recommended value.</span></span> 
    
   - <span data-ttu-id="4edbe-126">**Пкафсиф_мсжеид_ис_сеарч_кэй**— _Пмбинмсжеид_ фактически является [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) сообщения.</span><span class="sxs-lookup"><span data-stu-id="4edbe-126">**PCAFSIF_MSGEID_IS_SEARCH_KEY**— _pmbinMsgEid_ is actually the [PidTagSearchKey](https://msdn.microsoft.com/library/fcab369a-a1f4-4425-a272-e35046914a4d%28Office.15%29.aspx) of the message.</span></span> <span data-ttu-id="4edbe-127">Использование **PidTagSearchKey** является трудоемким и его следует избегать, если доступен [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) .</span><span class="sxs-lookup"><span data-stu-id="4edbe-127">Using a **PidTagSearchKey** is resource intensive, and should be avoided if a [PidTagEntryId](https://msdn.microsoft.com/library/ca02e873-c2d2-4d58-8df8-c05fbcdc8fba%28Office.15%29.aspx) is available.</span></span> 
    
## <a name="return-values"></a><span data-ttu-id="4edbe-128">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4edbe-128">Return values</span></span>

|<span data-ttu-id="4edbe-129">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4edbe-129">**HRESULT**</span></span>|<span data-ttu-id="4edbe-130">**Description**</span><span class="sxs-lookup"><span data-stu-id="4edbe-130">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4edbe-131">S_OK</span><span class="sxs-lookup"><span data-stu-id="4edbe-131">S_OK</span></span>  <br/> |<span data-ttu-id="4edbe-132">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4edbe-132">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="4edbe-133">E_INVALIDARG</span><span class="sxs-lookup"><span data-stu-id="4edbe-133">E_INVALIDARG</span></span>  <br/> | <span data-ttu-id="4edbe-134">_dwFlags_ содержит неизвестный флаг.</span><span class="sxs-lookup"><span data-stu-id="4edbe-134">_dwFlags_ contains an unknown flag.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4edbe-135">Замечания</span><span class="sxs-lookup"><span data-stu-id="4edbe-135">Remarks</span></span>

<span data-ttu-id="4edbe-136">Категории считаются персональными сведениями и не должны передаваться вне почтового ящика пользователя.</span><span class="sxs-lookup"><span data-stu-id="4edbe-136">Categories are considered personal information and should not be transmitted outside the mailbox of the user.</span></span> <span data-ttu-id="4edbe-137">Поэтому не вызывайте **хрпроцессконвактионфорсентитем** для неотправленного почтового элемента.</span><span class="sxs-lookup"><span data-stu-id="4edbe-137">Therefore, do not call **HrProcessConvActionForSentItem** on an unsent mail item.</span></span> <span data-ttu-id="4edbe-138">Вместо этого отправьте элемент, а затем вызовите **хрпроцессконвактионфорсентитем** для архивной копии.</span><span class="sxs-lookup"><span data-stu-id="4edbe-138">Instead, send the item, and then call **HrProcessConvActionForSentItem** on the archived copy.</span></span> <span data-ttu-id="4edbe-139">Архивная копия может храниться в папке "Отправленные" или в эквивалентном расположении.</span><span class="sxs-lookup"><span data-stu-id="4edbe-139">The archived copy may be stored in the Sent Items folder, or an equivalent location.</span></span> 
  
<span data-ttu-id="4edbe-140">Приложение должно быть в процессе работы с Outlook. exe, например из надстройки COM, для вызова **хрпроцессконвактионфорсентитем**.</span><span class="sxs-lookup"><span data-stu-id="4edbe-140">Your application must be in-process with Outlook.exe, such as from a COM add-in, to call **HrProcessConvActionForSentItem**.</span></span> <span data-ttu-id="4edbe-141">Если вы попытаетесь вызвать **хрпроцессконвактионфорсентитем** вне процесса, **хрпроцессконвактионфорсентитем** выдаст исключение нарушения прав доступа.</span><span class="sxs-lookup"><span data-stu-id="4edbe-141">If you attempt to call **HrProcessConvActionForSentItem** out-of-process, **HrProcessConvActionForSentItem** will throw an access-violation exception.</span></span> 
  

