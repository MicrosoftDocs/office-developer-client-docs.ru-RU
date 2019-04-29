---
title: Имапиформжетвиевконтекст
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
# <a name="imapiformgetviewcontext"></a><span data-ttu-id="2a10c-103">IMAPIForm::GetViewContext</span><span class="sxs-lookup"><span data-stu-id="2a10c-103">IMAPIForm::GetViewContext</span></span>

  
  
<span data-ttu-id="2a10c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a10c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a10c-105">Возвращает текущий контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="2a10c-105">Returns the current view context for the form.</span></span> 
  
```cpp
HRESULT GetViewContext(
  LPMAPIVIEWCONTEXT FAR * ppViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="2a10c-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="2a10c-106">Parameters</span></span>

 <span data-ttu-id="2a10c-107">_Ппвиевконтекст_</span><span class="sxs-lookup"><span data-stu-id="2a10c-107">_ppViewContext_</span></span>
  
> <span data-ttu-id="2a10c-108">вышли Указатель на указатель на контекст представления формы.</span><span class="sxs-lookup"><span data-stu-id="2a10c-108">[out] A pointer to a pointer to the form's view context.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="2a10c-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="2a10c-109">Return value</span></span>

<span data-ttu-id="2a10c-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="2a10c-110">S_OK</span></span> 
  
> <span data-ttu-id="2a10c-111">Контекст текущего представления формы успешно возвращен.</span><span class="sxs-lookup"><span data-stu-id="2a10c-111">The form's current view context was successfully returned.</span></span> 
    
<span data-ttu-id="2a10c-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="2a10c-112">S_FALSE</span></span> 
  
> <span data-ttu-id="2a10c-113">Контекст представления для формы отсутствует.</span><span class="sxs-lookup"><span data-stu-id="2a10c-113">There is no view context for the form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="2a10c-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="2a10c-114">Remarks</span></span>

<span data-ttu-id="2a10c-115">Средства просмотра форм вызывают **жетвиевконтекст** , чтобы получить указатель на контекст представления, установленный в предыдущем вызове [Имапиформ:: сетвиевконтекст](imapiform-setviewcontext.md).</span><span class="sxs-lookup"><span data-stu-id="2a10c-115">Form viewers call **GetViewContext** to obtain a pointer to the view context established in a previous call to [IMAPIForm::SetViewContext](imapiform-setviewcontext.md).</span></span> <span data-ttu-id="2a10c-116">Если в **сетвиевконтекст**не был выполнен вызов, **Жетвиевконтекст** ЗАДАЕТ для _ппвиевконтекст_ значение null.</span><span class="sxs-lookup"><span data-stu-id="2a10c-116">If no prior call has been made to **SetViewContext**, **GetViewContext** sets  _ppViewContext_ to NULL.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="2a10c-117">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="2a10c-117">Notes to implementers</span></span>

<span data-ttu-id="2a10c-118">Скопируйте указатель контекста представления формы в указатель, переданный с помощью средства просмотра форм, в параметр _ппвиевконтекст_ .</span><span class="sxs-lookup"><span data-stu-id="2a10c-118">Copy your form's view context pointer into the pointer passed in by the calling form viewer in the  _ppViewContext_ parameter.</span></span> <span data-ttu-id="2a10c-119">Если у формы нет контекста представления, задайте для параметра _ППВИЕВКОНТЕКСТ_ значение null.</span><span class="sxs-lookup"><span data-stu-id="2a10c-119">If the form does not have a view context, set  _ppViewContext_ to NULL.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="2a10c-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="2a10c-120">MFCMAPI reference</span></span>

<span data-ttu-id="2a10c-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="2a10c-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="2a10c-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="2a10c-122">**File**</span></span>|<span data-ttu-id="2a10c-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="2a10c-123">**Function**</span></span>|<span data-ttu-id="2a10c-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="2a10c-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="2a10c-125">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="2a10c-125">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="2a10c-126">Опенмессаженонмодал</span><span class="sxs-lookup"><span data-stu-id="2a10c-126">OpenMessageNonModal</span></span>  <br/> |<span data-ttu-id="2a10c-127">MFCMAPI использует метод **имапиформ:: жетвиевконтекст** , чтобы проверить, имеет ли форма контекст представления.</span><span class="sxs-lookup"><span data-stu-id="2a10c-127">MFCMAPI uses the **IMAPIForm::GetViewContext** method to check whether a form has a view context.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="2a10c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="2a10c-128">See also</span></span>



[<span data-ttu-id="2a10c-129">IMAPIViewContext : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a10c-129">IMAPIViewContext : IUnknown</span></span>](imapiviewcontextiunknown.md)
  
[<span data-ttu-id="2a10c-130">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="2a10c-130">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="2a10c-131">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="2a10c-131">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

