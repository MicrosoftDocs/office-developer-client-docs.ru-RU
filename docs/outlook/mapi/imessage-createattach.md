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
ms.openlocfilehash: 9cc2f5f3880466c0a70febedbc7aaec987b62bb3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22572095"
---
# <a name="imessagecreateattach"></a><span data-ttu-id="fae26-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="fae26-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="fae26-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="fae26-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="fae26-105">Создает новое вложение.</span><span class="sxs-lookup"><span data-stu-id="fae26-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="fae26-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="fae26-106">Parameters</span></span>

 <span data-ttu-id="fae26-107">_lpInterface_</span><span class="sxs-lookup"><span data-stu-id="fae26-107">_lpInterface_</span></span>
  
> <span data-ttu-id="fae26-108">[in] Указатель на интерфейс идентификатор, представляющий интерфейса, которые будут использоваться для доступа к сообщение (ИД интерфейса).</span><span class="sxs-lookup"><span data-stu-id="fae26-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="fae26-109">Передача значение NULL, результаты в стандартный интерфейс сообщения или **IMessage**, возвращаемых.</span><span class="sxs-lookup"><span data-stu-id="fae26-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="fae26-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="fae26-110">_ulFlags_</span></span>
  
> <span data-ttu-id="fae26-111">[in] Битовая маска флаги, который определяет способ создания вложение.</span><span class="sxs-lookup"><span data-stu-id="fae26-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="fae26-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="fae26-112">The following flag can be set:</span></span>
    
<span data-ttu-id="fae26-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="fae26-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="fae26-114">Позволяет **CreateAttach** для возврата успешно, возможно перед вложением является полностью доступны для клиента.</span><span class="sxs-lookup"><span data-stu-id="fae26-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="fae26-115">Если вложение не доступно, последующие подключения к нему может вызвать ошибку.</span><span class="sxs-lookup"><span data-stu-id="fae26-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="fae26-116">_lpulAttachmentNum_</span><span class="sxs-lookup"><span data-stu-id="fae26-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="fae26-117">[out] Указатель на индекса номер, идентифицирующий только что созданный вложения.</span><span class="sxs-lookup"><span data-stu-id="fae26-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="fae26-118">Этот номер является допустимым только в том случае, если сообщение открыто и является основой для свойства **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) вложения.</span><span class="sxs-lookup"><span data-stu-id="fae26-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="fae26-119">_lppAttach_</span><span class="sxs-lookup"><span data-stu-id="fae26-119">_lppAttach_</span></span>
  
> <span data-ttu-id="fae26-120">[out] Указатель на указатель на объект открыть вложение.</span><span class="sxs-lookup"><span data-stu-id="fae26-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="fae26-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="fae26-121">Return value</span></span>

<span data-ttu-id="fae26-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="fae26-122">S_OK</span></span> 
  
> <span data-ttu-id="fae26-123">Вложение успешно создан.</span><span class="sxs-lookup"><span data-stu-id="fae26-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="fae26-124">Замечания</span><span class="sxs-lookup"><span data-stu-id="fae26-124">Remarks</span></span>

<span data-ttu-id="fae26-125">Метод **IMessage::CreateAttach** создает новый вложения сообщения.</span><span class="sxs-lookup"><span data-stu-id="fae26-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="fae26-126">Новое вложение и свойств, заданные для него, недоступны, пока называется клиента метод [IMAPIProp::SaveChanges](imapiprop-savechanges.md) вложения и метод **IMAPIProp::SaveChanges** сообщений.</span><span class="sxs-lookup"><span data-stu-id="fae26-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="fae26-127">Номер вложения, на который указывает _lpulAttachmentNum_ — это уникальное и допускается только в контексте сообщения.</span><span class="sxs-lookup"><span data-stu-id="fae26-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="fae26-128">То есть два вложений в двух разных сообщений может быть тот же номер, а два вложений в то же сообщение нельзя.</span><span class="sxs-lookup"><span data-stu-id="fae26-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="fae26-129">См. также</span><span class="sxs-lookup"><span data-stu-id="fae26-129">See also</span></span>



[<span data-ttu-id="fae26-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="fae26-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

