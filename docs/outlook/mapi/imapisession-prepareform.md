---
title: IMAPISessionPrepareForm
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISession.PrepareForm
api_type:
- COM
ms.assetid: 98c0eab1-fd7e-46c3-8619-ccd6dc7cf8f7
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 026a120406b714a50a9191e4761021693a250b94
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809073"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="7ed66-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="7ed66-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="7ed66-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="7ed66-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="7ed66-105">Создает числовое маркера, который использует метод [IMAPISession::ShowForm](imapisession-showform.md) для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="7ed66-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="7ed66-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="7ed66-106">Parameters</span></span>

 <span data-ttu-id="7ed66-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="7ed66-107">_lpInterface_</span></span>
  
> <span data-ttu-id="7ed66-108">[in] Указатель на идентификатор интерфейса (ИД интерфейса), который представляет интерфейс, который будет использоваться для доступа к сообщения.</span><span class="sxs-lookup"><span data-stu-id="7ed66-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="7ed66-109">**Значение null,** результаты тестирования в стандартный интерфейс или [IMessage](imessageimapiprop.md)используется.</span><span class="sxs-lookup"><span data-stu-id="7ed66-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="7ed66-110">Параметр _lpInterface_ должно быть **равно null** или IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="7ed66-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="7ed66-111">_lpMessage_</span><span class="sxs-lookup"><span data-stu-id="7ed66-111">_lpMessage_</span></span>
  
> <span data-ttu-id="7ed66-112">[in] Указатель на сообщение, отображаемое в форме.</span><span class="sxs-lookup"><span data-stu-id="7ed66-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="7ed66-113">_lpulMessageToken_</span><span class="sxs-lookup"><span data-stu-id="7ed66-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="7ed66-114">[out] Указатель на маркер сообщения, который используется для доступа к сообщения с помощью метода **IMAPISession::ShowForm** , на который указывает _lpMessage_.</span><span class="sxs-lookup"><span data-stu-id="7ed66-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="7ed66-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="5">Return value</span></span>

<span data-ttu-id="7ed66-116">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="7ed66-116">S_OK</span></span> 
  
> <span data-ttu-id="7ed66-117">Подготовка формы выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="7ed66-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="7ed66-118">Замечания</span><span class="sxs-lookup"><span data-stu-id="7ed66-118">Remarks</span></span>

<span data-ttu-id="7ed66-119">Метод **IMAPISession::PrepareForm** создает маркер сообщения для сообщения, на который указывает параметр _lpMessage_ и вызывает метод [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) сообщение.</span><span class="sxs-lookup"><span data-stu-id="7ed66-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](http://msdn.microsoft.com/en-us/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="7ed66-120">Этот маркер передается в параметре _ulMessageToken_ **IMAPISession::ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="7ed66-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="7ed66-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="7ed66-121">Notes to callers</span></span>

<span data-ttu-id="7ed66-122">При успешном вызове **PrepareForm** освобождение сообщения, на который указывает _lpMessage_ путем вызова метода [функции IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) до вызова метода **ShowForm**.</span><span class="sxs-lookup"><span data-stu-id="7ed66-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](http://msdn.microsoft.com/en-us/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="7ed66-123">Освобождение сообщения, прежде чем вызывать **ShowForm** можно привести утечки памяти.</span><span class="sxs-lookup"><span data-stu-id="7ed66-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="7ed66-124">Справочник по mfcmapi (en)</span><span class="sxs-lookup"><span data-stu-id="7ed66-124">MFCMAPI reference</span></span>

<span data-ttu-id="7ed66-125">������ ���� mfcmapi (en) ���������� � ������� ����.</span><span class="sxs-lookup"><span data-stu-id="7ed66-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="7ed66-126">**����**</span><span class="sxs-lookup"><span data-stu-id="7ed66-126">**File**</span></span>|<span data-ttu-id="7ed66-127">**�������**</span><span class="sxs-lookup"><span data-stu-id="7ed66-127">**Function**</span></span>|<span data-ttu-id="7ed66-128">**�����������**</span><span class="sxs-lookup"><span data-stu-id="7ed66-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="7ed66-129">MAPIFormFunctions.cpp</span><span class="sxs-lookup"><span data-stu-id="7ed66-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="7ed66-130">OpenMessageModal</span><span class="sxs-lookup"><span data-stu-id="7ed66-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="7ed66-131">Mfcmapi (en) использует метод **IMAPISession::PrepareForm** , а также **IMAPISession::ShowForm**для отображения сообщения в модальную форму.</span><span class="sxs-lookup"><span data-stu-id="7ed66-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="7ed66-132">См. также</span><span class="sxs-lookup"><span data-stu-id="7ed66-132">See also</span></span>



[<span data-ttu-id="7ed66-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="7ed66-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="7ed66-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="7ed66-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="7ed66-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="7ed66-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

