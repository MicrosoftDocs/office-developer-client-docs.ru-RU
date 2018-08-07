---
title: IMAPIFormGetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.GetViewContext
api_type:
- COM
ms.assetid: c6938986-a9f9-4ef4-9655-ded55b7357db
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 2c463252aa029ac4c7cb2fac6e962a5d8af31b97
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808879"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="8f177-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="8f177-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="8f177-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="8f177-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="8f177-105">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="8f177-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="8f177-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="8f177-106">Parameters</span></span>

 <span data-ttu-id="8f177-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="8f177-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="8f177-108">[out] Указатель на указатель на контекст представления формы.</span><span class="sxs-lookup"><span data-stu-id="8f177-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="8f177-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="9">Return value</span></span>

<span data-ttu-id="8f177-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="8f177-110">S_OK</span></span> 
  
> <span data-ttu-id="8f177-111">Текущий контекст представления формы успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="8f177-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="8f177-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="8f177-112">S_FALSE</span></span> 
  
> <span data-ttu-id="8f177-113">Отсутствует контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="8f177-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="8f177-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="8f177-114">Remarks</span></span>

<span data-ttu-id="8f177-115">Средства просмотра формы вызов **GetViewContext** для получения указателя контекст представления, указанной в предыдущем вызов [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="8f177-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="8f177-116">Если предыдущий вызов не выполнена в **SetViewContext**, **GetViewContext** задает _ppViewContext_ значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8f177-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="8f177-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="8f177-117">Notes to implementers</span></span>

<span data-ttu-id="8f177-118">Скопируйте указатель контекст представления формы в указатель, переданный по вызову средства просмотра формы с помощью параметра _ppViewContext_ .</span><span class="sxs-lookup"><span data-stu-id="8f177-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="8f177-119">Если форма не имеет контекст представления, необходимо задайте _ppViewContext_ значение NULL.</span><span class="sxs-lookup"><span data-stu-id="8f177-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="8f177-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="8f177-120">MFCMAPI reference</span></span>

<span data-ttu-id="8f177-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="8f177-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="8f177-122">**����**</span><span class="sxs-lookup"><span data-stu-id="8f177-122">**File**</span></span>|<span data-ttu-id="8f177-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="8f177-123">**Function**</span></span>|<span data-ttu-id="8f177-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="8f177-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="8f177-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="8f177-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="8f177-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="8f177-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="8f177-127">Mfcmapi (en) использует метод **IMAPIForm::GetViewContext** , чтобы проверить наличие контекст представления.</span><span class="sxs-lookup"><span data-stu-id="8f177-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="8f177-128">См. также</span><span class="sxs-lookup"><span data-stu-id="8f177-128">See also</span></span>



[<span data-ttu-id="8f177-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f177-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="8f177-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="8f177-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="8f177-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="8f177-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

