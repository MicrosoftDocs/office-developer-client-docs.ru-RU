---
title: Иолкаккаунтманажердисплайаккаунтлист
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
# <a name="iolkaccountmanagerdisplayaccountlist"></a><span data-ttu-id="4d6ad-103">IOlkAccountManager::DisplayAccountList</span><span class="sxs-lookup"><span data-stu-id="4d6ad-103">IOlkAccountManager::DisplayAccountList</span></span>

<span data-ttu-id="4d6ad-104">Отображает диалоговое окно " **Параметры учетНой записи** " или " **Добавление новой учетной записи** ".</span><span class="sxs-lookup"><span data-stu-id="4d6ad-104">Displays either the **Account Settings** or **Add New Account** dialog box.</span></span> 
  
## <a name="quick-info"></a><span data-ttu-id="4d6ad-105">Краткие сведения</span><span class="sxs-lookup"><span data-stu-id="4d6ad-105">Quick info</span></span>

<span data-ttu-id="4d6ad-106">See [IOlkAccountManager](iolkaccountmanager.md).</span><span class="sxs-lookup"><span data-stu-id="4d6ad-106">See [IOlkAccountManager](iolkaccountmanager.md).</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="4d6ad-107">Параметры</span><span class="sxs-lookup"><span data-stu-id="4d6ad-107">Parameters</span></span>

<span data-ttu-id="4d6ad-108">_hwnd_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-108">_hwnd_</span></span>
  
> <span data-ttu-id="4d6ad-109">возврата Дескриптор окна, в котором отображается модальное диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-109">[in] The handle to the window to which the displayed dialog box is modal.</span></span> <span data-ttu-id="4d6ad-110">Может равняться нулю.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-110">May be zero.</span></span>
    
<span data-ttu-id="4d6ad-111">_dwFlags_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-111">_dwFlags_</span></span>
  
> <span data-ttu-id="4d6ad-112">возврата Флаги для изменения поведения отображения.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-112">[in] Flags to modify the behavior of the display.</span></span> 
    
   - <span data-ttu-id="4d6ad-113">**Акктуи_но_варнинг**— не отображать предупреждение о том, что изменения вступят в силу только после перезапуска Outlook.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-113">**ACCTUI_NO_WARNING**—Do not display the warning that changes will not take effect until Outlook is restarted.</span></span> <span data-ttu-id="4d6ad-114">Применяется только в том случае, если приложение выполняется в процессе работы с Outlook. exe.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-114">Applies only if the application is running in-process with Outlook.exe.</span></span>
    
   - <span data-ttu-id="4d6ad-115">**Акктуи_шов_дата_таб**— отображение диалогового окна " **Параметры учетной записи** " с выбранной вкладкой " **данные** ".</span><span class="sxs-lookup"><span data-stu-id="4d6ad-115">**ACCTUI_SHOW_DATA_TAB**—Show the **Account Settings** dialog box with the **Data** tab selected.</span></span> <span data-ttu-id="4d6ad-116">Допустимо, только если не задано значение **акктуи_шов_акктвизард** .</span><span class="sxs-lookup"><span data-stu-id="4d6ad-116">Valid only if **ACCTUI_SHOW_ACCTWIZARD** is not set.</span></span> 
    
   - <span data-ttu-id="4d6ad-117">**Акктуи_шов_акктвизард**— отображение диалогового окна " **Добавление новой учетной записи** ".</span><span class="sxs-lookup"><span data-stu-id="4d6ad-117">**ACCTUI_SHOW_ACCTWIZARD**—Display the **Add New Account** dialog box.</span></span> 
    
<span data-ttu-id="4d6ad-118">_Всзтитле_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-118">_wszTitle_</span></span>
  
> <span data-ttu-id="4d6ad-119">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-119">[in] This parameter is not used and should be NULL.</span></span>
    
<span data-ttu-id="4d6ad-120">_Ккатегориес_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-120">_cCategories_</span></span>
  
> <span data-ttu-id="4d6ad-121">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-121">[in] This parameter is not used and must be NULL.</span></span> 
    
<span data-ttu-id="4d6ad-122">_Ргклсидкатегориес_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-122">_rgclsidCategories_</span></span>
  
