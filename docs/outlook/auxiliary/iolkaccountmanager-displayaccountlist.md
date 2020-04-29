---
title: иолкаккаунтманажердисплайаккаунтлист
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
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="bf162-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="bf162-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="bf162-104">Отображает диалоговое окно " **Параметры учетной записи** " или " **Добавление новой учетной записи** ".</span><span class="sxs-lookup"><span data-stu-id="bf162-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="bf162-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="bf162-105">Quick info</span></span>

<span data-ttu-id="bf162-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="bf162-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="bf162-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="bf162-107">Parameters</span></span>

<span data-ttu-id="bf162-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="bf162-108">_hwnd_</span></span>
  
> <span data-ttu-id="bf162-109">возврата Дескриптор окна, в котором отображается модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bf162-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="bf162-110">Может равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="bf162-110">May be zero.</span></span>
    
<span data-ttu-id="bf162-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="bf162-111">_dwFlags_</span></span>
  
> <span data-ttu-id="bf162-112">возврата Флаги для изменения поведения отображения.</span><span class="sxs-lookup"><span data-stu-id="bf162-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="bf162-113">**ACCTUI_NO_WARNING**не отображать предупреждение о том, что изменения вступят в силу только после перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="bf162-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="bf162-114">Применяется только в том случае, если приложение выполняется в процессе работы с Outlook. exe.</span><span class="sxs-lookup"><span data-stu-id="bf162-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="bf162-115">**ACCTUI_SHOW_DATA_TAB**— отображение диалогового окна " **Параметры учетной записи** " с выбранной вкладкой " **данные** ".</span><span class="sxs-lookup"><span data-stu-id="bf162-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="bf162-116">Допустимо, только если не задано значение **ACCTUI_SHOW_ACCTWIZARD** .</span><span class="sxs-lookup"><span data-stu-id="bf162-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="bf162-117">**ACCTUI_SHOW_ACCTWIZARD**— отображение диалогового окна " **Добавление новой учетной записи** ".</span><span class="sxs-lookup"><span data-stu-id="bf162-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="bf162-118">_всзтитле_</span><span class="sxs-lookup"><span data-stu-id="bf162-118">_wszTitle_</span></span>
  
> <span data-ttu-id="bf162-119">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bf162-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="bf162-120">_ккатегориес_</span><span class="sxs-lookup"><span data-stu-id="bf162-120">_cCategories_</span></span>
  
> <span data-ttu-id="bf162-121">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bf162-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="bf162-122">_ргклсидкатегориес_</span><span class="sxs-lookup"><span data-stu-id="bf162-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="bf162-123">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bf162-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="bf162-124">_пклсидтипе_</span><span class="sxs-lookup"><span data-stu-id="bf162-124">_pclsidType_</span></span>
  
> <span data-ttu-id="bf162-125">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="bf162-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="bf162-126">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="bf162-126">Return values</span></span>

|<span data-ttu-id="bf162-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="bf162-127">**HRESULT**</span></span>|<span data-ttu-id="bf162-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="bf162-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="bf162-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="bf162-129">S_OK</span></span>  <br/> |<span data-ttu-id="bf162-130">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="bf162-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="bf162-131">E_ACCT_UI_BUSY</span><span class="sxs-lookup"><span data-stu-id="bf162-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="bf162-132">Не удается создать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="bf162-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="bf162-133">E_OLK_NOT_INITIALIZED</span><span class="sxs-lookup"><span data-stu-id="bf162-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="bf162-134">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="bf162-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="bf162-135">MAPI_E_CALL_FAILED</span><span class="sxs-lookup"><span data-stu-id="bf162-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="bf162-136">Диалоговое окно " **Добавление новой учетной записи** " вернуло ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf162-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="bf162-137">MAPI_E_INVALID_PARAMETER</span><span class="sxs-lookup"><span data-stu-id="bf162-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="bf162-138">Параметр _ккатегориес_, _ргклсидкатегориес_или _пклсидтипе_ имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="bf162-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="bf162-139">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="bf162-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="bf162-140">Диалоговое окно " **Параметры учетной записи** " возвратило ошибку.</span><span class="sxs-lookup"><span data-stu-id="bf162-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="bf162-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="bf162-141">Remarks</span></span>

<span data-ttu-id="bf162-142">Параметры _ккатегориес_, _ргклсидкатегориес_и _пклсидтипе_ не используются в данный момент и должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="bf162-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="bf162-143">_всзтитле_ не используется, и он также должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="bf162-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

