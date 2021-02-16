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
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="0c95c-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="0c95c-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="0c95c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0c95c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0c95c-105">Открывает форму для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="0c95c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0c95c-106">Parameters</span></span>

 <span data-ttu-id="0c95c-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="0c95c-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0c95c-108">[in] Handle to the parent window for the progress indicator that is displayed while the form is opened.</span><span class="sxs-lookup"><span data-stu-id="0c95c-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="0c95c-109">Параметр _ulUIParam_ игнорируется, если MAPI_DIALOG флага в параметре _ulFlags._</span><span class="sxs-lookup"><span data-stu-id="0c95c-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="0c95c-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0c95c-110">_ulFlags_</span></span>
  
> <span data-ttu-id="0c95c-111">[in] Битоваяmas флагов, которая управляет открытием формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="0c95c-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0c95c-112">The following flag can be set:</span></span>
    
<span data-ttu-id="0c95c-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="0c95c-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="0c95c-114">Отображает пользовательский интерфейс для предоставления состояния или запроса дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="0c95c-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="0c95c-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="0c95c-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="0c95c-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="0c95c-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="0c95c-117">[in] Указатель на информационный объект формы, используемый для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="0c95c-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="0c95c-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="0c95c-119">[in] Указатель на идентификатор интерфейса для интерфейса, возвращаемой для созданного объекта формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="0c95c-120">Параметр  _refiidToAsk_ не должен иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="0c95c-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="0c95c-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="0c95c-121">_ppvObj_</span></span>
  
> <span data-ttu-id="0c95c-122">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="0c95c-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0c95c-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0c95c-123">Return value</span></span>

<span data-ttu-id="0c95c-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0c95c-124">S_OK</span></span> 
  
> <span data-ttu-id="0c95c-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0c95c-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0c95c-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="0c95c-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="0c95c-127">Запрашиваемая интерфейс не поддерживается объектом формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="0c95c-128">Примечания</span><span class="sxs-lookup"><span data-stu-id="0c95c-128">Remarks</span></span>

<span data-ttu-id="0c95c-129">Посетители форм звонят **методу IMAPIFormMgr::CreateForm,** чтобы открыть форму для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="0c95c-130">**CreateForm** открывает форму, создавая экземпляр сервера форм для этой формы, как описано в данном объекте сведений формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="0c95c-131">При необходимости **CreateForm** вызывает метод [IMAPIFormMgr::P repareForm](imapiformmgr-prepareform.md) для загрузки кода сервера формы на диск пользователя.</span><span class="sxs-lookup"><span data-stu-id="0c95c-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="0c95c-132">Параметр  _pfrminfoToActivate должен_ указать на объект сведений о форме, который был правильно разрешен.</span><span class="sxs-lookup"><span data-stu-id="0c95c-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="0c95c-133">После открытия формы вызываемая форма должна настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и при желании настроить контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="0c95c-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="0c95c-134">Дополнительные сведения см. [в теме "Запуск сервера форм".](launching-a-form-server.md)</span><span class="sxs-lookup"><span data-stu-id="0c95c-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0c95c-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0c95c-135">MFCMAPI reference</span></span>

<span data-ttu-id="0c95c-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0c95c-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0c95c-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0c95c-137">**File**</span></span>|<span data-ttu-id="0c95c-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0c95c-138">**Function**</span></span>|<span data-ttu-id="0c95c-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0c95c-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0c95c-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="0c95c-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="0c95c-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="0c95c-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="0c95c-142">MFCMAPI использует метод **IMAPIFormMgr::CreateForm** для создания формы перед ее отображением.</span><span class="sxs-lookup"><span data-stu-id="0c95c-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0c95c-143">См. также</span><span class="sxs-lookup"><span data-stu-id="0c95c-143">See also</span></span>



[<span data-ttu-id="0c95c-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="0c95c-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="0c95c-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c95c-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="0c95c-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0c95c-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="0c95c-147">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="0c95c-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="0c95c-148">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="0c95c-148">Launching a Form Server</span></span>](launching-a-form-server.md)

