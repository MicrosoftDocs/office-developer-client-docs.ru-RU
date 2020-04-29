---
title: имапиформмгрселектформ
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
# <a name="imapiformmgrselectform"></a><span data-ttu-id="0efff-103">IMAPIFormMgr::SelectForm</span><span class="sxs-lookup"><span data-stu-id="0efff-103">IMAPIFormMgr::SelectForm</span></span>

  
  
<span data-ttu-id="0efff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0efff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0efff-105">Отображает диалоговое окно, которое позволяет пользователю выбрать форму и возвращает объект сведений о форме, который описывает эту форму.</span><span class="sxs-lookup"><span data-stu-id="0efff-105">Presents a dialog box that enables the user to select a form, and returns a form information object that describes that form.</span></span>
  
```cpp
HRESULT SelectForm(
  ULONG_PTR ulUIParam,
  ULONG ulFlags,
  LPCSTR pszTitle,
  LPMAPIFOLDER pfld,
  LPMAPIFORMINFO FAR * ppfrminfoReturned
);
```

## <a name="parameters"></a><span data-ttu-id="0efff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="0efff-106">Parameters</span></span>

 <span data-ttu-id="0efff-107">_улуипарам_</span><span class="sxs-lookup"><span data-stu-id="0efff-107">_ulUIParam_</span></span>
  
> <span data-ttu-id="0efff-108">возврата Дескриптор родительского окна отображаемого диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0efff-108">[in] A handle to the parent window of the displayed dialog box.</span></span> 
    
 <span data-ttu-id="0efff-109">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="0efff-109">_ulFlags_</span></span>
  
> <span data-ttu-id="0efff-110">возврата Битовая маска флагов, которые управляют типом переданных строк.</span><span class="sxs-lookup"><span data-stu-id="0efff-110">[in] A bitmask of flags that controls the type of the passed-in strings.</span></span> <span data-ttu-id="0efff-111">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="0efff-111">The following flag can be set:</span></span>
    
<span data-ttu-id="0efff-112">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="0efff-112">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="0efff-113">Переданные строки имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="0efff-113">The passed-in strings are in Unicode format.</span></span> <span data-ttu-id="0efff-114">Если флаг MAPI_UNICODE не установлен, строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="0efff-114">If the MAPI_UNICODE flag is not set, the strings are in ANSI format.</span></span>
    
 <span data-ttu-id="0efff-115">_псзтитле_</span><span class="sxs-lookup"><span data-stu-id="0efff-115">_pszTitle_</span></span>
  
> <span data-ttu-id="0efff-116">возврата Указатель на строку, которая содержит заголовок диалогового окна.</span><span class="sxs-lookup"><span data-stu-id="0efff-116">[in] A pointer to a string that contains the caption of the dialog box.</span></span> <span data-ttu-id="0efff-117">Если параметр _псзтитле_ имеет значение null, поставщик библиотеки форм предоставляет заголовок по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="0efff-117">If the  _pszTitle_ parameter is NULL, the form library provider supplies a default caption.</span></span> 
    
 <span data-ttu-id="0efff-118">_пфлд_</span><span class="sxs-lookup"><span data-stu-id="0efff-118">_pfld_</span></span>
  
> <span data-ttu-id="0efff-119">возврата Указатель на папку, из которой будет выбрана форма.</span><span class="sxs-lookup"><span data-stu-id="0efff-119">[in] A pointer to the folder from which to select the form.</span></span> <span data-ttu-id="0efff-120">Если параметр _пфлд_ имеет значение null, форма может быть выбрана из локального контейнера, персонального или контейнера формы организации.</span><span class="sxs-lookup"><span data-stu-id="0efff-120">If the  _pfld_ parameter is NULL, the form can be selected from the local, personal, or organization form container.</span></span> 
    
 <span data-ttu-id="0efff-121">_ппфрминфоретурнед_</span><span class="sxs-lookup"><span data-stu-id="0efff-121">_ppfrminfoReturned_</span></span>
  
> <span data-ttu-id="0efff-122">вышли Указатель на указатель на возвращенный объект сведений о форме.</span><span class="sxs-lookup"><span data-stu-id="0efff-122">[out] A pointer to a pointer to the returned form information object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="0efff-123">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="0efff-123">Return value</span></span>

<span data-ttu-id="0efff-124">S_OK</span><span class="sxs-lookup"><span data-stu-id="0efff-124">S_OK</span></span> 
  
> <span data-ttu-id="0efff-125">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="0efff-125">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="0efff-126">MAPI_E_BAD_CHARWIDTH</span><span class="sxs-lookup"><span data-stu-id="0efff-126">MAPI_E_BAD_CHARWIDTH</span></span> 
  
