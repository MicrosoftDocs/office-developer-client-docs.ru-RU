---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Отображает диалоговое окно "Параметры учетной записи" или "Добавление новой учетной записи".
ms.openlocfilehash: ecf5242fa4f224516e12e667ab66fd0adfe4a25d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33415035"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="928be-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="928be-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="928be-104">Отображает диалоговое окно **"Параметры учетной записи"** или **"Добавление новой** учетной записи".</span><span class="sxs-lookup"><span data-stu-id="928be-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="928be-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="928be-105">Quick info</span></span>

<span data-ttu-id="928be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="928be-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
```cpp
HRESULT IOlkAccountManager::DisplayAccountList ( 
    HWND hwnd,
    DWORD dwFlags,
    LPCWSTR wszTitle,
    DWORD cCategories,
    const CLSID * rgclsidCategories,
    const CLSID * pclsidType
);

```

## <a name="parameters"></a><span data-ttu-id="928be-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="928be-107">Parameters</span></span>

<span data-ttu-id="928be-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="928be-108">_hwnd_</span></span>
  
> <span data-ttu-id="928be-109">[in] Handle to the window to which the displayed dialog box is modal.</span><span class="sxs-lookup"><span data-stu-id="928be-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="928be-110">Может быть нулем.</span><span class="sxs-lookup"><span data-stu-id="928be-110">May be zero.</span></span>
    
<span data-ttu-id="928be-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="928be-111">_dwFlags_</span></span>
  
> <span data-ttu-id="928be-112">[in] Флаги для изменения поведения дисплея.</span><span class="sxs-lookup"><span data-stu-id="928be-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="928be-113">**ACCTUI_NO_WARNING**— не отображайте предупреждение о том, что изменения не будут действовать до перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="928be-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="928be-114">Применяется, только если приложение работает в процессе с Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="928be-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="928be-115">**ACCTUI_SHOW_DATA_TAB**— отображите диалоговое окно **"Параметры** учетной записи" с **выбранной** вкладками "Данные".</span><span class="sxs-lookup"><span data-stu-id="928be-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="928be-116">Допустимо, **только ACCTUI_SHOW_ACCTWIZARD** не за установлено.</span><span class="sxs-lookup"><span data-stu-id="928be-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="928be-117">**ACCTUI_SHOW_ACCTWIZARD**— отобразить диалоговое окно "Добавление **новой** учетной записи".</span><span class="sxs-lookup"><span data-stu-id="928be-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="928be-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="928be-118">_wszTitle_</span></span>
  
> <span data-ttu-id="928be-119">[in] Этот параметр не используется и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="928be-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="928be-120">_cCategories_</span></span>
  
> <span data-ttu-id="928be-121">[in] Этот параметр не используется и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="928be-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="928be-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="928be-123">[in] Этот параметр не используется и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="928be-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="928be-124">_pclsidType_</span></span>
  
> <span data-ttu-id="928be-125">[in] Этот параметр не используется и должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="928be-126">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="928be-126">Return values</span></span>

|<span data-ttu-id="928be-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="928be-127">**HRESULT**</span></span>|<span data-ttu-id="928be-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="928be-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="928be-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="928be-129">S_OK</span></span>  <br/> |<span data-ttu-id="928be-130">Вызов был успешным.</span><span class="sxs-lookup"><span data-stu-id="928be-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="928be-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="928be-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="928be-132">Не удалось создать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="928be-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="928be-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="928be-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="928be-134">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="928be-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="928be-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="928be-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="928be-136">В **диалоговом окне** "Добавление новой учетной записи" возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="928be-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="928be-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="928be-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="928be-138">Параметр  _cCategories,_  _rgclsidCategories_ или  _pclsidType_ не имеет NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="928be-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="928be-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="928be-140">В **диалоговом окне** "Параметры учетной записи" возвращена ошибка.</span><span class="sxs-lookup"><span data-stu-id="928be-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="928be-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="928be-141">Remarks</span></span>

<span data-ttu-id="928be-142">Параметры  _cCategories,_  _rgclsidCategories_ и  _pclsidType_ в настоящее время не используются и должны иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="928be-143">_wszTitle_ не используется и также должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="928be-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

