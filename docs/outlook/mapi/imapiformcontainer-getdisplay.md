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
ms.openlocfilehash: 66e23d73af53b05295bf2cbcd8c604ab3545bbca
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22573140"
---
# <a name="imapiformcontainergetdisplay"></a><span data-ttu-id="55694-103">IMAPIFormContainer::GetDisplay</span><span class="sxs-lookup"><span data-stu-id="55694-103">IMAPIFormContainer::GetDisplay</span></span>

  
  
<span data-ttu-id="55694-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="55694-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="55694-105">Возвращает отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="55694-105">Returns the display name of a form container.</span></span>
  
```cpp
HRESULT GetDisplay(
  ULONG ulFlags,
  LPSTR FAR * pszDisplayName
);
```

## <a name="parameters"></a><span data-ttu-id="55694-106">���������</span><span class="sxs-lookup"><span data-stu-id="55694-106">Parameters</span></span>

 <span data-ttu-id="55694-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="55694-107">_ulFlags_</span></span>
  
> <span data-ttu-id="55694-108">[in] Битовая маска флаги, определяющее тип возвращаемой строки.</span><span class="sxs-lookup"><span data-stu-id="55694-108">[in] A bitmask of flags that controls the type of the returned string.</span></span> <span data-ttu-id="55694-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="55694-109">The following flag can be set:</span></span>
    
<span data-ttu-id="55694-110">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="55694-110">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="55694-111">Возвращенная строка — в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="55694-111">The returned string is in Unicode format.</span></span> <span data-ttu-id="55694-112">Если флаг MAPI_UNICODE не установлен, то строка будет в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="55694-112">If the MAPI_UNICODE flag is not set, the string is in ANSI format.</span></span>
    
 <span data-ttu-id="55694-113">_pszDisplayName_</span><span class="sxs-lookup"><span data-stu-id="55694-113">_pszDisplayName_</span></span>
  
> <span data-ttu-id="55694-114">[out] Указатель на строку, содержащую отображаемое имя контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="55694-114">[out] A pointer to a string that contains the display name of the form container.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="55694-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="55694-115">Return value</span></span>

<span data-ttu-id="55694-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="55694-116">S_OK</span></span> 
  
> <span data-ttu-id="55694-117">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="55694-117">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="55694-118">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="55694-118">MFCMAPI reference</span></span>

<span data-ttu-id="55694-119">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="55694-119">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="55694-120">**Файл**</span><span class="sxs-lookup"><span data-stu-id="55694-120">**File**</span></span>|<span data-ttu-id="55694-121">**Функция**</span><span class="sxs-lookup"><span data-stu-id="55694-121">**Function**</span></span>|<span data-ttu-id="55694-122">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="55694-122">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="55694-123">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="55694-123">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="55694-124">CFormContainerDlg::CFormContainerDlg</span><span class="sxs-lookup"><span data-stu-id="55694-124">CFormContainerDlg::CFormContainerDlg</span></span>  <br/> |<span data-ttu-id="55694-125">Mfcmapi (en) использует метод **IMAPIFormContainer::GetDisplay** для получения имени контейнера формы при ее отображении CFormContainerDlg.</span><span class="sxs-lookup"><span data-stu-id="55694-125">MFCMAPI uses the **IMAPIFormContainer::GetDisplay** method to get the name of the form container when it renders CFormContainerDlg.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="55694-126">См. также</span><span class="sxs-lookup"><span data-stu-id="55694-126">See also</span></span>



[<span data-ttu-id="55694-127">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="55694-127">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="55694-128">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="55694-128">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

