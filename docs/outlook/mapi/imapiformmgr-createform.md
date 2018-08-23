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
ms.openlocfilehash: e86c3d9678739c09024c0655cbbbb702749a53f0
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22586167"
---
# <a name="imapiformmgrcreateform"></a><span data-ttu-id="b285e-103">IMAPIFormMgr::CreateForm</span><span class="sxs-lookup"><span data-stu-id="b285e-103">IMAPIFormMgr::CreateForm</span></span>

  
  
<span data-ttu-id="b285e-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b285e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b285e-105">Открывает форму для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-105">Opens a form to create a new message based on the form's message class.</span></span>
  
```cpp
HRESULT CreateForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  IMAPIFormInfo pfrminfoToActivate,
  REFIID refiidToAsk,
  LPVOID FAR * ppvObj
);
```

## <a name="parameters"></a><span data-ttu-id="b285e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b285e-106">Parameters</span></span>

 <span data-ttu-id="b285e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="b285e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="b285e-108">[in] Дескриптор родительского окна для индикатора, отображаемое при открытии формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-108">[in] A handle to the parent window for the progress indicator that is displayed while the form is opened.</span></span> <span data-ttu-id="b285e-109">Параметр _ulUIParam_ игнорируется, пока флаг MAPI_DIALOG будет выполнен с помощью параметра _ulFlags_ .</span><span class="sxs-lookup"><span data-stu-id="b285e-109">The  _ulUIParam_ parameter is ignored unless the MAPI_DIALOG flag is set in the  _ulFlags_ parameter.</span></span> 
    
 <span data-ttu-id="b285e-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b285e-110">_ulFlags_</span></span>
  
> <span data-ttu-id="b285e-111">[in] Битовая маска флаги, который определяет, как форма будет открыта.</span><span class="sxs-lookup"><span data-stu-id="b285e-111">[in] A bitmask of flags that controls how the form is opened.</span></span> <span data-ttu-id="b285e-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="b285e-112">The following flag can be set:</span></span>
    
<span data-ttu-id="b285e-113">MAPI_DIALOG</span><span class="sxs-lookup"><span data-stu-id="b285e-113">MAPI_DIALOG</span></span> 
  
> <span data-ttu-id="b285e-114">Отображает пользовательский интерфейс для предоставления состояния или запрашивать у пользователя для получения дополнительных сведений.</span><span class="sxs-lookup"><span data-stu-id="b285e-114">Displays a user interface to provide status or prompt the user for more information.</span></span> <span data-ttu-id="b285e-115">Если этот флаг не установлен, пользовательский интерфейс не отображается.</span><span class="sxs-lookup"><span data-stu-id="b285e-115">If this flag is not set, no user interface is displayed.</span></span>
    
 <span data-ttu-id="b285e-116">_pfrminfoToActivate_</span><span class="sxs-lookup"><span data-stu-id="b285e-116">_pfrminfoToActivate_</span></span>
  
> <span data-ttu-id="b285e-117">[in] Указатель на объект данные формы, который используется для открытия формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-117">[in] A pointer to the form information object that is used to open the form.</span></span>
    
 <span data-ttu-id="b285e-118">_refiidToAsk_</span><span class="sxs-lookup"><span data-stu-id="b285e-118">_refiidToAsk_</span></span>
  
> <span data-ttu-id="b285e-119">[in] Указатель интерфейса должно быть возвращено для объекта формы, которая была создана с идентификатором интерфейса (ИД интерфейса).</span><span class="sxs-lookup"><span data-stu-id="b285e-119">[in] A pointer to the interface identifier (IID) for the interface to be returned for the form object that was created.</span></span> <span data-ttu-id="b285e-120">Параметр _refiidToAsk_ не должна быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b285e-120">The  _refiidToAsk_ parameter must not be NULL.</span></span> 
    
 <span data-ttu-id="b285e-121">_ppvObj_</span><span class="sxs-lookup"><span data-stu-id="b285e-121">_ppvObj_</span></span>
  
