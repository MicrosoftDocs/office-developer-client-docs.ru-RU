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
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="39a7b-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="39a7b-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="39a7b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="39a7b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="39a7b-105">Представляет диалоговое окно, которое позволяет пользователю выбирать несколько форм и возвращает массив объектов информации о форме, описывая эти формы.</span><span class="sxs-lookup"><span data-stu-id="39a7b-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="39a7b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="39a7b-106">Parameters</span></span>

 <span data-ttu-id="39a7b-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="39a7b-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="39a7b-108">[in] Ручка родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="39a7b-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="39a7b-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="39a7b-109">_ulFlags_</span></span>
  
> <span data-ttu-id="39a7b-110">[in] Битмашка флагов, контролируемая типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="39a7b-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="39a7b-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="39a7b-111">The following flag can be set:</span></span>
    
<span data-ttu-id="39a7b-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="39a7b-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="39a7b-113">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="39a7b-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="39a7b-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="39a7b-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="39a7b-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="39a7b-115">_pszTitle_</span></span>
  
> <span data-ttu-id="39a7b-116">[in] Указатель на строку, содержаную подпись диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="39a7b-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="39a7b-117">Если параметр  _pszTitle_ — NULL, поставщик библиотеки форм, который предоставляет формы, содержит подпись по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="39a7b-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="39a7b-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="39a7b-118">_pfld_</span></span>
  
> <span data-ttu-id="39a7b-119">[in] Указатель на папку, из которой нужно выбрать формы.</span><span class="sxs-lookup"><span data-stu-id="39a7b-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="39a7b-120">Если параметр  _pfld_ является NULL, формы выбираются из локального, личного или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="39a7b-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="39a7b-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="39a7b-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="39a7b-122">[in] Указатель на массив объектов информации о форме, предварительно предварительно отбираемых для пользователя.</span><span class="sxs-lookup"><span data-stu-id="39a7b-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="39a7b-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="39a7b-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="39a7b-124">[вышел] Указатель на указатель возвращаемого массива информационных объектов форм.</span><span class="sxs-lookup"><span data-stu-id="39a7b-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="39a7b-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="39a7b-125">Return value</span></span>

<span data-ttu-id="39a7b-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="39a7b-126">S_OK</span></span> 
  
> <span data-ttu-id="39a7b-127">Вызов удался и возвращает ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="39a7b-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="39a7b-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="39a7b-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="39a7b-129">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="39a7b-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="39a7b-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="39a7b-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="39a7b-131">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="39a7b-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="39a7b-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="39a7b-132">Remarks</span></span>

<span data-ttu-id="39a7b-133">Зрители формы звонят по методу **IMAPIFormMgr:::SelectMultipleForms,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать несколько форм, а затем получить массив информационных объектов форм, описывая выбранные формы.</span><span class="sxs-lookup"><span data-stu-id="39a7b-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="39a7b-134">Диалоговое окно **SelectMultipleForms** отображает все формы независимо от того, скрыты ли они (то есть понятны ли их скрытые свойства).</span><span class="sxs-lookup"><span data-stu-id="39a7b-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="39a7b-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="39a7b-135">Notes to implementers</span></span>

<span data-ttu-id="39a7b-136">Если зритель формы передает флаг MAPI_UNICODE  _в параметре ulFlags,_ все строки являются Юникодом.</span><span class="sxs-lookup"><span data-stu-id="39a7b-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="39a7b-137">Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена.</span><span class="sxs-lookup"><span data-stu-id="39a7b-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="39a7b-138">См. также</span><span class="sxs-lookup"><span data-stu-id="39a7b-138">See also</span></span>



[<span data-ttu-id="39a7b-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="39a7b-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

