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
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="204f7-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="204f7-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="204f7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="204f7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="204f7-105">Представляет диалоговое окно, которое позволяет пользователю выбрать контейнер формы и возвращает интерфейс для выбранного пользователем объекта контейнера.</span><span class="sxs-lookup"><span data-stu-id="204f7-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="204f7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="204f7-106">Parameters</span></span>

 <span data-ttu-id="204f7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="204f7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="204f7-108">[in] Handle to the parent window of the displayed dialog box.</span><span class="sxs-lookup"><span data-stu-id="204f7-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="204f7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="204f7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="204f7-110">[in] Битоваяmas флагов, которая управляет тем, как выбирается библиотека форм (то есть как выбирается контейнер формы).</span><span class="sxs-lookup"><span data-stu-id="204f7-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="204f7-111">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="204f7-111">The following flags can be set:</span></span>
    
<span data-ttu-id="204f7-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="204f7-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="204f7-113">Выбор можно сделать из всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="204f7-113">Selection can be made from all containers.</span></span> <span data-ttu-id="204f7-114">Это тип выбора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="204f7-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="204f7-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="204f7-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="204f7-116">Выбор можно сделать только из контейнеров папок.</span><span class="sxs-lookup"><span data-stu-id="204f7-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="204f7-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="204f7-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="204f7-118">Выбор можно сделать только из контейнеров, не связанных с папками.</span><span class="sxs-lookup"><span data-stu-id="204f7-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="204f7-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="204f7-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="204f7-120">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="204f7-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="204f7-121">Этот интерфейс для объекта контейнера, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="204f7-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="204f7-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="204f7-122">Return value</span></span>

<span data-ttu-id="204f7-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="204f7-123">S_OK</span></span> 
  
> <span data-ttu-id="204f7-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="204f7-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="204f7-125">Примечания</span><span class="sxs-lookup"><span data-stu-id="204f7-125">Remarks</span></span>

<span data-ttu-id="204f7-126">Как правило, для выбора контейнера формы, в который устанавливается форма, необходимо вызвать метод **IMAPIFormMgr::SelectFormContainer.**</span><span class="sxs-lookup"><span data-stu-id="204f7-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="204f7-127">**SelectFormContainer** нельзя использовать для выбора локального контейнера формы со значением HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="204f7-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="204f7-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="204f7-128">MFCMAPI reference</span></span>

<span data-ttu-id="204f7-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="204f7-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="204f7-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="204f7-130">**File**</span></span>|<span data-ttu-id="204f7-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="204f7-131">**Function**</span></span>|<span data-ttu-id="204f7-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="204f7-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="204f7-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="204f7-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="204f7-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="204f7-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="204f7-135">MFCMAPI использует метод **IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отрисовки его содержимого.</span><span class="sxs-lookup"><span data-stu-id="204f7-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="204f7-136">См. также</span><span class="sxs-lookup"><span data-stu-id="204f7-136">See also</span></span>



[<span data-ttu-id="204f7-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="204f7-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="204f7-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="204f7-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

