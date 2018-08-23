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
ms.openlocfilehash: 555bb4820dc36934fb28197b7e222633a5248125
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22583185"
---
# <a name="imapiviewcontextsetadvisesink"></a><span data-ttu-id="c1744-103">IMAPIViewContext::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c1744-103">IMAPIViewContext::SetAdviseSink</span></span>

  
  
<span data-ttu-id="c1744-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c1744-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c1744-105">Управляет формы регистрации для получения уведомлений об изменениях в средстве просмотра.</span><span class="sxs-lookup"><span data-stu-id="c1744-105">Manages a form's registration to receive notifications about changes in the viewer.</span></span> 
  
```cpp
HRESULT SetAdviseSink(
LPMAPIFORMADVISESINK pmvns
);
```

## <a name="parameters"></a><span data-ttu-id="c1744-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="c1744-106">Parameters</span></span>

 <span data-ttu-id="c1744-107">_pmvns_</span><span class="sxs-lookup"><span data-stu-id="c1744-107">_pmvns_</span></span>
  
> <span data-ttu-id="c1744-108">[in] Указатель на форме уведомить приемник object или значение NULL.</span><span class="sxs-lookup"><span data-stu-id="c1744-108">[in] Pointer to a form advise sink object or NULL.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="c1744-109">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="c1744-109">Return value</span></span>

<span data-ttu-id="c1744-110">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="c1744-110">S_OK</span></span> 
  
> <span data-ttu-id="c1744-111">Регистрация или отмены для уведомления формы выполнено успешно.</span><span class="sxs-lookup"><span data-stu-id="c1744-111">The registration or cancellation for form notification succeeded.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="c1744-112">Замечания</span><span class="sxs-lookup"><span data-stu-id="c1744-112">Remarks</span></span>

<span data-ttu-id="c1744-113">Объекты формы вызовите метод **IMAPIViewContext::SetAdviseSink** , чтобы зарегистрировать сведения об изменениях в форме просмотра или отменить предварительная регистрация.</span><span class="sxs-lookup"><span data-stu-id="c1744-113">Form objects call the **IMAPIViewContext::SetAdviseSink** method to either register to learn about changes in the form viewer or cancel a prior registration.</span></span> <span data-ttu-id="c1744-114">Когда _pmvns_ имеет значение NULL, форма, где требуется реализовать для отмены регистрации.</span><span class="sxs-lookup"><span data-stu-id="c1744-114">When  _pmvns_ is set to NULL, the form wants to cancel a registration.</span></span> <span data-ttu-id="c1744-115">При _pmvns_ указывает на допустимый формы уведомить приемник, формы требуется зарегистрировать для уведомления.</span><span class="sxs-lookup"><span data-stu-id="c1744-115">When  _pmvns_ points to a valid form advise sink, the form wants to register for future notifications.</span></span> 
  
## <a name="notes-to-implementers"></a><span data-ttu-id="c1744-116">Примечания для исполнителей</span><span class="sxs-lookup"><span data-stu-id="c1744-116">Notes to implementers</span></span>

<span data-ttu-id="c1744-117">Когда **SetAdviseSink** включает в себя формы уведомить указателя приемника, продолжайте ссылки на нее до другого **SetAdviseSink** вызов Отмена уведомлений.</span><span class="sxs-lookup"><span data-stu-id="c1744-117">When **SetAdviseSink** includes a form advise sink pointer, keep a reference to it until another **SetAdviseSink** call is made to cancel notification.</span></span> <span data-ttu-id="c1744-118">Отправьте уведомление, когда происходит изменение в вашей средства просмотра и при загрузке нового сообщения.</span><span class="sxs-lookup"><span data-stu-id="c1744-118">Send a notification when a change occurs in your viewer and when you are loading a new message.</span></span> 
  
<span data-ttu-id="c1744-119">Для получения дополнительных сведений см [Отправка и получение уведомлений формы](sending-and-receiving-form-notifications.md).</span><span class="sxs-lookup"><span data-stu-id="c1744-119">For more information, see [Sending and Receiving Form Notifications](sending-and-receiving-form-notifications.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="c1744-120">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="c1744-120">MFCMAPI reference</span></span>

<span data-ttu-id="c1744-121">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="c1744-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="c1744-122">**����**</span><span class="sxs-lookup"><span data-stu-id="c1744-122">**File**</span></span>|<span data-ttu-id="c1744-123">**�������**</span><span class="sxs-lookup"><span data-stu-id="c1744-123">**Function**</span></span>|<span data-ttu-id="c1744-124">**�����������**</span><span class="sxs-lookup"><span data-stu-id="c1744-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="c1744-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="c1744-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="c1744-126">CMyMAPIFormViewer::SetAdviseSink</span><span class="sxs-lookup"><span data-stu-id="c1744-126">CMyMAPIFormViewer::SetAdviseSink</span></span>  <br/> |<span data-ttu-id="c1744-127">Mfcmapi (en) реализован метод **IMAPIViewContext::SetAdviseSink** в этой функции.</span><span class="sxs-lookup"><span data-stu-id="c1744-127">MFCMAPI implements the **IMAPIViewContext::SetAdviseSink** method in this function.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="c1744-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c1744-128">See also</span></span>



[<span data-ttu-id="c1744-129">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="c1744-129">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

