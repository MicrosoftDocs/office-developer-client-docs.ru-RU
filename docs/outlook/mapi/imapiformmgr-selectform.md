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
# <a name="imapiformmgrselectform"></a><span data-ttu-id="89879-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="89879-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="89879-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="89879-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="89879-105">Представляет диалоговое окно, которое позволяет пользователю выбрать форму, и возвращает объект информации о форме, описывая эту форму.</span><span class="sxs-lookup"><span data-stu-id="89879-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="89879-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="89879-106">Parameters</span></span>

 <span data-ttu-id="89879-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="89879-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="89879-108">[in] Ручка родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="89879-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="89879-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="89879-109">_ulFlags_</span></span>
  
> <span data-ttu-id="89879-110">[in] Битмашка флагов, контролируемая типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="89879-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="89879-111">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="89879-111">The following flag can be set:</span></span>
    
<span data-ttu-id="89879-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="89879-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="89879-113">Переданные строки находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="89879-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="89879-114">Если флаг MAPI_UNICODE не установлен, строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="89879-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="89879-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="89879-115">_pszTitle_</span></span>
  
> <span data-ttu-id="89879-116">[in] Указатель на строку, содержаную подпись диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="89879-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="89879-117">Если параметр  _pszTitle_ является NULL, поставщик библиотеки форм поставляет подпись по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="89879-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="89879-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="89879-118">_pfld_</span></span>
  
> <span data-ttu-id="89879-119">[in] Указатель на папку, из которой нужно выбрать форму.</span><span class="sxs-lookup"><span data-stu-id="89879-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="89879-120">Если параметр  _pfld_ NULL, форма может быть выбрана из локального, личного или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="89879-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="89879-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="89879-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="89879-122">[вышел] Указатель на указатель на возвращенный информационный объект формы.</span><span class="sxs-lookup"><span data-stu-id="89879-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="89879-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="89879-123">Return value</span></span>

<span data-ttu-id="89879-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="89879-124">S_OK</span></span> 
  
> <span data-ttu-id="89879-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="89879-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="89879-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="89879-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="89879-127">Либо был MAPI_UNICODE флаг, а реализация не поддерживает Юникод, либо MAPI_UNICODE не установлена, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="89879-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="89879-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="89879-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="89879-129">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="89879-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="89879-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="89879-130">Remarks</span></span>

<span data-ttu-id="89879-131">Зрители формы звонят по методу **IMAPIFormMgr:::SelectForm,** чтобы сначала представить диалоговое окно, которое позволяет пользователю выбрать форму, а затем получить информационный объект формы, описывая выбранную форму.</span><span class="sxs-lookup"><span data-stu-id="89879-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="89879-132">Диалоговое окно ограничивает пользователя в выборе одной формы.</span><span class="sxs-lookup"><span data-stu-id="89879-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="89879-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="89879-133">Notes to callers</span></span>

<span data-ttu-id="89879-134">В **диалоговом** окне SelectForm отображаются только не скрытые формы (то есть формы со скрытыми свойствами).</span><span class="sxs-lookup"><span data-stu-id="89879-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="89879-135">Если зритель формы передает флаг MAPI_UNICODE  _в параметре ulFlags,_ все строки являются Юникодом.</span><span class="sxs-lookup"><span data-stu-id="89879-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="89879-136">Поставщики библиотек форм, которые не поддерживают строки Юникод, должны MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE будет пройдена.</span><span class="sxs-lookup"><span data-stu-id="89879-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="89879-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="89879-137">MFCMAPI reference</span></span>

<span data-ttu-id="89879-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="89879-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="89879-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="89879-139">**File**</span></span>|<span data-ttu-id="89879-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="89879-140">**Function**</span></span>|<span data-ttu-id="89879-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="89879-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="89879-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="89879-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="89879-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="89879-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="89879-144">MFCMAPI использует **метод IMAPIFormMgr::SelectForm** для выбора формы и отправки сведений о форме в один или несколько журналов.</span><span class="sxs-lookup"><span data-stu-id="89879-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="89879-145">См. также</span><span class="sxs-lookup"><span data-stu-id="89879-145">See also</span></span>



[<span data-ttu-id="89879-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="89879-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="89879-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="89879-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

