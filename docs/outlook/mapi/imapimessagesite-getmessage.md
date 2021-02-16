---
title: IMAPIMessageSiteGetMessage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPIMessageSite.GetMessage
api_type:
- COM
ms.assetid: 49d12c49-84f8-44ac-bc4a-2ee44a46f8c1
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 03dd0553d0203585850ac5c4f8c91c86ef60236a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33409029"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="83fd9-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="83fd9-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="83fd9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="83fd9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="83fd9-105">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="83fd9-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="83fd9-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="83fd9-106">Parameters</span></span>

 <span data-ttu-id="83fd9-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="83fd9-107">_ppmsg_</span></span>
  
> <span data-ttu-id="83fd9-108">[out] Указатель на указатель на возвращенный интерфейс сообщения.</span><span class="sxs-lookup"><span data-stu-id="83fd9-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="83fd9-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="83fd9-109">Return value</span></span>

<span data-ttu-id="83fd9-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="83fd9-110">S_OK</span></span> 
  
> <span data-ttu-id="83fd9-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="83fd9-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="83fd9-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="83fd9-112">S_FALSE</span></span> 
  
> <span data-ttu-id="83fd9-113">В настоящее время для вызываемой формы сообщение не существует.</span><span class="sxs-lookup"><span data-stu-id="83fd9-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="83fd9-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="83fd9-114">Remarks</span></span>

<span data-ttu-id="83fd9-115">Формы вызвать **метод IMAPIMessageSite::GetMessage,** чтобы получить интерфейс для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="83fd9-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="83fd9-116">Текущее сообщение это то же сообщение, что и ранее переданное в методе [IPersistMessage::InitNew,](ipersistmessage-initnew.md) [IPersistMessage::Load](ipersistmessage-load.md)или [IPersistMessage::SaveCompleted.](ipersistmessage-savecompleted.md)</span><span class="sxs-lookup"><span data-stu-id="83fd9-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="83fd9-117">**GetMessage** возвращает S_FALSE, если сообщение в настоящее время не существует.</span><span class="sxs-lookup"><span data-stu-id="83fd9-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="83fd9-118">Это состояние может возникать после вызова метода [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) или до следующего вызова **IPersistMessage::Load** или **IPersistMessage::SaveCompleted.**</span><span class="sxs-lookup"><span data-stu-id="83fd9-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="83fd9-119">Список интерфейсов, связанных с серверами форм, см. в списке [интерфейсов форм MAPI.](mapi-form-interfaces.md)</span><span class="sxs-lookup"><span data-stu-id="83fd9-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="83fd9-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="83fd9-120">MFCMAPI reference</span></span>

<span data-ttu-id="83fd9-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="83fd9-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="83fd9-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="83fd9-122">**File**</span></span>|<span data-ttu-id="83fd9-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="83fd9-123">**Function**</span></span>|<span data-ttu-id="83fd9-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="83fd9-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="83fd9-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="83fd9-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="83fd9-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="83fd9-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="83fd9-127">MFCMAPI использует метод **IMAPIMessageSite::GetMessage** для возврата кэшного указателя сообщения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="83fd9-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="83fd9-128">См. также</span><span class="sxs-lookup"><span data-stu-id="83fd9-128">See also</span></span>



[<span data-ttu-id="83fd9-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="83fd9-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="83fd9-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="83fd9-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="83fd9-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83fd9-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="83fd9-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="83fd9-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="83fd9-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="83fd9-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="83fd9-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="83fd9-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="83fd9-135">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="83fd9-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="83fd9-136">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="83fd9-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

