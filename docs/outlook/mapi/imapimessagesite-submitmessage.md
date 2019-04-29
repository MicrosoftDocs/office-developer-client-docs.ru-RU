---
title: Имапимессажеситесубмитмессаже
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.SubmitMessage
api_type:
- COM
ms.assetid: 6b14c383-8bc6-4e86-bd92-0500272af40d
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 496732e334d2d39672048dd1a02346aaee4b70e1
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417030"
---
# <a name="imapimessagesitesubmitmessage"></a><span data-ttu-id="920af-103">IMAPIMessageSite::SubmitMessage</span><span class="sxs-lookup"><span data-stu-id="920af-103">IMAPIMessageSite::SubmitMessage</span></span>

  
  
<span data-ttu-id="920af-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="920af-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="920af-105">ЗаПрашивает доставку текущего сообщения в очередь на доставку.</span><span class="sxs-lookup"><span data-stu-id="920af-105">Requests that the current message be queued for delivery.</span></span>
  
```cpp
HRESULT SubmitMessage(
  ULONG ulFlags
);
```

## <a name="parameters"></a><span data-ttu-id="920af-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="920af-106">Parameters</span></span>

 <span data-ttu-id="920af-107">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="920af-107">_ulFlags_</span></span>
  
> <span data-ttu-id="920af-108">возврата Битовая маска флагов, определяющих способ отправки сообщения.</span><span class="sxs-lookup"><span data-stu-id="920af-108">[in] A bitmask of flags that controls how a message is submitted.</span></span> <span data-ttu-id="920af-109">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="920af-109">The following flag can be set:</span></span>
    
<span data-ttu-id="920af-110">ФОРЦЕ_СУБМИТ</span><span class="sxs-lookup"><span data-stu-id="920af-110">FORCE_SUBMIT</span></span> 
  
> <span data-ttu-id="920af-111">MAPI должен отправить сообщение, даже если оно не может быть отправлено немедленно.</span><span class="sxs-lookup"><span data-stu-id="920af-111">MAPI should submit the message even if it might not be sent immediately.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="920af-112">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="920af-112">Return value</span></span>

<span data-ttu-id="920af-113">S_OK</span><span class="sxs-lookup"><span data-stu-id="920af-113">S_OK</span></span> 
  
> <span data-ttu-id="920af-114">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="920af-114">The call succeeded and has returned the expected value or values.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="920af-115">Примечания</span><span class="sxs-lookup"><span data-stu-id="920af-115">Remarks</span></span>

<span data-ttu-id="920af-116">Объекты формы вызывают метод **имапимессажесите:: субмитмессаже** , чтобы запросить доставку сообщения в очередь на доставку.</span><span class="sxs-lookup"><span data-stu-id="920af-116">Form objects call the **IMAPIMessageSite::SubmitMessage** method to request that a message be queued for delivery.</span></span> <span data-ttu-id="920af-117">Сайт сообщения должен вызвать метод [иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) перед отправкой сообщения.</span><span class="sxs-lookup"><span data-stu-id="920af-117">The message site should call the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method before submitting the message.</span></span> <span data-ttu-id="920af-118">Сообщение не обязательно было сохранено ранее, так как **субмитмессаже** должно привести к сохранению сообщения, если оно было изменено.</span><span class="sxs-lookup"><span data-stu-id="920af-118">The message does not need to have been previously saved, because **SubmitMessage** should cause the message to be saved if the message has been modified.</span></span> <span data-ttu-id="920af-119">После возврата **субмитмессаже**форма должна проверять текущее сообщение, а затем отклонить его, если он не существует.</span><span class="sxs-lookup"><span data-stu-id="920af-119">After the return of **SubmitMessage**, the form must check for a current message and then dismiss itself if none exists.</span></span> 
  
<span data-ttu-id="920af-120">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="920af-120">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="920af-121">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="920af-121">MFCMAPI reference</span></span>

<span data-ttu-id="920af-122">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="920af-122">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="920af-123">**Файл**</span><span class="sxs-lookup"><span data-stu-id="920af-123">**File**</span></span>|<span data-ttu-id="920af-124">**Функция**</span><span class="sxs-lookup"><span data-stu-id="920af-124">**Function**</span></span>|<span data-ttu-id="920af-125">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="920af-125">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="920af-126">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="920af-126">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="920af-127">Кмимапиформвиевер:: Субмитмессаже</span><span class="sxs-lookup"><span data-stu-id="920af-127">CMyMAPIFormViewer::SubmitMessage</span></span>  <br/> |<span data-ttu-id="920af-128">MFCMAPI использует метод **имапимессажесите:: субмитмессаже** для сохранения сообщения.</span><span class="sxs-lookup"><span data-stu-id="920af-128">MFCMAPI uses the **IMAPIMessageSite::SubmitMessage** method to save the message.</span></span> <span data-ttu-id="920af-129">Сначала он вызывает метод **иперсистмессаже:: хандсоффмессаже** , а затем вызывает **субмитмессаже**.</span><span class="sxs-lookup"><span data-stu-id="920af-129">First, it calls the **IPersistMessage::HandsOffMessage** method, and then it calls **SubmitMessage**.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="920af-130">См. также</span><span class="sxs-lookup"><span data-stu-id="920af-130">See also</span></span>



[<span data-ttu-id="920af-131">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="920af-131">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="920af-132">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="920af-132">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="920af-133">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="920af-133">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="920af-134">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="920af-134">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