> <span data-ttu-id="0efff-127">Установлен флаг MAPI_UNICODE, а реализация не поддерживает Юникод, или MAPI_UNICODE не задано, а реализация поддерживает только Юникод.</span><span class="sxs-lookup"><span data-stu-id="0efff-127">Either the MAPI_UNICODE flag was set and the implementation does not support Unicode, or MAPI_UNICODE was not set and the implementation supports only Unicode.</span></span>
    
<span data-ttu-id="0efff-128">MAPI_E_USER_CANCEL</span><span class="sxs-lookup"><span data-stu-id="0efff-128">MAPI_E_USER_CANCEL</span></span> 
  
> <span data-ttu-id="0efff-129">Пользователь отменил операцию, как правило, нажав кнопку **Отмена** в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="0efff-129">The user canceled the operation, typically by clicking the **Cancel** button in the dialog box.</span></span> 
    
## <a name="remarks"></a><span data-ttu-id="0efff-130">Примечания</span><span class="sxs-lookup"><span data-stu-id="0efff-130">Remarks</span></span>

<span data-ttu-id="0efff-131">При просмотре форм вызывается метод **имапиформмгр:: селектформ** , чтобы сначала показать диалоговое окно, которое позволяет пользователю выбрать форму, а затем извлечь объект сведений о форме, описывающий выбранную форму.</span><span class="sxs-lookup"><span data-stu-id="0efff-131">Form viewers call the **IMAPIFormMgr::SelectForm** method to first present a dialog box that enables the user to select a form and then to retrieve a form information object that describes the selected form.</span></span> <span data-ttu-id="0efff-132">Диалоговое окно ограничивает выбор одной формы пользователем.</span><span class="sxs-lookup"><span data-stu-id="0efff-132">The dialog box constrains the user to select a single form.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="0efff-133">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="0efff-133">Notes to callers</span></span>

<span data-ttu-id="0efff-134">В диалоговом окне **селектформ** отображаются только те формы, которые не являются скрытыми (то есть формы со скрытыми свойствами были удалены).</span><span class="sxs-lookup"><span data-stu-id="0efff-134">The **SelectForm** dialog box displays only forms that are not hidden (that is, forms that have their hidden properties clear).</span></span> <span data-ttu-id="0efff-135">Если средство просмотра формы передает MAPI_UNICODEный флаг в параметре _ulFlags_ , все строки имеют кодировку Юникод.</span><span class="sxs-lookup"><span data-stu-id="0efff-135">If a form viewer passes the MAPI_UNICODE flag in the  _ulFlags_ parameter, all strings are Unicode.</span></span> <span data-ttu-id="0efff-136">Поставщики библиотеки форм, не поддерживающие строки Юникода, должны возвращать MAPI_E_BAD_CHARWIDTH, если MAPI_UNICODE передается.</span><span class="sxs-lookup"><span data-stu-id="0efff-136">Form library providers that do not support Unicode strings should return MAPI_E_BAD_CHARWIDTH if MAPI_UNICODE is passed.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="0efff-137">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="0efff-137">MFCMAPI reference</span></span>

<span data-ttu-id="0efff-138">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="0efff-138">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="0efff-139">**Файл**</span><span class="sxs-lookup"><span data-stu-id="0efff-139">**File**</span></span>|<span data-ttu-id="0efff-140">**Функция**</span><span class="sxs-lookup"><span data-stu-id="0efff-140">**Function**</span></span>|<span data-ttu-id="0efff-141">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="0efff-141">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="0efff-142">Фолдердлг. cpp</span><span class="sxs-lookup"><span data-stu-id="0efff-142">FolderDlg.cpp</span></span>  <br/> |<span data-ttu-id="0efff-143">Кфолдердлг:: Онселектформ</span><span class="sxs-lookup"><span data-stu-id="0efff-143">CFolderDlg::OnSelectForm</span></span>  <br/> |<span data-ttu-id="0efff-144">MFCMAPI использует метод **имапиформмгр:: селектформ** , чтобы выбрать форму и отправить сведения о форме в один или несколько журналов.</span><span class="sxs-lookup"><span data-stu-id="0efff-144">MFCMAPI uses the **IMAPIFormMgr::SelectForm** method to select a form and send information about the form to one or more logs.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="0efff-145">См. также</span><span class="sxs-lookup"><span data-stu-id="0efff-145">See also</span></span>



[<span data-ttu-id="0efff-146">IMAPIFormMgr : IUnknown</span><span class="sxs-lookup"><span data-stu-id="0efff-146">IMAPIFormMgr : IUnknown</span></span>](imapiformmgriunknown.md)


[<span data-ttu-id="0efff-147">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="0efff-147">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

