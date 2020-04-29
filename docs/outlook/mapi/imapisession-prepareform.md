---
title: имаписессионпрепареформ
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
ms.openlocfilehash: 3d8b1901123743b25b5bb9df174b297398c953b8
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32335768"
---
# <a name="imapisessionprepareform"></a><span data-ttu-id="1d12a-103">IMAPISession::PrepareForm</span><span class="sxs-lookup"><span data-stu-id="1d12a-103">IMAPISession::PrepareForm</span></span>

  
  
<span data-ttu-id="1d12a-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1d12a-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1d12a-105">Создает числовой маркер, который метод [IMAPISession:: шовформ](imapisession-showform.md) использует для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="1d12a-105">Creates a numeric token that the [IMAPISession::ShowForm](imapisession-showform.md) method uses to access a message.</span></span> 
  
```cpp
HRESULT PrepareForm(
  LPCIID lpInterface,
  LPMESSAGE lpMessage,
  ULONG FAR * lpulMessageToken
);
```

## <a name="parameters"></a><span data-ttu-id="1d12a-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="1d12a-106">Parameters</span></span>

 <span data-ttu-id="1d12a-107">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="1d12a-107">_lpInterface_</span></span>
  
> <span data-ttu-id="1d12a-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="1d12a-108">[in] A pointer to the interface identifier (IID) that represents the interface to be used to access the message.</span></span> <span data-ttu-id="1d12a-109">Передача **значений NULL** в стандартный интерфейс (или [iMessage](imessageimapiprop.md)) используется.</span><span class="sxs-lookup"><span data-stu-id="1d12a-109">Passing **null** results in the standard interface, or [IMessage](imessageimapiprop.md), being used.</span></span> <span data-ttu-id="1d12a-110">Параметр _лпинтерфаце_ должен иметь **значение NULL** или IID_IMessage.</span><span class="sxs-lookup"><span data-stu-id="1d12a-110">The  _lpInterface_ parameter must be **null** or IID_IMessage.</span></span> 
    
 <span data-ttu-id="1d12a-111">_лпмессаже_</span><span class="sxs-lookup"><span data-stu-id="1d12a-111">_lpMessage_</span></span>
  
> <span data-ttu-id="1d12a-112">возврата Указатель на сообщение, отображаемое в форме.</span><span class="sxs-lookup"><span data-stu-id="1d12a-112">[in] A pointer to the message to be displayed in the form.</span></span>
    
 <span data-ttu-id="1d12a-113">_лпулмессажетокен_</span><span class="sxs-lookup"><span data-stu-id="1d12a-113">_lpulMessageToken_</span></span>
  
> <span data-ttu-id="1d12a-114">вышли Указатель на маркер сообщения, используемый методом **IMAPISession:: шовформ** для доступа к сообщению, на которое указывает _лпмессаже_.</span><span class="sxs-lookup"><span data-stu-id="1d12a-114">[out] A pointer to a message token, which is used by the **IMAPISession::ShowForm** method to access the message pointed to by  _lpMessage_.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="1d12a-115">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="1d12a-115">Return value</span></span>

<span data-ttu-id="1d12a-116">S_OK</span><span class="sxs-lookup"><span data-stu-id="1d12a-116">S_OK</span></span> 
  
> <span data-ttu-id="1d12a-117">Подготовка формы выполнена успешно.</span><span class="sxs-lookup"><span data-stu-id="1d12a-117">The form preparation was successful.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="1d12a-118">Примечания</span><span class="sxs-lookup"><span data-stu-id="1d12a-118">Remarks</span></span>

<span data-ttu-id="1d12a-119">Метод **IMAPISession::P репареформ** создает маркер сообщения для сообщения, на который указывает параметр _лпмессаже_ , и вызывает метод [IUnknown:: AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) сообщения.</span><span class="sxs-lookup"><span data-stu-id="1d12a-119">The **IMAPISession::PrepareForm** method creates a message token for the message pointed to by the  _lpMessage_ parameter and calls the message's [IUnknown::AddRef](https://msdn.microsoft.com/library/ms691379%28v=VS.85%29.aspx) method.</span></span> <span data-ttu-id="1d12a-120">Этот маркер передается в параметре _улмессажетокен_ в **IMAPISession:: шовформ**.</span><span class="sxs-lookup"><span data-stu-id="1d12a-120">This token is passed in the  _ulMessageToken_ parameter to **IMAPISession::ShowForm**.</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="1d12a-121">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="1d12a-121">Notes to callers</span></span>

<span data-ttu-id="1d12a-122">Если вызов **препареформ** выполнен успешно, освободите сообщение, на которое указывает _лпмессаже_ , вызвав его метод [IUnknown:: Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) перед вызовом **шовформ**.</span><span class="sxs-lookup"><span data-stu-id="1d12a-122">If the call to **PrepareForm** succeeds, release the message pointed to by  _lpMessage_ by calling its [IUnknown::Release](https://msdn.microsoft.com/library/ms682317%28v=VS.85%29.aspx) method before you call **ShowForm**.</span></span> <span data-ttu-id="1d12a-123">Сбой при освобождении сообщения перед вызовом **шовформ** может привести к утечке памяти.</span><span class="sxs-lookup"><span data-stu-id="1d12a-123">Failure to release the message before you call **ShowForm** can cause memory leaks.</span></span> 
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="1d12a-124">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="1d12a-124">MFCMAPI reference</span></span>

<span data-ttu-id="1d12a-125">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="1d12a-125">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="1d12a-126">**Файл**</span><span class="sxs-lookup"><span data-stu-id="1d12a-126">**File**</span></span>|<span data-ttu-id="1d12a-127">**Функция**</span><span class="sxs-lookup"><span data-stu-id="1d12a-127">**Function**</span></span>|<span data-ttu-id="1d12a-128">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="1d12a-128">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="1d12a-129">Мапиформфунктионс. cpp</span><span class="sxs-lookup"><span data-stu-id="1d12a-129">MAPIFormFunctions.cpp</span></span>  <br/> |<span data-ttu-id="1d12a-130">опенмессажемодал</span><span class="sxs-lookup"><span data-stu-id="1d12a-130">OpenMessageModal</span></span>  <br/> |<span data-ttu-id="1d12a-131">MFCMAPI использует метод **IMAPISession::P репареформ** вместе с **IMAPISession:: шовформ**, чтобы отобразить сообщение в модальной форме.</span><span class="sxs-lookup"><span data-stu-id="1d12a-131">MFCMAPI uses the **IMAPISession::PrepareForm** method, along with **IMAPISession::ShowForm**, to display a message in a modal form.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="1d12a-132">См. также</span><span class="sxs-lookup"><span data-stu-id="1d12a-132">See also</span></span>



[<span data-ttu-id="1d12a-133">IMAPISession::ShowForm</span><span class="sxs-lookup"><span data-stu-id="1d12a-133">IMAPISession::ShowForm</span></span>](imapisession-showform.md)
  
[<span data-ttu-id="1d12a-134">IMAPISession: IUnknown</span><span class="sxs-lookup"><span data-stu-id="1d12a-134">IMAPISession : IUnknown</span></span>](imapisessioniunknown.md)


[<span data-ttu-id="1d12a-135">Mfcmapi (en) � �������� ������� ����</span><span class="sxs-lookup"><span data-stu-id="1d12a-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)

