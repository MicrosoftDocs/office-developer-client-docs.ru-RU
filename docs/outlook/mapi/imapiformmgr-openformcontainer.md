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
ms.openlocfilehash: 68a358c91e35c5a075e220794c78f4e5c96e43ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321639"
---
# <a name="imapiformmgropenformcontainer"></a><span data-ttu-id="87991-103">IMAPIFormMgr::OpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="87991-103">IMAPIFormMgr::OpenFormContainer</span></span>

  
  
<span data-ttu-id="87991-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="87991-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="87991-105">Открывает интерфейс [IMAPIFormContainer](imapiformcontaineriunknown.md) для определенного контейнера форм.</span><span class="sxs-lookup"><span data-stu-id="87991-105">Opens an [IMAPIFormContainer](imapiformcontaineriunknown.md) interface for a specific form container.</span></span> 
  
```cpp
HRESULT OpenFormContainer(
  HFRMREG hfrmreg,
  LPUNKNOWN lpunk,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="87991-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="87991-106">Parameters</span></span>

 <span data-ttu-id="87991-107">_hfrmreg_</span><span class="sxs-lookup"><span data-stu-id="87991-107">_hfrmreg_</span></span>
  
> <span data-ttu-id="87991-108">[in] Перемерение HFRMREG, которое указывает на открытие библиотеки форм (то есть открыть контейнер формы).</span><span class="sxs-lookup"><span data-stu-id="87991-108">[in] An HFRMREG enumeration that indicates the form library to open (that is, the form container to open).</span></span> <span data-ttu-id="87991-109">Переименовка HFRMREG — это переумерия, специфичного для поставщика библиотеки форм.</span><span class="sxs-lookup"><span data-stu-id="87991-109">An HFRMREG enumeration is an enumeration that is specific to a form library provider.</span></span> <span data-ttu-id="87991-110">Возможные значения HFRMREG включают следующие:</span><span class="sxs-lookup"><span data-stu-id="87991-110">Possible HFRMREG values include the following:</span></span>
    
<span data-ttu-id="87991-111">HFRMREG_DEFAULT</span><span class="sxs-lookup"><span data-stu-id="87991-111">HFRMREG_DEFAULT</span></span> 
  
> <span data-ttu-id="87991-112">Удобный контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="87991-112">A convenient form container.</span></span>
    
<span data-ttu-id="87991-113">HFRMREG_FOLDER</span><span class="sxs-lookup"><span data-stu-id="87991-113">HFRMREG_FOLDER</span></span> 
  
> <span data-ttu-id="87991-114">Контейнер папок.</span><span class="sxs-lookup"><span data-stu-id="87991-114">A folder container.</span></span> 
    
<span data-ttu-id="87991-115">HFRMREG_PERSONAL</span><span class="sxs-lookup"><span data-stu-id="87991-115">HFRMREG_PERSONAL</span></span> 
  
> <span data-ttu-id="87991-116">Контейнер для магазина сообщений по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="87991-116">The container for the default message store.</span></span> 
    
<span data-ttu-id="87991-117">HFRMREG_LOCAL</span><span class="sxs-lookup"><span data-stu-id="87991-117">HFRMREG_LOCAL</span></span> 
  
> <span data-ttu-id="87991-118">Локальный контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="87991-118">A local form container.</span></span> 
    
 <span data-ttu-id="87991-119">_lpunk_</span><span class="sxs-lookup"><span data-stu-id="87991-119">_lpunk_</span></span>
  
> <span data-ttu-id="87991-120">[in] Указатель на объект, для которого открыт интерфейс.</span><span class="sxs-lookup"><span data-stu-id="87991-120">[in] A pointer to the object for which the interface is opened.</span></span> <span data-ttu-id="87991-121">Параметр  _lpunk_ должен быть **null,** если для  _параметра hfrmreg_ не требуется указатель объекта.</span><span class="sxs-lookup"><span data-stu-id="87991-121">The  _lpunk_ parameter must be **null** unless the value for the  _hfrmreg_ parameter requires an object pointer.</span></span> 
    
 <span data-ttu-id="87991-122">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="87991-122">_lppfcnt_</span></span>
  
> <span data-ttu-id="87991-123">[вышел] Указатель на указатель на объект контейнера возвращаемой формы.</span><span class="sxs-lookup"><span data-stu-id="87991-123">[out] A pointer to a pointer to the returned form container object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="87991-124">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="87991-124">Return value</span></span>

<span data-ttu-id="87991-125">S_OK</span><span class="sxs-lookup"><span data-stu-id="87991-125">S_OK</span></span> 
  
> <span data-ttu-id="87991-126">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="87991-126">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="87991-127">MAPI_E_NO_INTERFACE</span><span class="sxs-lookup"><span data-stu-id="87991-127">MAPI_E_NO_INTERFACE</span></span> 
  
> <span data-ttu-id="87991-128">Объект, на который указывает  _lpunk,_ не поддерживает необходимый интерфейс.</span><span class="sxs-lookup"><span data-stu-id="87991-128">The object pointed to by  _lpunk_ does not support the required interface.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="87991-129">Примечания</span><span class="sxs-lookup"><span data-stu-id="87991-129">Remarks</span></span>

<span data-ttu-id="87991-130">Зрители формы звонят по методу **IMAPIFormMgr::OpenFormContainer,** чтобы открыть **интерфейс IMAPIFormContainer** для определенного контейнера форм.</span><span class="sxs-lookup"><span data-stu-id="87991-130">Form viewers call the **IMAPIFormMgr::OpenFormContainer** method to open an **IMAPIFormContainer** interface for a specific form container.</span></span> <span data-ttu-id="87991-131">Затем этот интерфейс можно использовать для установки форм в контейнер формы и удаления их из контейнера форм.</span><span class="sxs-lookup"><span data-stu-id="87991-131">This interface can then be used for installing forms into and removing forms from a form container.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="87991-132">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="87991-132">Notes to callers</span></span>

<span data-ttu-id="87991-133">Если значение _в hfrmreg_ HFRMREG_FOLDER, идентификатор интерфейса, используемый в _lpunk,_ должен быть ненульным и должен позволять [методу IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) звонить в интерфейс [IMAPIFolder.](imapifolderimapicontainer.md) </span><span class="sxs-lookup"><span data-stu-id="87991-133">If the value in  _hfrmreg_ is HFRMREG_FOLDER, the interface identifier used in  _lpunk_ must be non- **null** and must allow [IUnknown::QueryInterface](https://msdn.microsoft.com/library/ms682521%28v=VS.85%29.aspx) method calls to an [IMAPIFolder](imapifolderimapicontainer.md) interface.</span></span> 
  
<span data-ttu-id="87991-134">Чтобы открыть локальный контейнер формы, необходимо использовать вызов метода **OpenFormContainer** или [функции MAPIOpenLocalFormContainer;](mapiopenlocalformcontainer.md) Вы не можете использовать [метод IMAPIFormMgr::SelectFormContainer,](imapiformmgr-selectformcontainer.md) чтобы позволить пользователю выбрать локальный контейнер формы.</span><span class="sxs-lookup"><span data-stu-id="87991-134">To open the local form container, you must use a call to **OpenFormContainer** method or the [MAPIOpenLocalFormContainer](mapiopenlocalformcontainer.md) function; you cannot use the [IMAPIFormMgr::SelectFormContainer](imapiformmgr-selectformcontainer.md) method to enable the user to select the local form container.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="87991-135">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="87991-135">MFCMAPI reference</span></span>

<span data-ttu-id="87991-136">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="87991-136">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="87991-137">**Файл**</span><span class="sxs-lookup"><span data-stu-id="87991-137">**File**</span></span>|<span data-ttu-id="87991-138">**Функция**</span><span class="sxs-lookup"><span data-stu-id="87991-138">**Function**</span></span>|<span data-ttu-id="87991-139">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="87991-139">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="87991-140">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="87991-140">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="87991-141">CMainDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="87991-141">CMainDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="87991-142">MFCMAPI использует **метод IMAPIFormMgr::OpenFormContainer** для получения контейнера формы, чтобы можно было отрисовывать содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="87991-142">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container so the container's contents can be rendered.</span></span>  <br/> |
|<span data-ttu-id="87991-143">MsgStoreDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="87991-143">MsgStoreDlg.cpp</span></span>  <br/> |<span data-ttu-id="87991-144">CMsgStoreDlg::OnOpenFormContainer</span><span class="sxs-lookup"><span data-stu-id="87991-144">CMsgStoreDlg::OnOpenFormContainer</span></span>  <br/> |<span data-ttu-id="87991-145">MFCMAPI использует метод **IMAPIFormMgr::OpenFormContainer** для получения контейнера формы для папки, чтобы можно было отрисовывать содержимое контейнера.</span><span class="sxs-lookup"><span data-stu-id="87991-145">MFCMAPI uses the **IMAPIFormMgr::OpenFormContainer** method to retrieve a form container for a folder so the container's contents can be rendered.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="87991-146">См. также</span><span class="sxs-lookup"><span data-stu-id="87991-146">See also</span></span>



[<span data-ttu-id="87991-147">IMAPIFormContainer::InstallForm</span><span class="sxs-lookup"><span data-stu-id="87991-147">IMAPIFormContainer::InstallForm</span></span>](imapiformcontainer-installform.md)
  
[<span data-ttu-id="87991-148">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="87991-148">IMAPIFormMgr::SelectFormContainer</span></span>](imapiformmgr-selectformcontainer.md)
  
[<span data-ttu-id="87991-149">MAPIOpenLocalFormContainer</span><span class="sxs-lookup"><span data-stu-id="87991-149">MAPIOpenLocalFormContainer</span></span>](mapiopenlocalformcontainer.md)
  
[<span data-ttu-id="87991-150">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="87991-150">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="87991-151">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="87991-151">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

