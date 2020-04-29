---
title: имессажекреатеаттач
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
# <a name="imessagecreateattach"></a><span data-ttu-id="891c4-103">IMessage::CreateAttach</span><span class="sxs-lookup"><span data-stu-id="891c4-103">IMessage::CreateAttach</span></span>

  
  
<span data-ttu-id="891c4-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="891c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="891c4-105">Создает новое вложение.</span><span class="sxs-lookup"><span data-stu-id="891c4-105">Creates a new attachment.</span></span>
  
```cpp
HRESULT CreateAttach(
LPCIID lpInterface,
ULONG ulFlags,
ULONG FAR * lpulAttachmentNum,
LPATTACH FAR * lppAttach
);
```

## <a name="parameters"></a><span data-ttu-id="891c4-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="891c4-106">Parameters</span></span>

 <span data-ttu-id="891c4-107">_лпинтерфаце_</span><span class="sxs-lookup"><span data-stu-id="891c4-107">_lpInterface_</span></span>
  
> <span data-ttu-id="891c4-108">возврата Указатель на идентификатор интерфейса (IID), представляющий интерфейс, который будет использоваться для доступа к сообщению.</span><span class="sxs-lookup"><span data-stu-id="891c4-108">[in] Pointer to the interface identifier (IID) representing the interface to be used to access the message.</span></span> <span data-ttu-id="891c4-109">Передача результатов NULL в стандартный интерфейс сообщения (или **iMessage**) возвращается.</span><span class="sxs-lookup"><span data-stu-id="891c4-109">Passing NULL results in the message's standard interface, or **IMessage**, being returned.</span></span> 
    
 <span data-ttu-id="891c4-110">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="891c4-110">_ulFlags_</span></span>
  
> <span data-ttu-id="891c4-111">возврата Битовая маска флагов, определяющих способ создания вложения.</span><span class="sxs-lookup"><span data-stu-id="891c4-111">[in] Bitmask of flags that controls how the attachment is created.</span></span> <span data-ttu-id="891c4-112">Можно задать следующий флаг:</span><span class="sxs-lookup"><span data-stu-id="891c4-112">The following flag can be set:</span></span>
    
<span data-ttu-id="891c4-113">MAPI_DEFERRED_ERRORS</span><span class="sxs-lookup"><span data-stu-id="891c4-113">MAPI_DEFERRED_ERRORS</span></span> 
  
> <span data-ttu-id="891c4-114">Разрешает успешное возвращение **креатеаттач** , возможно, перед тем, как вложение будет полностью доступно для вызывающего клиента.</span><span class="sxs-lookup"><span data-stu-id="891c4-114">Allows **CreateAttach** to return successfully, possibly before the attachment is fully accessible to the calling client.</span></span> <span data-ttu-id="891c4-115">Если вложение недоступно, то выполнение последующих вызовов может привести к ошибке.</span><span class="sxs-lookup"><span data-stu-id="891c4-115">If the attachment is not accessible, making a subsequent call to it can result in an error.</span></span> 
    
 <span data-ttu-id="891c4-116">_лпулаттачментнум_</span><span class="sxs-lookup"><span data-stu-id="891c4-116">_lpulAttachmentNum_</span></span>
  
> <span data-ttu-id="891c4-117">вышли Указатель на номер индекса, идентифицирующий вновь созданное вложение.</span><span class="sxs-lookup"><span data-stu-id="891c4-117">[out] Pointer to an index number identifying the newly created attachment.</span></span> <span data-ttu-id="891c4-118">Это значение действительно только в том случае, если сообщение открыто и является основой для свойства **PR_ATTACH_NUM** вложения ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="891c4-118">This number is valid only when the message is open and is the basis for the attachment's **PR_ATTACH_NUM** ([PidTagAttachNumber](pidtagattachnumber-canonical-property.md)) property.</span></span>
    
 <span data-ttu-id="891c4-119">_лппаттач_</span><span class="sxs-lookup"><span data-stu-id="891c4-119">_lppAttach_</span></span>
  
> <span data-ttu-id="891c4-120">вышли Указатель на указатель на открытый объект вложения.</span><span class="sxs-lookup"><span data-stu-id="891c4-120">[out] Pointer to a pointer to the open attachment object.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="891c4-121">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="891c4-121">Return value</span></span>

<span data-ttu-id="891c4-122">S_OK</span><span class="sxs-lookup"><span data-stu-id="891c4-122">S_OK</span></span> 
  
> <span data-ttu-id="891c4-123">Вложение успешно создано.</span><span class="sxs-lookup"><span data-stu-id="891c4-123">The attachment was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="891c4-124">Примечания</span><span class="sxs-lookup"><span data-stu-id="891c4-124">Remarks</span></span>

<span data-ttu-id="891c4-125">Метод **iMessage:: креатеаттач** создает новое вложение для сообщения.</span><span class="sxs-lookup"><span data-stu-id="891c4-125">The **IMessage::CreateAttach** method creates a new attachment on a message.</span></span> <span data-ttu-id="891c4-126">Новое вложение и все свойства, заданные для него, недоступны до тех пор, пока клиент не вызовет метод [IMAPIProp:: SaveChanges](imapiprop-savechanges.md) для вложения и сообщение **IMAPIProp:: SaveChanges** .</span><span class="sxs-lookup"><span data-stu-id="891c4-126">The new attachment and any properties that are set for it, are not available until a client has called both the attachment's [IMAPIProp::SaveChanges](imapiprop-savechanges.md) method and the message's **IMAPIProp::SaveChanges** method.</span></span> 
  
<span data-ttu-id="891c4-127">Номер вложения, на который указывает _лпулаттачментнум_ , является уникальным и действительным только в пределах контекста сообщения.</span><span class="sxs-lookup"><span data-stu-id="891c4-127">The attachment number pointed to by  _lpulAttachmentNum_ is unique and valid only within the context of the message.</span></span> <span data-ttu-id="891c4-128">То есть два вложения в двух разных сообщениях могут иметь одинаковый номер, в то время как два вложения в одном сообщении не могут.</span><span class="sxs-lookup"><span data-stu-id="891c4-128">That is, two attachments in two different messages can have the same number while two attachments in the same message cannot.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="891c4-129">См. также</span><span class="sxs-lookup"><span data-stu-id="891c4-129">See also</span></span>



[<span data-ttu-id="891c4-130">IMessage: IMAPIProp</span><span class="sxs-lookup"><span data-stu-id="891c4-130">IMessage : IMAPIProp</span></span>](imessageimapiprop.md)

