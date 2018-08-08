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
ms.openlocfilehash: 0f9826dab72968055604c5bb9f8f537facc5618e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808914"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="2079e-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="2079e-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="2079e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2079e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2079e-105">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="2079e-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="2079e-106">���������</span><span class="sxs-lookup"><span data-stu-id="2079e-106">Parameters</span></span>

 <span data-ttu-id="2079e-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="2079e-107">_ulFlags_</span></span>
  
> <span data-ttu-id="2079e-108">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="2079e-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="2079e-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="2079e-109">The following flag can be set:</span></span>
    
<span data-ttu-id="2079e-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2079e-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="2079e-111">Возвращенная строка — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="2079e-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="2079e-112">Если флаг MAPI_UNICODE не установлен, то строка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="2079e-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="2079e-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="2079e-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="2079e-114">[out] Указатель на строку, содержащую отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="2079e-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2079e-115">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="2079e-115">Return value</span></span>

<span data-ttu-id="2079e-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="2079e-116">S_OK</span></span> 
  
> <span data-ttu-id="2079e-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="2079e-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="2079e-118">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="2079e-118">MFCMAPI reference</span></span>

<span data-ttu-id="2079e-119">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="2079e-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2079e-120">**����**</span><span class="sxs-lookup"><span data-stu-id="2079e-120">**File**</span></span>|<span data-ttu-id="2079e-121">**�������**</span><span class="sxs-lookup"><span data-stu-id="2079e-121">**Function**</span></span>|<span data-ttu-id="2079e-122">**�����������**</span><span class="sxs-lookup"><span data-stu-id="2079e-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2079e-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="2079e-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="2079e-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="2079e-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="2079e-125">Mfcmapi (en) использует метод **IMAPIFormContainer::GetDisplay** для получения имени контейнера формы при ее отображении CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="2079e-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2079e-126">См. также</span><span class="sxs-lookup"><span data-stu-id="2079e-126">See also</span></span>



[<span data-ttu-id="2079e-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2079e-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="2079e-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2079e-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

