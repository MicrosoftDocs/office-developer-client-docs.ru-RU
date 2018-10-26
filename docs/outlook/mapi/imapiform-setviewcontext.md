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
ms.openlocfilehash: 81d99b2bbe6ef7914a4b7d253a3472026872260d
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25384313"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="510aa-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="510aa-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="510aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="510aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="510aa-105">Устанавливает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="510aa-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="510aa-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="510aa-106">Parameters</span></span>

 <span data-ttu-id="510aa-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="510aa-107">_pViewContext_</span></span>
  
> <span data-ttu-id="510aa-108">[in] Указатель на новый контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="510aa-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="510aa-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="510aa-109">Return value</span></span>

<span data-ttu-id="510aa-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="510aa-110">S_OK</span></span> 
  
> <span data-ttu-id="510aa-111">Контекст представления был успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="510aa-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="510aa-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="510aa-112">Remarks</span></span>

<span data-ttu-id="510aa-113">Средства просмотра формы вызовите метод **IMAPIForm::SetViewContext** , чтобы установить контекст представления определенной формы как текущий.</span><span class="sxs-lookup"><span data-stu-id="510aa-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="510aa-114">Форма может иметь только один контекст представления за раз.</span><span class="sxs-lookup"><span data-stu-id="510aa-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="510aa-115">Примечания для реализующих</span><span class="sxs-lookup"><span data-stu-id="510aa-115">Notes to implementers</span></span>

<span data-ttu-id="510aa-116">Большинство серверов формы реализации **SetViewContext** , используя следующий алгоритм:</span><span class="sxs-lookup"><span data-stu-id="510aa-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="510aa-117">Если контекст представления для формы уже существует, Отмена регистрации формы путем вызова метода [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с **значение null,** с помощью параметра _pmnvs_ , а затем вызвать контекст представления [функции IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) метод, чтобы уменьшить его счетчик ссылок.</span><span class="sxs-lookup"><span data-stu-id="510aa-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="510aa-118">Если новый контекст представления, не равно **null**, вызов **IMAPIViewContext::SetAdviseSink** с помощью параметра _pViewContext_ для настройки нового представления уведомить приемника.</span><span class="sxs-lookup"><span data-stu-id="510aa-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="510aa-119">Если новый контекст представления, не равно **null**, вызовите метод [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) , чтобы определить, какие флаги состояния были установлены.</span><span class="sxs-lookup"><span data-stu-id="510aa-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="510aa-120">Если новый контекст представления, не равно **null**, сохраните ее и вызвать метод [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) увеличить счетчик ссылок на него.</span><span class="sxs-lookup"><span data-stu-id="510aa-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="510aa-121">Обновите все элементы пользовательского интерфейса, которые зависят от контекста представления.</span><span class="sxs-lookup"><span data-stu-id="510aa-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="510aa-122">В зависимости от состояния флаги, возвращенный из **IMAPIViewContext::GetViewStatus** **SetViewContext** можно также выполнить другие действия.</span><span class="sxs-lookup"><span data-stu-id="510aa-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="510aa-123">Например если возвращаются флаги VCSTATUS_NEXT и VCSTATUS_PREV, **SetViewContext** можно включить кнопки **Далее** и **Назад** для нового контекста представления.</span><span class="sxs-lookup"><span data-stu-id="510aa-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="510aa-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="510aa-124">MFCMAPI reference</span></span>

<span data-ttu-id="510aa-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="510aa-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="510aa-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="510aa-126">**File**</span></span>|<span data-ttu-id="510aa-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="510aa-127">**Function**</span></span>|<span data-ttu-id="510aa-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="510aa-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="510aa-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="510aa-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="510aa-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="510aa-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="510aa-131">Mfcmapi (en) использует метод **IMAPIForm::SetViewContext** для установки контекст представления mfcmapi (en) на форме перед отображением формы.</span><span class="sxs-lookup"><span data-stu-id="510aa-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="510aa-132">См. также</span><span class="sxs-lookup"><span data-stu-id="510aa-132">See also</span></span>



[<span data-ttu-id="510aa-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="510aa-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="510aa-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="510aa-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="510aa-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="510aa-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="510aa-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="510aa-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

