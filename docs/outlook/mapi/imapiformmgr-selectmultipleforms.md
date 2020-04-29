---
title: имапиформмгрселектмултиплеформс
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
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="a89b9-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="a89b9-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="a89b9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a89b9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a89b9-105">Отображает диалоговое окно, позволяющее пользователю выбрать несколько форм и возвратить массив объектов сведений о форме, описывающих эти формы.</span><span class="sxs-lookup"><span data-stu-id="a89b9-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="a89b9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a89b9-106">Parameters</span></span>

 <span data-ttu-id="a89b9-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="a89b9-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="a89b9-108">возврата Дескриптор родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a89b9-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="a89b9-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="a89b9-109">_ulFlags_</span></span>
  
> <span data-ttu-id="a89b9-110">возврата Битовая маска флагов, которые управляют типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="a89b9-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="a89b9-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="a89b9-111">The following flag can be set:</span></span>
    
<span data-ttu-id="a89b9-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="a89b9-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="a89b9-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="a89b9-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="a89b9-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="a89b9-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="a89b9-115">_псзтитле_</span><span class="sxs-lookup"><span data-stu-id="a89b9-115">_pszTitle_</span></span>
  
> <span data-ttu-id="a89b9-116">возврата Указатель на строку, которая содержит заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="a89b9-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="a89b9-117">Если параметр _псзтитле_ имеет значение null, поставщик библиотеки форм, предоставляющий формы, предоставляет заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="a89b9-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="a89b9-118">_пфлд_</span><span class="sxs-lookup"><span data-stu-id="a89b9-118">_pfld_</span></span>
  
> <span data-ttu-id="a89b9-119">возврата Указатель на папку, из которой необходимо выбрать формы.</span><span class="sxs-lookup"><span data-stu-id="a89b9-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="a89b9-120">Если параметр _пфлд_ имеет значение null, формы выбираются из локального контейнера, персонального или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="a89b9-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="a89b9-121">_пфрминфоаррай_</span><span class="sxs-lookup"><span data-stu-id="a89b9-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="a89b9-122">возврата Указатель на массив объектов данных формы, выбранных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="a89b9-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="a89b9-123">_ппфрминфоаррай_</span><span class="sxs-lookup"><span data-stu-id="a89b9-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="a89b9-124">вышли Указатель на указатель на возвращенный массив объектов данных формы.</span><span class="sxs-lookup"><span data-stu-id="a89b9-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a89b9-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="a89b9-125">Return value</span></span>

<span data-ttu-id="a89b9-126">S_OK</span><span class="sxs-lookup"><span data-stu-id="a89b9-126">S_OK</span></span> 
  
> <span data-ttu-id="a89b9-127">Вызов выполнен успешно и вернул ожидаемое значение или значения.</span><span class="sxs-lookup"><span data-stu-id="a89b9-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="a89b9-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="a89b9-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="a89b9-129">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="a89b9-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="a89b9-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="a89b9-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="a89b9-131">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="a89b9-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="a89b9-132">Примечания</span><span class="sxs-lookup"><span data-stu-id="a89b9-132">Remarks</span></span>

<span data-ttu-id="a89b9-133">При просмотре форм вызывается метод **имапиформмгр:: селектмултиплеформс** , чтобы сначала показать диалоговое окно, которое позволяет пользователю выбрать несколько форм, а затем извлечь массив объектов данных формы, описывающих выбранные формы.</span><span class="sxs-lookup"><span data-stu-id="a89b9-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="a89b9-134">В диалоговом окне **селектмултиплеформс** отображаются все формы, независимо от того, являются ли они скрытыми (то есть независимо от того, являются ли их скрытые свойства понятными).</span><span class="sxs-lookup"><span data-stu-id="a89b9-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="a89b9-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="a89b9-135">Notes to implementers</span></span>

<span data-ttu-id="a89b9-136">Если средство просмотра формы передает MAPI_UNICODEный флаг в параметре _ulFlags_ , все строки имеют кодировку Юникод.</span><span class="sxs-lookup"><span data-stu-id="a89b9-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="a89b9-137">Поставщики библиотеки форм, не поддерживающие строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE передается.</span><span class="sxs-lookup"><span data-stu-id="a89b9-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a89b9-138">См. также</span><span class="sxs-lookup"><span data-stu-id="a89b9-138">See also</span></span>



[<span data-ttu-id="a89b9-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a89b9-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

