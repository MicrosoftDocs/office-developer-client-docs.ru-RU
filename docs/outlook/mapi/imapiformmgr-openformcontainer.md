---
title: IMAPIFormMgrOpenFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.OpenFormContainer
api_type:
- COM
ms.assetid: df02bdc5-903a-4ce2-9f43-5f4513ea19b3
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 64031725e06a949464e7bfabb0a2f114d325470e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808936"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="6b621-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b621-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="6b621-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6b621-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="6b621-105">Откроется интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для контейнера конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="6b621-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6b621-106">Parameters</span></span>

 <span data-ttu-id="6b621-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="6b621-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="6b621-108">[in] Перечисление HFRMREG, которое указывает, библиотека форм, чтобы открыть (то есть, формы контейнер, чтобы открыть).</span><span class="sxs-lookup"><span data-stu-id="6b621-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="6b621-109">Перечисление HFRMREG является перечислением, характерные для поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="6b621-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="6b621-110">Возможные значения HFRMREG относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="6b621-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="6b621-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="6b621-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="6b621-112">Контейнер удобное формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-112">A convenient form container.</span></span>
    
<span data-ttu-id="6b621-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="6b621-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="6b621-114">Контейнер папки.</span><span class="sxs-lookup"><span data-stu-id="6b621-114">A folder container.</span></span> 
    
<span data-ttu-id="6b621-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="6b621-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="6b621-116">Контейнер для хранения сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="6b621-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="6b621-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="6b621-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="6b621-118">Контейнер локального формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-118">A local form container.</span></span> 
    
 <span data-ttu-id="6b621-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="6b621-119">_lpunk_</span></span>
  
> <span data-ttu-id="6b621-120">[in] Указатель на объект, для которого открывается интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6b621-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="6b621-121">Параметр _lpunk_ должен быть **значение null** , если значение параметра _hfrmreg_ не требует указателя на объект.</span><span class="sxs-lookup"><span data-stu-id="6b621-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="6b621-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="6b621-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="6b621-123">[out] Указатель на указатель на объект контейнера возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6b621-124">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="6b621-124">Return value</span></span>

<span data-ttu-id="6b621-125">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="6b621-125">S_OK</span></span> 
  
> <span data-ttu-id="6b621-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6b621-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6b621-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="6b621-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="6b621-128">Объект, на который указывает _lpunk_ не поддерживает необходимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="6b621-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="6b621-129">Замечания</span><span class="sxs-lookup"><span data-stu-id="6b621-129">Remarks</span></span>

<span data-ttu-id="6b621-130">Средства просмотра форм вызовите метод **IMAPIFormMgr::OpenFormContainer** для открытия **IMAPIFormContainer** интерфейс для контейнера конкретной формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="6b621-131">Затем этот интерфейс используется для установки в и удаление форм из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="6b621-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="6b621-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="6b621-132">Notes to callers</span></span>

<span data-ttu-id="6b621-133">Если значение в _hfrmreg_ HFRMREG_FOLDER, идентификатор интерфейса, используемый в _lpunk_ должно быть **значение null** и необходимо иметь возможность вызова метода [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) интерфейс [IMAPIFolder](imapifolderimapicontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="6b621-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](http://msdn.microsoft.com/en-us/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="6b621-134">Чтобы открыть контейнер локального формы, необходимо использовать вызов метода **OpenFormContainer** или функцию [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) . Чтобы разрешить пользователю выбрать контейнер локальной форме нельзя использовать метод [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) .</span><span class="sxs-lookup"><span data-stu-id="6b621-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6b621-135">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="6b621-135">MFCMAPI reference</span></span>

<span data-ttu-id="6b621-136">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="6b621-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6b621-137">**����**</span><span class="sxs-lookup"><span data-stu-id="6b621-137">**File**</span></span>|<span data-ttu-id="6b621-138">**�������**</span><span class="sxs-lookup"><span data-stu-id="6b621-138">**Function**</span></span>|<span data-ttu-id="6b621-139">**�����������**</span><span class="sxs-lookup"><span data-stu-id="6b621-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6b621-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6b621-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="6b621-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b621-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="6b621-142">Mfcmapi (en) использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнером формы, поэтому можно отобразить содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="6b621-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="6b621-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="6b621-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="6b621-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b621-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="6b621-145">Mfcmapi (en) использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнером формы для папки, поэтому можно отобразить содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="6b621-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6b621-146">См. также</span><span class="sxs-lookup"><span data-stu-id="6b621-146">See also</span></span>



[<span data-ttu-id="6b621-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="6b621-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="6b621-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b621-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="6b621-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="6b621-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="6b621-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6b621-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="6b621-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="6b621-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

