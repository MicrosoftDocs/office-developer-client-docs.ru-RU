---
title: IMAPIFormContainerRemoveForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIFormContainer.RemoveForm
api_type:
- COM
ms.assetid: 7f851ce8-bd01-4ea5-86e0-e44323cc0aab
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 0d2c908f86ccd66ffd3a2eb2506d129ee2a14d48
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808896"
---
# <a name="imapiformcontainerremoveform"></a><span data-ttu-id="a2b7d-103">IMAPIFormContainer::RemoveForm</span><span class="sxs-lookup"><span data-stu-id="a2b7d-103">IMAPIFormContainer::RemoveForm</span></span>

  
  
<span data-ttu-id="a2b7d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a2b7d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a2b7d-105">Удаление определенной формы из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-105">Removes a particular form from a form container.</span></span>
  
```cpp
HRESULT RemoveForm(
  LPCSTR szMessageClass
);
```

## <a name="parameters"></a><span data-ttu-id="a2b7d-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="a2b7d-106">Parameters</span></span>

 <span data-ttu-id="a2b7d-107">_szMessageClass_</span><span class="sxs-lookup"><span data-stu-id="a2b7d-107">_szMessageClass_</span></span>
  
> <span data-ttu-id="a2b7d-108">[in] Строка, имена класса сообщений для формы для удаления из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-108">[in] A string that names the message class of the form to be removed from the form container.</span></span> <span data-ttu-id="a2b7d-109">Имена классов сообщений всегда являются строками ANSI, никогда не Юникод.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-109">Message class names are always ANSI strings, never Unicode.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="a2b7d-110">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="a2b7d-110">Return value</span></span>

<span data-ttu-id="a2b7d-111">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="a2b7d-111">S_OK</span></span> 
  
> <span data-ttu-id="a2b7d-112">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-112">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="a2b7d-113">MAPI_E_NOT_FOUND</span><span class="sxs-lookup"><span data-stu-id="a2b7d-113">MAPI_E_NOT_FOUND</span></span> 
  
> <span data-ttu-id="a2b7d-114">Класс сообщения, переданной в параметре _szMessageClass_ не соответствует класса сообщений для любой формы в контейнере формы.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-114">The message class passed in the  _szMessageClass_ parameter does not match the message class of any form in the form container.</span></span> 
    
## <a name="mfcmapi-reference"></a><span data-ttu-id="a2b7d-115">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="a2b7d-115">MFCMAPI reference</span></span>

<span data-ttu-id="a2b7d-116">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-116">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="a2b7d-117">**����**</span><span class="sxs-lookup"><span data-stu-id="a2b7d-117">**File**</span></span>|<span data-ttu-id="a2b7d-118">**�������**</span><span class="sxs-lookup"><span data-stu-id="a2b7d-118">**Function**</span></span>|<span data-ttu-id="a2b7d-119">**�����������**</span><span class="sxs-lookup"><span data-stu-id="a2b7d-119">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="a2b7d-120">FormContainerDlg.cpp</span><span class="sxs-lookup"><span data-stu-id="a2b7d-120">FormContainerDlg.cpp</span></span>  <br/> |<span data-ttu-id="a2b7d-121">CFormContainerDlg::OnDeleteSelectedItem</span><span class="sxs-lookup"><span data-stu-id="a2b7d-121">CFormContainerDlg::OnDeleteSelectedItem</span></span>  <br/> |<span data-ttu-id="a2b7d-122">Mfcmapi (en) использует метод **IMAPIFormContainer::RemoveForm** для удаления формы из контейнера формы.</span><span class="sxs-lookup"><span data-stu-id="a2b7d-122">MFCMAPI uses the **IMAPIFormContainer::RemoveForm** method to delete a form from a form container.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="a2b7d-123">См. также</span><span class="sxs-lookup"><span data-stu-id="a2b7d-123">See also</span></span>



[<span data-ttu-id="a2b7d-124">IMAPIFormContainer : IUnknown</span><span class="sxs-lookup"><span data-stu-id="a2b7d-124">IMAPIFormContainer : IUnknown</span></span>](imapiformcontaineriunknown.md)


[<span data-ttu-id="a2b7d-125">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="a2b7d-125">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

