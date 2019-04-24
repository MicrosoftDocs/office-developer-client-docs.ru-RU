---
title: Имапимессажеситежетмессаже
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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32321282"
---
# <a name="imapimessagesitegetmessage"></a><span data-ttu-id="84fd4-103">IMAPIMessageSite::GetMessage</span><span class="sxs-lookup"><span data-stu-id="84fd4-103">IMAPIMessageSite::GetMessage</span></span>

  
  
<span data-ttu-id="84fd4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="84fd4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="84fd4-105">Возвращает текущее сообщение.</span><span class="sxs-lookup"><span data-stu-id="84fd4-105">Returns the current message.</span></span>
  
```cpp
HRESULT GetMessage(
  LPMESSAGE FAR * ppmsg
);
```

## <a name="parameters"></a><span data-ttu-id="84fd4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="84fd4-106">Parameters</span></span>

 <span data-ttu-id="84fd4-107">_ппмсг_</span><span class="sxs-lookup"><span data-stu-id="84fd4-107">_ppmsg_</span></span>
  
> <span data-ttu-id="84fd4-108">вышли Указатель на указатель на возвращенный интерфейс для сообщения.</span><span class="sxs-lookup"><span data-stu-id="84fd4-108">[out] A pointer to a pointer to the returned interface for the message.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="84fd4-109">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="84fd4-109">Return value</span></span>

<span data-ttu-id="84fd4-110">S_OK</span><span class="sxs-lookup"><span data-stu-id="84fd4-110">S_OK</span></span> 
  
> <span data-ttu-id="84fd4-111">����� ������� � ������ ��������� ��������� ��� ��������.</span><span class="sxs-lookup"><span data-stu-id="84fd4-111">The call succeeded and has returned the expected value or values.</span></span>
    
<span data-ttu-id="84fd4-112">S_FALSE</span><span class="sxs-lookup"><span data-stu-id="84fd4-112">S_FALSE</span></span> 
  
> <span data-ttu-id="84fd4-113">Для вызывающей формы не существует сообщения.</span><span class="sxs-lookup"><span data-stu-id="84fd4-113">No message currently exists for the calling form.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="84fd4-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="84fd4-114">Remarks</span></span>

<span data-ttu-id="84fd4-115">Формы вызывают метод **имапимессажесите::** , чтобы получить интерфейс сообщения для текущего сообщения.</span><span class="sxs-lookup"><span data-stu-id="84fd4-115">Forms call the **IMAPIMessageSite::GetMessage** method to obtain a message interface for the current message.</span></span> <span data-ttu-id="84fd4-116">Текущее сообщение это то же сообщение, которое ранее было передано в методе [иперсистмессаже:: инитнев](ipersistmessage-initnew.md), [Иперсистмессаже:: Load](ipersistmessage-load.md)или [иперсистмессаже:: савекомплетед](ipersistmessage-savecompleted.md) .</span><span class="sxs-lookup"><span data-stu-id="84fd4-116">The current message is the same message as was previously passed in the [IPersistMessage::InitNew](ipersistmessage-initnew.md), [IPersistMessage::Load](ipersistmessage-load.md), or [IPersistMessage::SaveCompleted](ipersistmessage-savecompleted.md) method.</span></span> 
  
 <span data-ttu-id="84fd4-117">\*\*\*\* ВОЗВРАЩАЕТ значение S_FALSE, если сообщение в настоящее время не существует.</span><span class="sxs-lookup"><span data-stu-id="84fd4-117">**GetMessage** returns S_FALSE if no message currently exists.</span></span> <span data-ttu-id="84fd4-118">Это состояние может происходить после вызовов метода [иперсистмессаже:: хандсоффмессаже](ipersistmessage-handsoffmessage.md) или перед следующим вызовом **Иперсистмессаже:: Load** или **иперсистмессаже:: савекомплетед** .</span><span class="sxs-lookup"><span data-stu-id="84fd4-118">This state can occur after calls to the [IPersistMessage::HandsOffMessage](ipersistmessage-handsoffmessage.md) method or before the next call to **IPersistMessage::Load** or **IPersistMessage::SaveCompleted** is made.</span></span> 
  
