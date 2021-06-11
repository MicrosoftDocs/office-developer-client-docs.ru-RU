---
title: IMAPIFormMgrSelectFormContainer
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFolder.CopyMessages
api_type:
- COM
ms.assetid: c33daad6-52c4-4968-ac56-415178c9bf12
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: bfddc24e6a9c7cf8bdeae1e5ea730ecdb116f564
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33428594"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="5b9e3-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="5b9e3-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="5b9e3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5b9e3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5b9e3-105">Представляет диалоговое окно, которое позволяет пользователю выбрать контейнер формы и возвращает интерфейс для выбранного пользователем объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="5b9e3-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5b9e3-106">Parameters</span></span>

 <span data-ttu-id="5b9e3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="5b9e3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="5b9e3-108">[in] Ручка родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="5b9e3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5b9e3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="5b9e3-110">[in] Битмаска флагов, которая управляет тем, как выбирается библиотека форм (то есть, как выбирается контейнер формы).</span><span class="sxs-lookup"><span data-stu-id="5b9e3-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="5b9e3-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="5b9e3-111">The following flags can be set:</span></span>
    
<span data-ttu-id="5b9e3-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="5b9e3-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="5b9e3-113">Выбор можно сделать из всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-113">Selection can be made from all containers.</span></span> <span data-ttu-id="5b9e3-114">Это тип выбора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="5b9e3-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="5b9e3-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="5b9e3-116">Выбор можно сделать только из контейнеров папок.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="5b9e3-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="5b9e3-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="5b9e3-118">Выбор может быть выполнен только из контейнеров, не связанных с папками.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="5b9e3-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="5b9e3-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="5b9e3-120">[вышел] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="5b9e3-121">Этот интерфейс для объекта контейнера, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5b9e3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5b9e3-122">Return value</span></span>

<span data-ttu-id="5b9e3-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="5b9e3-123">S_OK</span></span> 
  
> <span data-ttu-id="5b9e3-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="5b9e3-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="5b9e3-125">Remarks</span></span>

<span data-ttu-id="5b9e3-126">Как правило, зрители формы звонят по **методу IMAPIFormMgr::SelectFormContainer,** чтобы выбрать контейнер формы, в который установлена форма.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="5b9e3-127">**SelectFormContainer** нельзя использовать для выбора локального контейнера форм, который имеет значение HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="5b9e3-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5b9e3-128">MFCMAPI reference</span></span>

<span data-ttu-id="5b9e3-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5b9e3-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5b9e3-130">**File**</span></span>|<span data-ttu-id="5b9e3-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5b9e3-131">**Function**</span></span>|<span data-ttu-id="5b9e3-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5b9e3-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5b9e3-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5b9e3-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="5b9e3-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="5b9e3-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="5b9e3-135">MFCMAPI использует **метод IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отрисовка его содержимого.</span><span class="sxs-lookup"><span data-stu-id="5b9e3-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5b9e3-136">См. также</span><span class="sxs-lookup"><span data-stu-id="5b9e3-136">See also</span></span>



[<span data-ttu-id="5b9e3-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5b9e3-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="5b9e3-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5b9e3-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

