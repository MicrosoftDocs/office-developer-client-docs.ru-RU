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
ms.openlocfilehash: b481eaf00b7568da5f02ffa3301e8f2698a98e1e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808944"
---
# <a name="imapiformmgrselectform"></a><span data-ttu-id="f9cf7-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="f9cf7-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="f9cf7-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="f9cf7-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="f9cf7-105">Предоставляет диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект данные формы с описанием данной форме.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="f9cf7-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="f9cf7-106">Parameters</span></span>

 <span data-ttu-id="f9cf7-107">_ulUIParam_</span><span class="sxs-lookup"><span data-stu-id="f9cf7-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="f9cf7-108">[in] Дескриптор родительского окна, отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="f9cf7-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="f9cf7-109">_ulFlags_</span></span>
  
> <span data-ttu-id="f9cf7-110">[in] Битовая маска флаги, определяющее тип строк, переданное.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="f9cf7-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="f9cf7-111">The following flag can be set:</span></span>
    
<span data-ttu-id="f9cf7-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="f9cf7-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="f9cf7-113">Строки переданное хранятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="f9cf7-114">Если флаг MAPI_UNICODE не установлен, они в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="f9cf7-115">_pszTitle_</span><span class="sxs-lookup"><span data-stu-id="f9cf7-115">_pszTitle_</span></span>
  
> <span data-ttu-id="f9cf7-116">[in] Указатель на строку, которая содержит заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="f9cf7-117">Если параметр _pszTitle_ имеет значение NULL, поставщик библиотеки форм предоставляет заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="f9cf7-118">_pfld_</span><span class="sxs-lookup"><span data-stu-id="f9cf7-118">_pfld_</span></span>
  
> <span data-ttu-id="f9cf7-119">[in] Указатель на папку для выбора формы.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="f9cf7-120">Если параметр _pfld_ имеет значение NULL, форма можно выбирать из контейнера формы local, личный или организации.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="f9cf7-121">_ppfrminfoReturned_</span><span class="sxs-lookup"><span data-stu-id="f9cf7-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="f9cf7-122">[out] Указатель на указатель на объект сведения возвращенные формы.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="f9cf7-123">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="f9cf7-123">Return value</span></span>

<span data-ttu-id="f9cf7-124">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="f9cf7-124">S_OK</span></span> 
  
> <span data-ttu-id="f9cf7-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="f9cf7-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="f9cf7-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="f9cf7-127">Либо был установлен флажок MAPI_UNICODE и реализация не поддерживает Юникод, или MAPI_UNICODE не было установлено и реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="f9cf7-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="f9cf7-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="f9cf7-129">Пользователь отменил операцию, как правило, нажмите кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="f9cf7-130">Замечания</span><span class="sxs-lookup"><span data-stu-id="f9cf7-130">Remarks</span></span>

<span data-ttu-id="f9cf7-131">Средства просмотра формы вызвать метод **IMAPIFormMgr::SelectForm** для первым диалоговое окно, которое позволяет пользователю выбрать формы и затем для получения объекта данные формы, описывающий выбранной формы.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="f9cf7-132">Диалоговое окно ограничения, предписывающие пользователю выбрать одну форму.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="f9cf7-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="f9cf7-133">Notes to callers</span></span>

<span data-ttu-id="f9cf7-134">Диалоговое окно **SelectForm** отображает только формы, которые не являются скрытыми (то есть, форм, имеющих их скрытые свойства снимите флажок).</span><span class="sxs-lookup"><span data-stu-id="f9cf7-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="f9cf7-135">Если форма просмотра передает флаг MAPI_UNICODE в параметре _ulFlags_ , все строки содержат Юникод.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="f9cf7-136">Поставщики библиотеки форм, которые не поддерживают строк в кодировке Юникод должен возвращать MAPI_E_BAD_CHARWIDTH, если передается MAPI_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="f9cf7-137">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="f9cf7-137">MFCMAPI reference</span></span>

<span data-ttu-id="f9cf7-138">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="f9cf7-139">**����**</span><span class="sxs-lookup"><span data-stu-id="f9cf7-139">**File**</span></span>|<span data-ttu-id="f9cf7-140">**�������**</span><span class="sxs-lookup"><span data-stu-id="f9cf7-140">**Function**</span></span>|<span data-ttu-id="f9cf7-141">**�����������**</span><span class="sxs-lookup"><span data-stu-id="f9cf7-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="f9cf7-142">FolderDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="f9cf7-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="f9cf7-143">CFolderDlg::OnSelectForm</span><span class="sxs-lookup"><span data-stu-id="f9cf7-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="f9cf7-144">Mfcmapi (en) использует метод **IMAPIFormMgr::SelectForm** для выбора формы и отправки информации о формы для одного или нескольких журналов.</span><span class="sxs-lookup"><span data-stu-id="f9cf7-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="f9cf7-145">См. также</span><span class="sxs-lookup"><span data-stu-id="f9cf7-145">See also</span></span>



[<span data-ttu-id="f9cf7-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="f9cf7-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="f9cf7-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="f9cf7-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

