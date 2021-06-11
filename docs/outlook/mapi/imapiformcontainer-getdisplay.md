---
title: IMAPIFormContainerGetDisplay
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.GetDisplay
api_type:
- COM
ms.assetid: 6829e273-4a75-4278-b58a-ae7543e075ac
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 994041d050df56fd3fa3c0e599542e05a202ad65
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416134"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="5a011-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="5a011-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="5a011-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5a011-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5a011-105">Возвращает имя отображения контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="5a011-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="5a011-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="5a011-106">Parameters</span></span>

 <span data-ttu-id="5a011-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="5a011-107">_ulFlags_</span></span>
  
> <span data-ttu-id="5a011-108">[in] Битмашка флагов, контролируемая типом возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="5a011-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="5a011-109">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="5a011-109">The following flag can be set:</span></span>
    
<span data-ttu-id="5a011-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="5a011-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="5a011-111">Возвращенная строка находится в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="5a011-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="5a011-112">Если флаг MAPI_UNICODE не установлен, строка находится в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="5a011-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="5a011-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="5a011-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="5a011-114">[вышел] Указатель на строку с отображаемой именем контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="5a011-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="5a011-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5a011-115">Return value</span></span>

<span data-ttu-id="5a011-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="5a011-116">S_OK</span></span> 
  
> <span data-ttu-id="5a011-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="5a011-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="5a011-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="5a011-118">MFCMAPI reference</span></span>

<span data-ttu-id="5a011-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="5a011-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="5a011-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="5a011-120">**File**</span></span>|<span data-ttu-id="5a011-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="5a011-121">**Function**</span></span>|<span data-ttu-id="5a011-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="5a011-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="5a011-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="5a011-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="5a011-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="5a011-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="5a011-125">MFCMAPI использует метод **IMAPIFormContainer::GetDisplay** для получения имени контейнера формы при отрисовке CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="5a011-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="5a011-126">См. также</span><span class="sxs-lookup"><span data-stu-id="5a011-126">See also</span></span>



[<span data-ttu-id="5a011-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="5a011-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="5a011-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="5a011-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

