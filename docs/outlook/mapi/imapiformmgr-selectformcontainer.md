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
ms.openlocfilehash: ef9b99f06b62fd361bb780debb527ec2d7457589
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808968"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="bc0d3-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="bc0d3-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="bc0d3-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="bc0d3-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="bc0d3-105">Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="bc0d3-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="bc0d3-106">Parameters</span></span>

 <span data-ttu-id="bc0d3-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="bc0d3-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="bc0d3-108">[in] Дескриптор родительского окна, отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="bc0d3-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="bc0d3-109">_ulFlags_</span></span>
  
> <span data-ttu-id="bc0d3-110">[in] Битовая маска флагов, который определяет, как Выбор библиотеки форм (то есть, как контейнер формы установлен).</span><span class="sxs-lookup"><span data-stu-id="bc0d3-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="bc0d3-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="bc0d3-111">The following flags can be set:</span></span>
    
<span data-ttu-id="bc0d3-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="bc0d3-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="bc0d3-113">Выбор могут поступать из всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-113">Selection can be made from all containers.</span></span> <span data-ttu-id="bc0d3-114">Это тип выделения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="bc0d3-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="bc0d3-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="bc0d3-116">Выбор могут быть созданы только из папки контейнеров.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="bc0d3-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="bc0d3-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="bc0d3-118">Выбор могут быть созданы только из контейнеров, которые не связаны с папками.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="bc0d3-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="bc0d3-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="bc0d3-120">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="bc0d3-121">Этот интерфейс — объект-контейнер, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="bc0d3-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2">Return value</span></span>

<span data-ttu-id="bc0d3-123">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="bc0d3-123">S_OK</span></span> 
  
> <span data-ttu-id="bc0d3-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="bc0d3-125">���������</span><span class="sxs-lookup"><span data-stu-id="bc0d3-125">Remarks</span></span>

<span data-ttu-id="bc0d3-126">Средства просмотра формы обычно вызовите метод **IMAPIFormMgr::SelectFormContainer** для выбора формы контейнер, в котором установлен формы.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="bc0d3-127">**SelectFormContainer** не может использоваться для выбора контейнера локального формы, который имеет значение HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="bc0d3-128">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="bc0d3-128">MFCMAPI reference</span></span>

<span data-ttu-id="bc0d3-129">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="bc0d3-130">**����**</span><span class="sxs-lookup"><span data-stu-id="bc0d3-130">**File**</span></span>|<span data-ttu-id="bc0d3-131">**�������**</span><span class="sxs-lookup"><span data-stu-id="bc0d3-131">**Function**</span></span>|<span data-ttu-id="bc0d3-132">**�����������**</span><span class="sxs-lookup"><span data-stu-id="bc0d3-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="bc0d3-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="bc0d3-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="bc0d3-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="bc0d3-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="bc0d3-135">Mfcmapi (en) использует метод **IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отображением его содержимого.</span><span class="sxs-lookup"><span data-stu-id="bc0d3-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="bc0d3-136">См. также</span><span class="sxs-lookup"><span data-stu-id="bc0d3-136">See also</span></span>



[<span data-ttu-id="bc0d3-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="bc0d3-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="bc0d3-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="bc0d3-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