> <span data-ttu-id="4d6ad-123">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-123">[in] This parameter is not used and must be NULL.</span></span>
    
<span data-ttu-id="4d6ad-124">_Пклсидтипе_</span><span class="sxs-lookup"><span data-stu-id="4d6ad-124">_pclsidType_</span></span>
  
> <span data-ttu-id="4d6ad-125">возврата Этот параметр не используется и должен иметь значение NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-125">[in] This parameter is not used and must be NULL.</span></span>
    
## <a name="return-values"></a><span data-ttu-id="4d6ad-126">Возвращаемые значения</span><span class="sxs-lookup"><span data-stu-id="4d6ad-126">Return values</span></span>

|<span data-ttu-id="4d6ad-127">**HRESULT**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-127">**HRESULT**</span></span>|<span data-ttu-id="4d6ad-128">**Description**</span><span class="sxs-lookup"><span data-stu-id="4d6ad-128">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="4d6ad-129">S_OK</span><span class="sxs-lookup"><span data-stu-id="4d6ad-129">S_OK</span></span>  <br/> |<span data-ttu-id="4d6ad-130">Вызов выполнен успешно.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-130">The call was successful.</span></span>  <br/> |
|<span data-ttu-id="4d6ad-131">Е_АККТ_УИ_БУСИ</span><span class="sxs-lookup"><span data-stu-id="4d6ad-131">E_ACCT_UI_BUSY</span></span>  <br/> |<span data-ttu-id="4d6ad-132">Не удается создать диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-132">The dialog box could not be created.</span></span>  <br/> |
|<span data-ttu-id="4d6ad-133">Е_ОЛК_НОТ_ИНИТИАЛИЗЕД</span><span class="sxs-lookup"><span data-stu-id="4d6ad-133">E_OLK_NOT_INITIALIZED</span></span>  <br/> |<span data-ttu-id="4d6ad-134">The account manager has not been initialized for use.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-134">The account manager has not been initialized for use.</span></span>  <br/> |
|<span data-ttu-id="4d6ad-135">МАПИ_Е_КАЛЛ_ФАИЛЕД</span><span class="sxs-lookup"><span data-stu-id="4d6ad-135">MAPI_E_CALL_FAILED</span></span>  <br/> |<span data-ttu-id="4d6ad-136">Диалоговое окно " **Добавление новой учетНой записи** " вернуло ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-136">The **Add New Account** dialog box returned an error.</span></span>  <br/> |
|<span data-ttu-id="4d6ad-137">МАПИ_Е_ИНВАЛИД_ПАРАМЕТЕР</span><span class="sxs-lookup"><span data-stu-id="4d6ad-137">MAPI_E_INVALID_PARAMETER</span></span>  <br/> |<span data-ttu-id="4d6ad-138">Параметр _ккатегориес_, _ргклсидкатегориес_или _пклсидтипе_ имеет значение, отличное от NULL.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-138">The  _cCategories_,  _rgclsidCategories_, or  _pclsidType_ parameter is non-NULL.</span></span>  <br/> |
|<span data-ttu-id="4d6ad-139">МАПИ_Е_УСЕР_КАНЦЕЛ</span><span class="sxs-lookup"><span data-stu-id="4d6ad-139">MAPI_E_USER_CANCEL</span></span>  <br/> |<span data-ttu-id="4d6ad-140">Диалоговое окно " **Параметры учетНой записи** " возвратило ошибку.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-140">The **Account Settings** dialog box returned an error.</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="4d6ad-141">Примечания</span><span class="sxs-lookup"><span data-stu-id="4d6ad-141">Remarks</span></span>

<span data-ttu-id="4d6ad-142">Параметры _ккатегориес_, _ргклсидкатегориес_и _пклсидтипе_ не используются в данный момент и должны иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-142">The  _cCategories_,  _rgclsidCategories_, and  _pclsidType_ parameters are not used at this time and must be NULL.</span></span>  <span data-ttu-id="4d6ad-143">_всзтитле_ не используется, и он также должен иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="4d6ad-143">_wszTitle_ is not used and should also be NULL.</span></span> 
  

