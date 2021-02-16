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
ms.openlocfilehash: f0b217372f6b4848f83c993846cd08a81c7098e8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430905"
---
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="c93d4-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="c93d4-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="c93d4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c93d4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c93d4-105">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="c93d4-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="c93d4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c93d4-106">Parameters</span></span>

 <span data-ttu-id="c93d4-107">_ppViewContext_</span><span class="sxs-lookup"><span data-stu-id="c93d4-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="c93d4-108">[out] Указатель на указатель на контекст представления формы.</span><span class="sxs-lookup"><span data-stu-id="c93d4-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c93d4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="c93d4-109">Return value</span></span>

<span data-ttu-id="c93d4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="c93d4-110">S_OK</span></span> 
  
> <span data-ttu-id="c93d4-111">Был успешно возвращен текущий контекст представления формы.</span><span class="sxs-lookup"><span data-stu-id="c93d4-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="c93d4-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="c93d4-112">S_FALSE</span></span> 
  
> <span data-ttu-id="c93d4-113">Контекст представления для формы не существует.</span><span class="sxs-lookup"><span data-stu-id="c93d4-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c93d4-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="c93d4-114">Remarks</span></span>

<span data-ttu-id="c93d4-115">Посетители форм **звонят GetViewContext,** чтобы получить указатель на контекст представления, установленный в предыдущем вызове [IMAPIForm::SetViewContext.](imapiform-setviewcontext.md)</span><span class="sxs-lookup"><span data-stu-id="c93d4-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="c93d4-116">Если до вызова **SetViewContext** не было выполнено, **GetViewContext** устанавливает  _для ppViewContext_ nULL.</span><span class="sxs-lookup"><span data-stu-id="c93d4-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c93d4-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c93d4-117">Notes to implementers</span></span>

<span data-ttu-id="c93d4-118">Скопируйте указатель контекста представления формы в указатель, переданный вызываемой просматриваемой формой в параметре _ppViewContext._</span><span class="sxs-lookup"><span data-stu-id="c93d4-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="c93d4-119">Если форма не имеет контекста представления, установите  _для ppViewContext_ nULL.</span><span class="sxs-lookup"><span data-stu-id="c93d4-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c93d4-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="c93d4-120">MFCMAPI reference</span></span>

<span data-ttu-id="c93d4-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="c93d4-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c93d4-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="c93d4-122">**File**</span></span>|<span data-ttu-id="c93d4-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="c93d4-123">**Function**</span></span>|<span data-ttu-id="c93d4-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="c93d4-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c93d4-125">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="c93d4-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="c93d4-126">OpenMessageNonModal</span><span class="sxs-lookup"><span data-stu-id="c93d4-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="c93d4-127">MFCMAPI использует метод **IMAPIForm::GetViewContext,** чтобы проверить, имеет ли форма контекст представления.</span><span class="sxs-lookup"><span data-stu-id="c93d4-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c93d4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c93d4-128">See also</span></span>



[<span data-ttu-id="c93d4-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c93d4-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="c93d4-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="c93d4-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="c93d4-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c93d4-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

