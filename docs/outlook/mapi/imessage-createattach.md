---
title: IMessageCreateAttach
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.IMessage::CreateAttach
api_type:
- COM
ms.assetid: 01711aca-c598-438c-88d7-0719b6691e34
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f534912377aadb3c342030fc02fce26693857476
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417674"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="e3ec7-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="e3ec7-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="e3ec7-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ec7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ec7-105">Создает новое вложение.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="e3ec7-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="e3ec7-106">Parameters</span></span>

 <span data-ttu-id="e3ec7-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-107">_lpInterface_</span></span>
  
> <span data-ttu-id="e3ec7-108">[in] Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="e3ec7-109">Передача NULL приводит к возвращению стандартного интерфейса сообщения или **IMessage.**</span><span class="sxs-lookup"><span data-stu-id="e3ec7-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="e3ec7-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-110">_ulFlags_</span></span>
  
> <span data-ttu-id="e3ec7-111">[in] Bitmask флагов, которые контролируют, как создается вложение.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="e3ec7-112">Можно установить следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="e3ec7-112">The following flag can be set:</span></span>
    
<span data-ttu-id="e3ec7-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="e3ec7-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="e3ec7-114">Позволяет **CreateAttach** успешно возвращаться, возможно, до полного доступности вложения для вызываемого клиента.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="e3ec7-115">Если вложение не доступно, последующий вызов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="e3ec7-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="e3ec7-117">[вышел] Указатель на номер индекса, определяющий недавно созданное вложение.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="e3ec7-118">Этот номер действителен только в том случае, если сообщение  открыто и является основой для свойства[PR_ATTACH_NUM (PidTagAttachNumber).](pidtagattachnumber-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="e3ec7-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="e3ec7-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="e3ec7-119">_lppAttach_</span></span>
  
> <span data-ttu-id="e3ec7-120">[вышел] Указатель на указатель на открытый объект вложения.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="e3ec7-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="e3ec7-121">Return value</span></span>

<span data-ttu-id="e3ec7-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="e3ec7-122">S_OK</span></span> 
  
> <span data-ttu-id="e3ec7-123">Вложение было успешно создано.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="e3ec7-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="e3ec7-124">Remarks</span></span>

<span data-ttu-id="e3ec7-125">Метод **IMessage::CreateAttach** создает новое вложение в сообщение.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="e3ec7-126">Новое вложение и все свойства, которые для него установлены, недоступны до тех пор, пока клиент не вызвал метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) и метод **IMAPIProp::SaveChanges.**</span><span class="sxs-lookup"><span data-stu-id="e3ec7-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="e3ec7-127">Номер вложения, на который указывает  _lpulAttachmentNum,_ уникален и действителен только в контексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="e3ec7-128">То есть два вложения в двух разных сообщениях могут иметь одинаковое число, а два вложения в одном сообщении не могут.</span><span class="sxs-lookup"><span data-stu-id="e3ec7-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3ec7-129">См. также</span><span class="sxs-lookup"><span data-stu-id="e3ec7-129">See also</span></span>



[<span data-ttu-id="e3ec7-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="e3ec7-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

