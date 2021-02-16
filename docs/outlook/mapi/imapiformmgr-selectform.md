---
title: IMAPIFormMgrSelectForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormMgr.SelectForm
api_type:
- COM
ms.assetid: c1cfe71b-01f3-429a-8b4c-73191a2ffea0
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c25f352e7fa607a46741164574a4ba91d4026edf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33423582"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="9b27e-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="9b27e-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="9b27e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9b27e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9b27e-105">Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект сведений о форме, описывая эту форму.</span><span class="sxs-lookup"><span data-stu-id="9b27e-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="9b27e-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="9b27e-106">Parameters</span></span>

 <span data-ttu-id="9b27e-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="9b27e-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="9b27e-108">[in] Handle to the parent window of the displayed dialog box.</span><span class="sxs-lookup"><span data-stu-id="9b27e-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="9b27e-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="9b27e-109">_ulFlags_</span></span>
  
> <span data-ttu-id="9b27e-110">[in] Битоваяmas флагов, которая управляет типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="9b27e-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="9b27e-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="9b27e-111">The following flag can be set:</span></span>
    
<span data-ttu-id="9b27e-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="9b27e-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="9b27e-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="9b27e-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="9b27e-114">Если флаг MAPI_UNICODE не установлен, строки будут в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="9b27e-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="9b27e-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="9b27e-115">_pszTitle_</span></span>
  
> <span data-ttu-id="9b27e-116">[in] Указатель на строку, которая содержит заголовок диалоговых окна.</span><span class="sxs-lookup"><span data-stu-id="9b27e-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="9b27e-117">Если параметр  _pszTitle_ имеет значение NULL, поставщик библиотеки форм передает заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="9b27e-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="9b27e-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="9b27e-118">_pfld_</span></span>
  
> <span data-ttu-id="9b27e-119">[in] Указатель на папку, из которой нужно выбрать форму.</span><span class="sxs-lookup"><span data-stu-id="9b27e-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="9b27e-120">Если параметр  _pfld_ имеет NULL, форму можно выбрать из локального, личного или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="9b27e-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="9b27e-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="9b27e-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="9b27e-122">[out] Указатель на указатель на возвращенный объект сведений формы.</span><span class="sxs-lookup"><span data-stu-id="9b27e-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="9b27e-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9b27e-123">Return value</span></span>

<span data-ttu-id="9b27e-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="9b27e-124">S_OK</span></span> 
  
> <span data-ttu-id="9b27e-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="9b27e-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="9b27e-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="9b27e-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="9b27e-127">Либо флаг MAPI_UNICODE установлен, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлен, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="9b27e-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="9b27e-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="9b27e-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="9b27e-129">Пользователь отменил операцию, обычно нажав  кнопку "Отмена" в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="9b27e-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="9b27e-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="9b27e-130">Remarks</span></span>

<span data-ttu-id="9b27e-131">Посетители форм вызовите метод **IMAPIFormMgr::SelectForm,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать форму, а затем получить объект сведений о форме, описывая выбранную форму.</span><span class="sxs-lookup"><span data-stu-id="9b27e-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="9b27e-132">Диалоговое окно ограничивает выбор одной формы пользователем.</span><span class="sxs-lookup"><span data-stu-id="9b27e-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="9b27e-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="9b27e-133">Notes to callers</span></span>

<span data-ttu-id="9b27e-134">В **диалоговом окне SelectForm** отображаются только те формы, которые не являются скрытыми (то есть формы со скрытыми свойствами не скрыты).</span><span class="sxs-lookup"><span data-stu-id="9b27e-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="9b27e-135">Если просмотр формы передает флаг MAPI_UNICODE в  _параметре ulFlags,_ все строки будут Юникод.</span><span class="sxs-lookup"><span data-stu-id="9b27e-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="9b27e-136">Поставщики библиотеки форм, которые не поддерживают строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, MAPI_UNICODE передается.</span><span class="sxs-lookup"><span data-stu-id="9b27e-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="9b27e-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="9b27e-137">MFCMAPI reference</span></span>

<span data-ttu-id="9b27e-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="9b27e-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="9b27e-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="9b27e-139">**File**</span></span>|<span data-ttu-id="9b27e-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="9b27e-140">**Function**</span></span>|<span data-ttu-id="9b27e-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="9b27e-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="9b27e-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="9b27e-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="9b27e-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="9b27e-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="9b27e-144">MFCMAPI использует метод **IMAPIFormMgr::SelectForm** для выбора формы и отправки сведений о форме в один или несколько журналов.</span><span class="sxs-lookup"><span data-stu-id="9b27e-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="9b27e-145">См. также</span><span class="sxs-lookup"><span data-stu-id="9b27e-145">See also</span></span>



[<span data-ttu-id="9b27e-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="9b27e-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="9b27e-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="9b27e-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

