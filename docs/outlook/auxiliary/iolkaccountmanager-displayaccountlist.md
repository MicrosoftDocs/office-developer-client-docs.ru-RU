---
title: IOlkAccountManagerDisplayAccountList
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: a637dcab-81e0-4195-a1d5-61d9957fcf10
description: Отображает диалоговое окно Параметры учетной записи или добавление новой учетной записи.
ms.openlocfilehash: 3c7c433eb4d8f316d32b6cd12bbbbb0e1a1cee43
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807852"
---
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="dc6a7-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="dc6a7-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="dc6a7-104">Отображает диалоговое окно **Настройки учетной записи** и **Добавление новой учетной записи** .</span><span class="sxs-lookup"><span data-stu-id="dc6a7-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="dc6a7-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="dc6a7-105">Quick info</span></span>

<span data-ttu-id="dc6a7-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="dc6a7-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="dc6a7-107">Parameters</span><span class="sxs-lookup"><span data-stu-id="dc6a7-107">Parameters</span></span>

<span data-ttu-id="dc6a7-108">_HWND_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-108">_hwnd_</span></span>
  
> <span data-ttu-id="dc6a7-109">[in] Дескриптор окна модальное диалоговое окно отображаемой.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="dc6a7-110">Может быть равно нулю.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-110">May be zero.</span></span>
    
<span data-ttu-id="dc6a7-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-111">_dwFlags_</span></span>
  
> <span data-ttu-id="dc6a7-112">[in] Флаги для изменения режима отображения.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="dc6a7-113">**ACCTUI_NO_WARNING**— не выводить предупреждения о том, что изменения не вступят в силу только после перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="dc6a7-114">Применяется только в том случае, если приложение является выполняется в процессе с Outlook.exe.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="dc6a7-115">**ACCTUI_SHOW_DATA_TAB**— Показать диалоговое окно **Параметры учетной записи** с вкладкой **данных** .</span><span class="sxs-lookup"><span data-stu-id="dc6a7-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="dc6a7-116">Допустимо только в том случае, если не указано **ACCTUI_SHOW_ACCTWIZARD** .</span><span class="sxs-lookup"><span data-stu-id="dc6a7-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="dc6a7-117">**ACCTUI_SHOW_ACCTWIZARD**— Отображение диалогового окна **Добавление новой учетной записи** .</span><span class="sxs-lookup"><span data-stu-id="dc6a7-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="dc6a7-118">_wszTitle_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-118">_wszTitle_</span></span>
  
> <span data-ttu-id="dc6a7-119">[in] Этот параметр не используется и не должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="dc6a7-120">_cCategories_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-120">_cCategories_</span></span>
  
> <span data-ttu-id="dc6a7-121">[in] Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="dc6a7-122">_rgclsidCategories_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="dc6a7-123">[in] Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="dc6a7-124">_pclsidType_</span><span class="sxs-lookup"><span data-stu-id="dc6a7-124">_pclsidType_</span></span>
  
> <span data-ttu-id="dc6a7-125">[in] Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="dc6a7-126">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="dc6a7-126">Return values</span></span>

|<span data-ttu-id="dc6a7-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="dc6a7-127">**HRESULT**</span></span>|<span data-ttu-id="dc6a7-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="dc6a7-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="dc6a7-129">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="dc6a7-129">S_OK</span></span>  <br/> |<span data-ttu-id="dc6a7-130">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="dc6a7-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="dc6a7-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="dc6a7-132">Не удалось создать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="dc6a7-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="dc6a7-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="dc6a7-134">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="dc6a7-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="dc6a7-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="dc6a7-136">Диалоговое окно " **Добавление новой учетной записи** " возвратил ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="dc6a7-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="dc6a7-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="dc6a7-138">Параметр _cCategories_, _rgclsidCategories_или _pclsidType_ не равно NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="dc6a7-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="dc6a7-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="dc6a7-140">Диалоговое окно " **Настройка учетных записей** " возвратил ошибку.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="dc6a7-141">Замечания</span><span class="sxs-lookup"><span data-stu-id="dc6a7-141">Remarks</span></span>

<span data-ttu-id="dc6a7-142">Параметры _cCategories_, _rgclsidCategories_и _pclsidType_ не используется в данный момент и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="dc6a7-143">_wszTitle_ не используется, а также должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="dc6a7-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

