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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32350948"
---
# <a name="imapiformsetviewcontext"></a><span data-ttu-id="747fc-103">IMAPIForm::SetViewContext</span><span class="sxs-lookup"><span data-stu-id="747fc-103">IMAPIForm::SetViewContext</span></span>

  
  
<span data-ttu-id="747fc-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="747fc-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="747fc-105">Устанавливает контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="747fc-105">Establishes a view context for the form.</span></span> 
  
```cpp
HRESULT SetViewContext(
  LPMAPIVIEWCONTEXT pViewContext
);
```

## <a name="parameters"></a><span data-ttu-id="747fc-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="747fc-106">Parameters</span></span>

 <span data-ttu-id="747fc-107">_pViewContext_</span><span class="sxs-lookup"><span data-stu-id="747fc-107">_pViewContext_</span></span>
  
> <span data-ttu-id="747fc-108">[in] Указатель на новый контекст представления для формы.</span><span class="sxs-lookup"><span data-stu-id="747fc-108">[in] A pointer to the new view context for the form.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="747fc-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="747fc-109">Return value</span></span>

<span data-ttu-id="747fc-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="747fc-110">S_OK</span></span> 
  
> <span data-ttu-id="747fc-111">Контекст представления успешно установлен.</span><span class="sxs-lookup"><span data-stu-id="747fc-111">The view context was successfully set.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="747fc-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="747fc-112">Remarks</span></span>

<span data-ttu-id="747fc-113">Посетители форм **звонят методу IMAPIForm::SetViewContext,** чтобы установить определенный контекст представления формы как текущий.</span><span class="sxs-lookup"><span data-stu-id="747fc-113">Form viewers call the **IMAPIForm::SetViewContext** method to establish a particular form view context as current.</span></span> <span data-ttu-id="747fc-114">Одновременно форма может иметь только один контекст представления.</span><span class="sxs-lookup"><span data-stu-id="747fc-114">A form can have only one view context at a time.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="747fc-115">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="747fc-115">Notes to implementers</span></span>

<span data-ttu-id="747fc-116">Большинство серверов форм **реализуют SetViewContext** с помощью следующего алгоритма:</span><span class="sxs-lookup"><span data-stu-id="747fc-116">Most form servers implement **SetViewContext** by using the following algorithm:</span></span> 
  
- <span data-ttu-id="747fc-117">Если контекст представления уже существует для формы, отмените регистрацию формы, вызывая метод [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) с нулью в параметре _pmnvs,_ а затем вызовите метод [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) контекста представления, чтобы понижить количество ссылок. </span><span class="sxs-lookup"><span data-stu-id="747fc-117">If a view context already exists for the form, cancel the form's registration by calling the [IMAPIViewContext::SetAdviseSink](imapiviewcontext-setadvisesink.md) method with **null** in the  _pmnvs_ parameter, and then call the view context's [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method to decrement its reference count.</span></span> 
    
- <span data-ttu-id="747fc-118">Если новый контекст представления не имеет **null,** вызовите **IMAPIViewContext::SetAdviseSink** с помощью параметра  _pViewContext_ для того, чтобы настроить новый окн.</span><span class="sxs-lookup"><span data-stu-id="747fc-118">If the new view context is not **null**, call **IMAPIViewContext::SetAdviseSink** by using the  _pViewContext_ parameter to set up a new view advise sink.</span></span> 
    
- <span data-ttu-id="747fc-119">Если новый контекст представления не имеет **null,** вызовите метод [IMAPIViewContext::GetViewStatus,](imapiviewcontext-getviewstatus.md) чтобы определить, какие флаги состояния были установлены.</span><span class="sxs-lookup"><span data-stu-id="747fc-119">If the new view context is not **null**, call the [IMAPIViewContext::GetViewStatus](imapiviewcontext-getviewstatus.md) method to determine which status flags have been set.</span></span> 
    
- <span data-ttu-id="747fc-120">Если новый контекст представления не имеет **null,** храните его и вызовите его метод [IUnknown::AddRef,](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) чтобы повысьть количество ссылок.</span><span class="sxs-lookup"><span data-stu-id="747fc-120">If the new view context is not **null**, store it and call its [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28VS.85%29.aspx) method to increment its reference count.</span></span> 
    
- <span data-ttu-id="747fc-121">Обновление всех элементов пользовательского интерфейса, которые зависят от контекста представления.</span><span class="sxs-lookup"><span data-stu-id="747fc-121">Update any user interface elements that depend on the view context.</span></span> 
    
<span data-ttu-id="747fc-122">В зависимости от флагов состояния, возвращаемого **из IMAPIViewContext::GetViewStatus,** **SetViewContext** также может выполнять другие действия.</span><span class="sxs-lookup"><span data-stu-id="747fc-122">Depending on the status flags returned from **IMAPIViewContext::GetViewStatus**, **SetViewContext** can also perform other actions.</span></span> <span data-ttu-id="747fc-123">Например, если VCSTATUS_NEXT и VCSTATUS_PREV флаги, **SetViewContext** может включить кнопки **"Далее"** и "Назад" для нового контекста представления. </span><span class="sxs-lookup"><span data-stu-id="747fc-123">For example, if the VCSTATUS_NEXT and VCSTATUS_PREV flags are returned, **SetViewContext** can enable the **Next** and **Previous** buttons for the new view context.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="747fc-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="747fc-124">MFCMAPI reference</span></span>

<span data-ttu-id="747fc-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="747fc-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="747fc-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="747fc-126">**File**</span></span>|<span data-ttu-id="747fc-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="747fc-127">**Function**</span></span>|<span data-ttu-id="747fc-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="747fc-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="747fc-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="747fc-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="747fc-130">CreateAndDisplayNewMailInFolder</span><span class="sxs-lookup"><span data-stu-id="747fc-130">CreateAndDisplayNewMailInFolder</span></span>  <br/> |<span data-ttu-id="747fc-131">MFCMAPI использует метод **IMAPIForm::SetViewContext,** чтобы настроить контекст представления MFCMAPI в форме перед отображением формы.</span><span class="sxs-lookup"><span data-stu-id="747fc-131">MFCMAPI uses the **IMAPIForm::SetViewContext** method to set MFCMAPI's view context on the form before the form is displayed.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="747fc-132">См. также</span><span class="sxs-lookup"><span data-stu-id="747fc-132">See also</span></span>



[<span data-ttu-id="747fc-133">IMAPIViewContext::GetViewStatus</span><span class="sxs-lookup"><span data-stu-id="747fc-133">IMAPIViewContext::GetViewStatus</span></span>](imapiviewcontext-getviewstatus.md)
  
[<span data-ttu-id="747fc-134">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="747fc-134">IMAPIViewContext::SetAdviseSink</span></span>](imapiviewcontext-setadvisesink.md)
  
[<span data-ttu-id="747fc-135">IMAPIForm : IUnknown</span><span class="sxs-lookup"><span data-stu-id="747fc-135">IMAPIForm : IUnknown</span></span>](imapiformiunknown.md)


[<span data-ttu-id="747fc-136">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="747fc-136">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

