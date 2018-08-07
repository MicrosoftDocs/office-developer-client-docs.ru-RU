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
ms.openlocfilehash: 096437f10c5b992a1db55f6a856c38021a81b99a
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808960"
---
# <a name="imapiformmgrselectmultipleforms"></a><span data-ttu-id="d4a6e-103">IMAPIFormMgr::SelectMultipleForms</span><span class="sxs-lookup"><span data-stu-id="d4a6e-103">IMAPIFormMgr::SelectMultipleForms</span></span>

  
  
<span data-ttu-id="d4a6e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="d4a6e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="d4a6e-105">Предоставляет диалоговое окно, которое позволяет пользователю выбрать нескольких форм и возвращает массив формы объекты, которые описывают формах.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-105">Presents a dialog box that enables the user to select multiple forms, and returns an array of form information objects that describe those forms.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="d4a6e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="d4a6e-106">Parameters</span></span>

 <span data-ttu-id="d4a6e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="d4a6e-108">[in] Дескриптор родительского окна, отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="d4a6e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="d4a6e-110">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="d4a6e-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="d4a6e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="d4a6e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="d4a6e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="d4a6e-113">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="d4a6e-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="d4a6e-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-115">_pszTitle_</span></span>
  
> <span data-ttu-id="d4a6e-116">[in] Указатель на строку, которая содержит заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="d4a6e-117">Если параметр _pszTitle_ имеет значение NULL, поставщик библиотеки форм, предоставляющий форм предоставляет заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-117">If the  _pszTitle_ parameter is NULL, the form library provider that provides the forms supplies a default caption.</span></span> 
    
 <span data-ttu-id="d4a6e-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-118">_pfld_</span></span>
  
> <span data-ttu-id="d4a6e-119">[in] Указатель на папку для выбора формы.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-119">[in] A pointer to the folder from which to select the forms.</span></span> <span data-ttu-id="d4a6e-120">Если параметр _pfld_ имеет значение NULL, формы выбираются из контейнера формы local, личный или организации.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-120">If the  _pfld_ parameter is NULL, the forms are selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="d4a6e-121">_pfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-121">_pfrminfoarray_</span></span>
  
> <span data-ttu-id="d4a6e-122">[in] Указатель на массив объектов формы сведения, которые предварительно выбранных для пользователя.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-122">[in] A pointer to an array of form information objects that are preselected for the user.</span></span>
    
 <span data-ttu-id="d4a6e-123">_ppfrminfoarray_</span><span class="sxs-lookup"><span data-stu-id="d4a6e-123">_ppfrminfoarray_</span></span>
  
> <span data-ttu-id="d4a6e-124">[out] Указатель на указатель на возвращаемый массив объектов данные формы.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-124">[out] A pointer to a pointer to the returned array of form information objects.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="d4a6e-125">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="d4a6e-126">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="d4a6e-126">S_OK</span></span> 
  
> <span data-ttu-id="d4a6e-127">Вызов успешно и возвращается ожидаемым значением или значения.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-127">The call succeeded and returned the expected value or values.</span></span>
    
<span data-ttu-id="d4a6e-128">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="d4a6e-128">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="d4a6e-129">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-129">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="d4a6e-130">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="d4a6e-130">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="d4a6e-131">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-131">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="d4a6e-132">Замечания</span><span class="sxs-lookup"><span data-stu-id="d4a6e-132">Remarks</span></span>

<span data-ttu-id="d4a6e-133">Средства просмотра формы вызвать метод **IMAPIFormMgr::SelectMultipleForms** для первым диалоговое окно, которое позволяет пользователю выбрать нескольких форм нажмите для получения массива формы сведения объекты и, описывающие выбранные формы.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-133">Form viewers call the **IMAPIFormMgr::SelectMultipleForms** method to first present a dialog box that enables the user to select multiple forms and then to retrieve an array of form information objects that describe the selected forms.</span></span> <span data-ttu-id="d4a6e-134">Диалоговое окно **SelectMultipleForms** отображает все формы ли они являются скрытыми (то есть ли их скрытые свойства не установлены).</span><span class="sxs-lookup"><span data-stu-id="d4a6e-134">The **SelectMultipleForms** dialog box displays all forms, whether or not they are hidden (that is, whether or not their hidden properties are clear).</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="d4a6e-135">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="d4a6e-135">Notes to implementers</span></span>

<span data-ttu-id="d4a6e-136">Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки содержат Юникод.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-136">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="d4a6e-137">Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="d4a6e-137">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="d4a6e-138">См. также</span><span class="sxs-lookup"><span data-stu-id="d4a6e-138">See also</span></span>



[<span data-ttu-id="d4a6e-139">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="d4a6e-139">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)