<span data-ttu-id="84fd4-119">Список интерфейсов, связанных с серверами форм, представлен в статье [интерфейсы форм MAPI](mapi-form-interfaces.md).</span><span class="sxs-lookup"><span data-stu-id="84fd4-119">For a list of interfaces related to form servers, see [MAPI Form Interfaces](mapi-form-interfaces.md).</span></span>
  
## <a name="mfcmapi-reference"></a><span data-ttu-id="84fd4-120">Справочные материалы по MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="84fd4-120">MFCMAPI reference</span></span>

<span data-ttu-id="84fd4-121">Пример кода MFCMAPI указан в приведенной ниже таблице.</span><span class="sxs-lookup"><span data-stu-id="84fd4-121">For MFCMAPI sample code, see the following table.</span></span>
  
|<span data-ttu-id="84fd4-122">**Файл**</span><span class="sxs-lookup"><span data-stu-id="84fd4-122">**File**</span></span>|<span data-ttu-id="84fd4-123">**Функция**</span><span class="sxs-lookup"><span data-stu-id="84fd4-123">**Function**</span></span>|<span data-ttu-id="84fd4-124">**Примечание**</span><span class="sxs-lookup"><span data-stu-id="84fd4-124">**Comment**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="84fd4-125">Мимапиформвиевер. cpp</span><span class="sxs-lookup"><span data-stu-id="84fd4-125">MyMAPIFormViewer.cpp</span></span>  <br/> |<span data-ttu-id="84fd4-126">Кмимапиформвиевер:: @ Session</span><span class="sxs-lookup"><span data-stu-id="84fd4-126">CMyMAPIFormViewer::GetSession</span></span>  <br/> |<span data-ttu-id="84fd4-127">MFCMAPI использует метод **имапимессажесите::-Message** , чтобы возвратить текущий указатель сообщения, если он доступен.</span><span class="sxs-lookup"><span data-stu-id="84fd4-127">MFCMAPI uses the **IMAPIMessageSite::GetMessage** method to return the currently cached message pointer, if it is available.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="84fd4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="84fd4-128">See also</span></span>



[<span data-ttu-id="84fd4-129">IPersistMessage::HandsOffMessage</span><span class="sxs-lookup"><span data-stu-id="84fd4-129">IPersistMessage::HandsOffMessage</span></span>](ipersistmessage-handsoffmessage.md)
  
[<span data-ttu-id="84fd4-130">IPersistMessage::InitNew</span><span class="sxs-lookup"><span data-stu-id="84fd4-130">IPersistMessage::InitNew</span></span>](ipersistmessage-initnew.md)
  
[<span data-ttu-id="84fd4-131">IPersistMessage : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84fd4-131">IPersistMessage : IUnknown</span></span>](ipersistmessageiunknown.md)
  
[<span data-ttu-id="84fd4-132">IPersistMessage::Load</span><span class="sxs-lookup"><span data-stu-id="84fd4-132">IPersistMessage::Load</span></span>](ipersistmessage-load.md)
  
[<span data-ttu-id="84fd4-133">IPersistMessage::SaveCompleted</span><span class="sxs-lookup"><span data-stu-id="84fd4-133">IPersistMessage::SaveCompleted</span></span>](ipersistmessage-savecompleted.md)
  
[<span data-ttu-id="84fd4-134">IMAPIMessageSite : IUnknown</span><span class="sxs-lookup"><span data-stu-id="84fd4-134">IMAPIMessageSite : IUnknown</span></span>](imapimessagesiteiunknown.md)


[<span data-ttu-id="84fd4-135">MFCMAPI как пример кода</span><span class="sxs-lookup"><span data-stu-id="84fd4-135">MFCMAPI as a Code Sample</span></span>](mfcmapi-as-a-code-sample.md)
  
[<span data-ttu-id="84fd4-136">Интерфейсы форм MAPI</span><span class="sxs-lookup"><span data-stu-id="84fd4-136">MAPI Form Interfaces</span></span>](mapi-form-interfaces.md)

