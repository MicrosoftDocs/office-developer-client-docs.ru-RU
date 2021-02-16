---
title: IMAPIFormMgrSelectMultipleForms
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectMultipleForms
api_type:
- COM
ms.assetid: 172f8f53-b837-4286-9236-3f72806d7f1f
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c40d853c49645638c2ec4001d86e64a1b2d2e381
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420313"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="1e40d-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="1e40d-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="1e40d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1e40d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1e40d-105">Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив информационных объектов формы, описывая эти формы.</span><span class="sxs-lookup"><span data-stu-id="1e40d-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
```cpp
HRESULT SelectMultipleForms(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFOARRAY pfrminfoarray,
  LPMAPIFORMINFOARRAY FAR * ppfrminfoarray
);
```

## <a name="parameters"></a><span data-ttu-id="1e40d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1e40d-106">Parameters</span></span>

 <span data-ttu-id="1e40d-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="1e40d-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="1e40d-108">[in] Handle to the parent window of the displayed dialog box.</span><span class="sxs-lookup"><span data-stu-id="1e40d-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="1e40d-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="1e40d-109">_ulFlags_</span></span>
  
> <span data-ttu-id="1e40d-110">[in] Битоваяmas флагов, которая управляет типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="1e40d-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="1e40d-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="1e40d-111">The following flag can be set:</span></span>
    
<span data-ttu-id="1e40d-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="1e40d-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="1e40d-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="1e40d-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="1e40d-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="1e40d-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="1e40d-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="1e40d-115">_pszTitle_</span></span>
  
> <span data-ttu-id="1e40d-116">[in] Указатель на строку, которая содержит заголовок диалоговых окно.</span><span class="sxs-lookup"><span data-stu-id="1e40d-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="1e40d-117">Если параметр  _pszTitle_ имеет значение NULL, поставщик библиотеки форм, который предоставляет формы, предоставляет заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="1e40d-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="1e40d-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="1e40d-118">_pfld_</span></span>
  
> <span data-ttu-id="1e40d-119">[in] Указатель на папку, из которой нужно выбрать формы.</span><span class="sxs-lookup"><span data-stu-id="1e40d-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="1e40d-120">Если параметр  _pfld_ имеет NULL, формы выбираются из локального, личного или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="1e40d-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="1e40d-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="1e40d-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="1e40d-122">[in] Указатель на массив информационных объектов формы, предварительно выборки для пользователя.</span><span class="sxs-lookup"><span data-stu-id="1e40d-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="1e40d-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="1e40d-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="1e40d-124">[out] Указатель на указатель на возвращенный массив информационных объектов формы.</span><span class="sxs-lookup"><span data-stu-id="1e40d-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1e40d-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1e40d-125">Return value</span></span>

<span data-ttu-id="1e40d-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="1e40d-126">S_OK</span></span> 
  
> <span data-ttu-id="1e40d-127">Вызов был успешным и возвратил ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="1e40d-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="1e40d-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="1e40d-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="1e40d-129">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="1e40d-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="1e40d-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="1e40d-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="1e40d-131">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="1e40d-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="1e40d-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="1e40d-132">Remarks</span></span>

<span data-ttu-id="1e40d-133">С помощью метода **IMAPIFormMgr::SelectMultipleForms можно вызвать метод IMAPIFormMgr::SelectMultipleForms,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбирать несколько форм, а затем извлекать массив информационных объектов форм, которые описывают выбранные формы.</span><span class="sxs-lookup"><span data-stu-id="1e40d-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="1e40d-134">В диалоговом окне **SelectMultipleForms** отображаются все формы независимо от того, являются ли они скрытыми (то есть понятны ли их скрытые свойства).</span><span class="sxs-lookup"><span data-stu-id="1e40d-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="1e40d-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="1e40d-135">Notes to implementers</span></span>

<span data-ttu-id="1e40d-136">Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки будут Юникод.</span><span class="sxs-lookup"><span data-stu-id="1e40d-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="1e40d-137">Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается.</span><span class="sxs-lookup"><span data-stu-id="1e40d-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="1e40d-138">См. также</span><span class="sxs-lookup"><span data-stu-id="1e40d-138">See also</span></span>



[<span data-ttu-id="1e40d-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="1e40d-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

