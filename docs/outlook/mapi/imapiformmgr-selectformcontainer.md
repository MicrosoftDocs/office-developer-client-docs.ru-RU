---
title: Имапиформмгрселектформконтаинер
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321590"
---
# <a name="imapiformmgrselectformcontainer"></a><span data-ttu-id="d9bff-103">IMAPIFormMgr::SelectFormContainer</span><span class="sxs-lookup"><span data-stu-id="d9bff-103">IMAPIFormMgr::SelectFormContainer</span></span>

  
  
<span data-ttu-id="d9bff-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d9bff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d9bff-105">Отображает диалоговое окно, позволяющее пользователю выбрать контейнер формы и возврат интерфейса для объекта контейнера, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="d9bff-105">Presents a dialog box that enables the user to select a form container, and returns an interface for the container object the user selected.</span></span>
  
```cpp
HRESULT SelectFormContainer(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPMAPIFORMCONTAINER FAR * lppfcnt
);
```

## <a name="parameters"></a><span data-ttu-id="d9bff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d9bff-106">Parameters</span></span>

 <span data-ttu-id="d9bff-107">_Улуипарам_</span><span class="sxs-lookup"><span data-stu-id="d9bff-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d9bff-108">возврата Дескриптор родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d9bff-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="d9bff-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d9bff-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d9bff-110">возврата Битовая маска флагов, определяющих, как выбирается Библиотека форм (то есть, как выбран контейнер форм).</span><span class="sxs-lookup"><span data-stu-id="d9bff-110">[in] A bitmask of flags that controls how the form library is selected (that is, how the form container is selected).</span></span> <span data-ttu-id="d9bff-111">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="d9bff-111">The following flags can be set:</span></span>
    
<span data-ttu-id="d9bff-112">МАПИФОРМ_СЕЛЕКТ_АЛЛ_РЕГИСТРИЕС</span><span class="sxs-lookup"><span data-stu-id="d9bff-112">MAPIFORM_SELECT_ALL_REGISTRIES</span></span> 
  
> <span data-ttu-id="d9bff-113">Выбор можно выполнить из всех контейнеров.</span><span class="sxs-lookup"><span data-stu-id="d9bff-113">Selection can be made from all containers.</span></span> <span data-ttu-id="d9bff-114">Это тип выбора по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d9bff-114">This is the default selection type.</span></span> 
    
<span data-ttu-id="d9bff-115">МАПИФОРМ_СЕЛЕКТ_ФОЛДЕР_РЕГИСТРИ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="d9bff-115">MAPIFORM_SELECT_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="d9bff-116">Выбор можно осуществлять только из контейнеров папок.</span><span class="sxs-lookup"><span data-stu-id="d9bff-116">Selection can be made only from folder containers.</span></span>
    
<span data-ttu-id="d9bff-117">МАПИФОРМ_СЕЛЕКТ_НОН_ФОЛДЕР_РЕГИСТРИ_ОНЛИ</span><span class="sxs-lookup"><span data-stu-id="d9bff-117">MAPIFORM_SELECT_NON_FOLDER_REGISTRY_ONLY</span></span> 
  
> <span data-ttu-id="d9bff-118">Выбор можно осуществлять только из контейнеров, которые не связаны с папками.</span><span class="sxs-lookup"><span data-stu-id="d9bff-118">Selection can be made only from containers that are not associated with folders.</span></span>
    
 <span data-ttu-id="d9bff-119">_лппфкнт_</span><span class="sxs-lookup"><span data-stu-id="d9bff-119">_lppfcnt_</span></span>
  
> <span data-ttu-id="d9bff-120">вышли Указатель на указатель на возвращенный интерфейс.</span><span class="sxs-lookup"><span data-stu-id="d9bff-120">[out] A pointer to a pointer to the returned interface.</span></span> <span data-ttu-id="d9bff-121">Этот интерфейс предназначен для объекта Container, выбранного пользователем.</span><span class="sxs-lookup"><span data-stu-id="d9bff-121">This interface is for the container object that is selected by the user.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d9bff-122">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="d9bff-122">Return value</span></span>

<span data-ttu-id="d9bff-123">S_OK</span><span class="sxs-lookup"><span data-stu-id="d9bff-123">S_OK</span></span> 
  
> <span data-ttu-id="d9bff-124">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="d9bff-124">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="d9bff-125">Замечания</span><span class="sxs-lookup"><span data-stu-id="d9bff-125">Remarks</span></span>

<span data-ttu-id="d9bff-126">Средства просмотра форм обычно вызывают метод **имапиформмгр:: селектформконтаинер** для выбора контейнера формы, в котором установлена форма.</span><span class="sxs-lookup"><span data-stu-id="d9bff-126">Form viewers typically call the **IMAPIFormMgr::SelectFormContainer** method to select a form container into which a form is installed.</span></span> <span data-ttu-id="d9bff-127">**Селектформконтаинер** не может использоваться для выбора локального контейнера форм, который имеет значение хфрмрег_локал.</span><span class="sxs-lookup"><span data-stu-id="d9bff-127">**SelectFormContainer** cannot be used to select the local form container, which has the value HFRMREG_LOCAL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="d9bff-128">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="d9bff-128">MFCMAPI reference</span></span>

<span data-ttu-id="d9bff-129">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="d9bff-129">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="d9bff-130">**Файл**</span><span class="sxs-lookup"><span data-stu-id="d9bff-130">**File**</span></span>|<span data-ttu-id="d9bff-131">**Функция**</span><span class="sxs-lookup"><span data-stu-id="d9bff-131">**Function**</span></span>|<span data-ttu-id="d9bff-132">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="d9bff-132">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="d9bff-133">Маиндлг. cpp</span><span class="sxs-lookup"><span data-stu-id="d9bff-133">MainDlg.cpp</span></span>  <br/> |<span data-ttu-id="d9bff-134">Кмаиндлг:: Онселектформконтаинер</span><span class="sxs-lookup"><span data-stu-id="d9bff-134">CMainDlg::OnSelectFormContainer</span></span>  <br/> |<span data-ttu-id="d9bff-135">MFCMAPI использует метод **имапиформмгр:: селектформконтаинер** для выбора контейнера формы перед отображением его содержимого.</span><span class="sxs-lookup"><span data-stu-id="d9bff-135">MFCMAPI uses the **IMAPIFormMgr::SelectFormContainer** method to select a form container before rendering its contents.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="d9bff-136">См. также</span><span class="sxs-lookup"><span data-stu-id="d9bff-136">See also</span></span>



[<span data-ttu-id="d9bff-137">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d9bff-137">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="d9bff-138">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="d9bff-138">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

