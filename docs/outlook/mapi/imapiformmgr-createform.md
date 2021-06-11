---
title: IMAPIFormMgrCreateForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.CreateForm
api_type:
- COM
ms.assetid: 7d4d50f8-3904-4e93-a535-ac7decceb1a3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c6e18ee9f8ea1d7dc6592d576c5a1163db526639
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419851"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="d35bb-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="d35bb-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="d35bb-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d35bb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d35bb-105">Открывает форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="d35bb-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="d35bb-106">Parameters</span></span>

 <span data-ttu-id="d35bb-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d35bb-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d35bb-108">[in] Ручка родительского окна для индикатора прогресса, отображаемого во время открытия формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="d35bb-109">Параметр _ulUIParam_ игнорируется, если флаг MAPI_DIALOG в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="d35bb-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="d35bb-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d35bb-110">_ulFlags_</span></span>
  
> <span data-ttu-id="d35bb-111">[in] Битмаски флагов, которые контролируют, как форма открывается.</span><span class="sxs-lookup"><span data-stu-id="d35bb-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="d35bb-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d35bb-112">The following flag can be set:</span></span>
    
<span data-ttu-id="d35bb-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="d35bb-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="d35bb-114">Отображает пользовательский интерфейс для предоставления статуса или запроса дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="d35bb-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="d35bb-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="d35bb-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="d35bb-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="d35bb-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="d35bb-117">[in] Указатель на информационный объект формы, используемый для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="d35bb-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="d35bb-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="d35bb-119">[in] Указатель на идентификатор интерфейса (IID) для возврата интерфейса для созданного объекта формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="d35bb-120">Параметр  _refiidToAsk_ не должен быть NULL.</span><span class="sxs-lookup"><span data-stu-id="d35bb-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="d35bb-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="d35bb-121">_ppvObj_</span></span>
  
> <span data-ttu-id="d35bb-122">[вышел] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d35bb-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d35bb-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d35bb-123">Return value</span></span>

<span data-ttu-id="d35bb-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="d35bb-124">S_OK</span></span> 
  
> <span data-ttu-id="d35bb-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d35bb-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="d35bb-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="d35bb-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="d35bb-127">Запрашиваемая интерфейсная форма не поддерживается объектом формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d35bb-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="d35bb-128">Remarks</span></span>

<span data-ttu-id="d35bb-129">Зрители формы звонят по методу **IMAPIFormMgr::CreateForm,** чтобы открыть форму для создания нового сообщения на основе класса сообщений формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="d35bb-130">**CreateForm** открывает форму, создавая экземпляр сервера формы для этой формы, как описано в данном информационном объекте формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="d35bb-131">При необходимости **CreateForm** вызывает [метод IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) для загрузки кода сервера форм на диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="d35bb-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="d35bb-132">Параметр  _pfrminfoToActivate должен_ указать на объект информационной формы, который был правильно разрешен.</span><span class="sxs-lookup"><span data-stu-id="d35bb-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="d35bb-133">После открытия формы зритель формы вызова должен настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и может дополнительно настроить контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="d35bb-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="d35bb-134">Дополнительные сведения см. в [дополнительных сведениях о запуске сервера форм.](launching-a-form-server.md)</span><span class="sxs-lookup"><span data-stu-id="d35bb-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d35bb-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d35bb-135">MFCMAPI reference</span></span>

<span data-ttu-id="d35bb-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d35bb-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d35bb-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d35bb-137">**File**</span></span>|<span data-ttu-id="d35bb-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d35bb-138">**Function**</span></span>|<span data-ttu-id="d35bb-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d35bb-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d35bb-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="d35bb-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="d35bb-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="d35bb-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="d35bb-142">MFCMAPI использует **метод IMAPIFormMgr::CreateForm** для создания формы перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="d35bb-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d35bb-143">См. также</span><span class="sxs-lookup"><span data-stu-id="d35bb-143">See also</span></span>



[<span data-ttu-id="d35bb-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="d35bb-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="d35bb-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d35bb-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="d35bb-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d35bb-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="d35bb-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="d35bb-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="d35bb-148">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="d35bb-148">Launching a Form Server</span></span>](launching-a-form-server.md)

