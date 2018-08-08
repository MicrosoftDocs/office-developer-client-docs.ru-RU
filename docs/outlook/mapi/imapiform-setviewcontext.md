---
title: IMAPIFormSetViewContext
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIForm.SetViewContext
api_type:
- COM
ms.assetid: a7b10007-42d8-4755-8362-f8ad9a8dad68
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: c1ba49ba1b4deacb684da1411d86ebd4dd19e63f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808890"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="72679-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="72679-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="72679-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="72679-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="72679-105">Устанавливает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="72679-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="72679-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="72679-106">Parameters</span></span>

 <span data-ttu-id="72679-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="72679-107">_pViewContext_</span></span>
  
> <span data-ttu-id="72679-108">[in] Указатель на новый контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="72679-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="72679-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="72679-109">Return value</span></span>

<span data-ttu-id="72679-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="72679-110">S_OK</span></span> 
  
> <span data-ttu-id="72679-111">Контекст представления был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="72679-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="72679-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="72679-112">Remarks</span></span>

<span data-ttu-id="72679-113">Средства просмотра формы вызовите метод **IMAPIForm::SetViewContext** , чтобы установить контекст представления определенной формы как текущий.</span><span class="sxs-lookup"><span data-stu-id="72679-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="72679-114">Форма может иметь только один контекст представления за раз.</span><span class="sxs-lookup"><span data-stu-id="72679-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="72679-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="72679-115">Notes to implementers</span></span>

<span data-ttu-id="72679-116">Большинство серверов формы реализации **SetViewContext** , используя следующий алгоритм:</span><span class="sxs-lookup"><span data-stu-id="72679-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="72679-117">Если контекст представления для формы уже существует, Отмена регистрации формы путем вызова метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с **значение null,** с помощью параметра _pmnvs_ , а затем вызвать контекст представления [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) метод, чтобы уменьшить его счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="72679-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="72679-118">Если новый контекст представления, не равно **null**, вызов **IMAPIViewContext::SetAdviseSink** с помощью параметра _pViewContext_ для настройки нового представления уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="72679-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="72679-119">Если новый контекст представления, не равно **null**, вызовите метод [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) , чтобы определить, какие флаги состояния были установлены.</span><span class="sxs-lookup"><span data-stu-id="72679-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="72679-120">Если новый контекст представления, не равно **null**, сохраните ее и вызвать метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) увеличить счетчик ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="72679-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="72679-121">Обновите все элементы пользовательского интерфейса, которые зависят от контекста представления.</span><span class="sxs-lookup"><span data-stu-id="72679-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="72679-122">В зависимости от состояния флаги, возвращенный из **IMAPIViewContext::GetViewStatus** **SetViewContext** можно также выполнить другие действия.</span><span class="sxs-lookup"><span data-stu-id="72679-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="72679-123">Например если возвращаются флаги VCSTATUS_NEXT и VCSTATUS_PREV, **SetViewContext** можно включить кнопки **Далее** и **Назад** для нового контекста представления.</span><span class="sxs-lookup"><span data-stu-id="72679-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="72679-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="72679-124">MFCMAPI reference</span></span>

<span data-ttu-id="72679-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="72679-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="72679-126">**����**</span><span class="sxs-lookup"><span data-stu-id="72679-126">**File**</span></span>|<span data-ttu-id="72679-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="72679-127">**Function**</span></span>|<span data-ttu-id="72679-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="72679-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="72679-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="72679-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="72679-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="72679-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="72679-131">Mfcmapi (en) использует метод **IMAPIForm::SetViewContext** для установки контекст представления mfcmapi (en) на форме перед отображением формы.</span><span class="sxs-lookup"><span data-stu-id="72679-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="72679-132">См. также</span><span class="sxs-lookup"><span data-stu-id="72679-132">See also</span></span>



[<span data-ttu-id="72679-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="72679-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="72679-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="72679-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="72679-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="72679-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="72679-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="72679-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