> <span data-ttu-id="b285e-122">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="b285e-122">[out] A pointer to a pointer to the returned interface.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b285e-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b285e-123">Return value</span></span>

<span data-ttu-id="b285e-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b285e-124">S_OK</span></span> 
  
> <span data-ttu-id="b285e-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="b285e-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="b285e-126">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="b285e-126">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="b285e-127">Запрошенный интерфейс не поддерживается объектом формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-127">The requested interface is not supported by the form object.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b285e-128">Замечания</span><span class="sxs-lookup"><span data-stu-id="b285e-128">Remarks</span></span>

<span data-ttu-id="b285e-129">Средства просмотра форм вызовите метод **IMAPIFormMgr::CreateForm** для открытия формы для создания нового сообщения на основе класса сообщения формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-129">Form viewers call the **IMAPIFormMgr::CreateForm** method to open a form to create a new message based on the form's message class.</span></span> <span data-ttu-id="b285e-130">**CreateForm** открывает форму путем создания экземпляра сервера форм для этой формы, как описано в объекте данные указанной формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-130">**CreateForm** opens the form by creating an instance of the form server for that form as described in the given form information object.</span></span> <span data-ttu-id="b285e-131">При необходимости **CreateForm** вызывает метод [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) , чтобы загрузить серверного кода формы диск компьютера пользователя.</span><span class="sxs-lookup"><span data-stu-id="b285e-131">If required, **CreateForm** calls the [IMAPIFormMgr::PrepareForm](imapiformmgr-prepareform.md) method to download the form server code to the user's disk.</span></span> 
  
<span data-ttu-id="b285e-132">Параметр _pfrminfoToActivate_ должен указывать на объект данные формы, правильно разрешены.</span><span class="sxs-lookup"><span data-stu-id="b285e-132">The  _pfrminfoToActivate_ parameter must point to a form information object that has been correctly resolved.</span></span> 
  
<span data-ttu-id="b285e-133">После открытия формы, вызывающий средство просмотра формы необходимо настроить сообщение с помощью интерфейса [IPersistMessage](ipersistmessageiunknown.md) и при необходимости можно настроить контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="b285e-133">After the form has been opened, the calling form viewer must set up a message by using the [IPersistMessage](ipersistmessageiunknown.md) interface and can optionally set up a view context for the form.</span></span> <span data-ttu-id="b285e-134">Для получения дополнительных сведений см [запуска сервера формы](launching-a-form-server.md).</span><span class="sxs-lookup"><span data-stu-id="b285e-134">For more information, see [Launching a Form Server](launching-a-form-server.md).</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="b285e-135">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="b285e-135">MFCMAPI reference</span></span>

<span data-ttu-id="b285e-136">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="b285e-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="b285e-137">**����**</span><span class="sxs-lookup"><span data-stu-id="b285e-137">**File**</span></span>|<span data-ttu-id="b285e-138">**�������**</span><span class="sxs-lookup"><span data-stu-id="b285e-138">**Function**</span></span>|<span data-ttu-id="b285e-139">**�����������**</span><span class="sxs-lookup"><span data-stu-id="b285e-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="b285e-140">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="b285e-140">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="b285e-141">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="b285e-141">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="b285e-142">Mfcmapi (en) использует метод **IMAPIFormMgr::CreateForm** для создания формы перед их отображением.</span><span class="sxs-lookup"><span data-stu-id="b285e-142">MFCMAPI uses the **IMAPIFormMgr::CreateForm** method to create a form before displaying it.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="b285e-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b285e-143">See also</span></span>



[<span data-ttu-id="b285e-144">IMAPIFormMgr::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="b285e-144">IMAPIFormMgr::PrepareForm</span></span>](imapiformmgr-prepareform.md)
  
[<span data-ttu-id="b285e-145">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b285e-145">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="b285e-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="b285e-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="b285e-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="b285e-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="b285e-148">Запуск сервера форм</span><span class="sxs-lookup"><span data-stu-id="b285e-148">Launching a Form Server</span></span>](launching-a-form-server.md)

