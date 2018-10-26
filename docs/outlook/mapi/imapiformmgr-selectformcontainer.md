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
ms.openlocfilehash: f66d0fb1fc9d252ff8b6985c4a54de79313266d1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22577928"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="2de80-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="2de80-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="2de80-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2de80-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2de80-105">Отображает диалоговое окно, которое позволяет пользователю выбрать контейнер, формы и возвращает интерфейс для объекта контейнера выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="2de80-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="2de80-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2de80-106">Parameters</span></span>

 <span data-ttu-id="2de80-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="2de80-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="2de80-108">[in] Дескриптор родительского окна, отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="2de80-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="2de80-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2de80-109">_ulFlags_</span></span>
  
> <span data-ttu-id="2de80-110">[in] Битовая маска флагов, который определяет, как Выбор библиотеки форм (то есть, как контейнер формы установлен).</span><span class="sxs-lookup"><span data-stu-id="2de80-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="2de80-111">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="2de80-111">The following flags can be set:</span></span>
    
<span data-ttu-id="2de80-112">MAPIFORM_SELECT_ALL_REGISTRIES</span><span class="sxs-lookup"><span data-stu-id="2de80-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="2de80-113">Выбор могут поступать из всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2de80-113">Selection can be made from all containers.</span></span> <span data-ttu-id="2de80-114">Это тип выделения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="2de80-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="2de80-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="2de80-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="2de80-116">Выбор могут быть созданы только из папки контейнеров.</span><span class="sxs-lookup"><span data-stu-id="2de80-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="2de80-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span><span class="sxs-lookup"><span data-stu-id="2de80-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="2de80-118">Выбор могут быть созданы только из контейнеров, которые не связаны с папками.</span><span class="sxs-lookup"><span data-stu-id="2de80-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="2de80-119">_lppfcnt_</span><span class="sxs-lookup"><span data-stu-id="2de80-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="2de80-120">[out] Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="2de80-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="2de80-121">Этот интерфейс — объект-контейнер, выбранный пользователем.</span><span class="sxs-lookup"><span data-stu-id="2de80-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2de80-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2de80-122">Return value</span></span>

<span data-ttu-id="2de80-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="2de80-123">S_OK</span></span> 
  
> <span data-ttu-id="2de80-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2de80-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2de80-125">���������</span><span class="sxs-lookup"><span data-stu-id="2de80-125">Remarks</span></span>

<span data-ttu-id="2de80-126">Средства просмотра формы обычно вызовите метод **IMAPIFormMgr::SelectFormContainer** для выбора формы контейнер, в котором установлен формы.</span><span class="sxs-lookup"><span data-stu-id="2de80-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="2de80-127">**SelectFormContainer** не может использоваться для выбора контейнера локального формы, который имеет значение HFRMREG_LOCAL.</span><span class="sxs-lookup"><span data-stu-id="2de80-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2de80-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2de80-128">MFCMAPI reference</span></span>

<span data-ttu-id="2de80-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2de80-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2de80-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2de80-130">**File**</span></span>|<span data-ttu-id="2de80-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2de80-131">**Function**</span></span>|<span data-ttu-id="2de80-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2de80-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2de80-133">MainDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2de80-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="2de80-134">CMainDlg::OnSelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="2de80-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="2de80-135">Mfcmapi (en) использует метод **IMAPIFormMgr::SelectFormContainer** для выбора контейнера формы перед отображением его содержимого.</span><span class="sxs-lookup"><span data-stu-id="2de80-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2de80-136">См. также</span><span class="sxs-lookup"><span data-stu-id="2de80-136">See also</span></span>



[<span data-ttu-id="2de80-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2de80-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="2de80-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2de80-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

