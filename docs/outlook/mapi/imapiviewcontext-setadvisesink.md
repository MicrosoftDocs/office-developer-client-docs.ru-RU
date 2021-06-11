---
title: IMAPIViewContextSetAdviseSink
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIViewContext.SetAdviseSink
api_type:
- COM
ms.assetid: 4799084a-b5d1-48c3-a889-b2f0e9d68c30
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 7ee641214e1eaae667af356fd8dbe51ff7dc7982
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33419396"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="ab84b-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ab84b-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="ab84b-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ab84b-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ab84b-105">Управляет регистрацией формы для получения уведомлений об изменениях в зрителье.</span><span class="sxs-lookup"><span data-stu-id="ab84b-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="ab84b-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="ab84b-106">Parameters</span></span>

 <span data-ttu-id="ab84b-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="ab84b-107">_pmvns_</span></span>
  
> <span data-ttu-id="ab84b-108">[in] Указатель на форму советую объекту раковины или NULL.</span><span class="sxs-lookup"><span data-stu-id="ab84b-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="ab84b-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="ab84b-109">Return value</span></span>

<span data-ttu-id="ab84b-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="ab84b-110">S_OK</span></span> 
  
> <span data-ttu-id="ab84b-111">Регистрация или отмена уведомления о форме увенчались успехом.</span><span class="sxs-lookup"><span data-stu-id="ab84b-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="ab84b-112">Примечания</span><span class="sxs-lookup"><span data-stu-id="ab84b-112">Remarks</span></span>

<span data-ttu-id="ab84b-113">Объекты формы звонят по методу **IMAPIViewContext::SetAdviseSink,** чтобы зарегистрироваться, чтобы узнать об изменениях в виде просмотра или отменить предварительную регистрацию.</span><span class="sxs-lookup"><span data-stu-id="ab84b-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="ab84b-114">Когда  _pmvns_ задают NULL, форма хочет отменить регистрацию.</span><span class="sxs-lookup"><span data-stu-id="ab84b-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="ab84b-115">Когда  _pmvns указывает_ на допустимую форму, советую раковину, форма хочет зарегистрироваться для будущих уведомлений.</span><span class="sxs-lookup"><span data-stu-id="ab84b-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="ab84b-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="ab84b-116">Notes to implementers</span></span>

<span data-ttu-id="ab84b-117">Когда **SetAdviseSink** включает указатель на раковину формы, сохраняйте ссылку на нее, пока не будет сделан другой вызов **SetAdviseSink** для отмены уведомления.</span><span class="sxs-lookup"><span data-stu-id="ab84b-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="ab84b-118">Отправьте уведомление о том, когда в вашем зрителье происходит изменение и когда вы загружаете новое сообщение.</span><span class="sxs-lookup"><span data-stu-id="ab84b-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="ab84b-119">Дополнительные сведения см. в [рублях Отправка и получение уведомлений о форме.](sending-and-receiving-form-notifications.md)</span><span class="sxs-lookup"><span data-stu-id="ab84b-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="ab84b-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="ab84b-120">MFCMAPI reference</span></span>

<span data-ttu-id="ab84b-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="ab84b-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="ab84b-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="ab84b-122">**File**</span></span>|<span data-ttu-id="ab84b-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="ab84b-123">**Function**</span></span>|<span data-ttu-id="ab84b-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="ab84b-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ab84b-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="ab84b-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="ab84b-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="ab84b-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="ab84b-127">MFCMAPI реализует метод **IMAPIViewContext::SetAdviseSink** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="ab84b-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ab84b-128">См. также</span><span class="sxs-lookup"><span data-stu-id="ab84b-128">See also</span></span>



[<span data-ttu-id="ab84b-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="ab84b-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

