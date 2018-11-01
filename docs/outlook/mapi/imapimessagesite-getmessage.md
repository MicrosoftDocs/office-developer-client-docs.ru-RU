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
ms.openlocfilehash: 3612c12a503174484d4a469ffa167922a015ed5b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576612"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="6bdf2-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="6bdf2-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="6bdf2-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6bdf2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6bdf2-105">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="6bdf2-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="6bdf2-106">Parameters</span></span>

 <span data-ttu-id="6bdf2-107">_ppmsg_</span><span class="sxs-lookup"><span data-stu-id="6bdf2-107">_ppmsg_</span></span>
  
> <span data-ttu-id="6bdf2-108">[out] Указатель на указатель на возвращенный интерфейс для сообщения.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="6bdf2-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="6bdf2-109">Return value</span></span>

<span data-ttu-id="6bdf2-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="6bdf2-110">S_OK</span></span> 
  
> <span data-ttu-id="6bdf2-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="6bdf2-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="6bdf2-112">S_FALSE</span></span> 
  
> <span data-ttu-id="6bdf2-113">Для вызова формы в настоящий момент не сообщения.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="6bdf2-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="6bdf2-114">Remarks</span></span>

<span data-ttu-id="6bdf2-115">Форм вызовите метод **IMAPIMessageSite::GetMessage** для получения интерфейса сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="6bdf2-116">Текущее сообщение имеет то же сообщение как ранее был передан в метод [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md)или [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="6bdf2-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="6bdf2-117">**GetMessage** возвращает S_FALSE, если сообщение не в настоящий момент.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="6bdf2-118">Это состояние может произойти после вызовов в метод [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) или до следующего вызова **IPersistMessage::Load** или **IPersistMessage::SaveCompleted** будет создано.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="6bdf2-119">Список интерфейсы, связанные с серверами формы в разделе [Интерфейсов формы MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="6bdf2-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="6bdf2-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="6bdf2-120">MFCMAPI reference</span></span>

<span data-ttu-id="6bdf2-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="6bdf2-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="6bdf2-122">**File**</span></span>|<span data-ttu-id="6bdf2-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="6bdf2-123">**Function**</span></span>|<span data-ttu-id="6bdf2-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="6bdf2-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6bdf2-125">MyMAPIFormViewer.cpp</span><span class="sxs-lookup"><span data-stu-id="6bdf2-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="6bdf2-126">CMyMAPIFormViewer::GetSession</span><span class="sxs-lookup"><span data-stu-id="6bdf2-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="6bdf2-127">Mfcmapi (en) использует метод **IMAPIMessageSite::GetMessage** возвращает указатель в настоящее время кэширования сообщение, если она доступна.</span><span class="sxs-lookup"><span data-stu-id="6bdf2-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="6bdf2-128">См. также</span><span class="sxs-lookup"><span data-stu-id="6bdf2-128">See also</span></span>



[<span data-ttu-id="6bdf2-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="6bdf2-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="6bdf2-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="6bdf2-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="6bdf2-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bdf2-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="6bdf2-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="6bdf2-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="6bdf2-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="6bdf2-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="6bdf2-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="6bdf2-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="6bdf2-135">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="6bdf2-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="6bdf2-136">Интерфейсы формы MAPI</span><span class="sxs-lookup"><span data-stu-id="6bdf2-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

