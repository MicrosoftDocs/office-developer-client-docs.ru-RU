---
title: IMAPISupportCreateOneOff
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- IMAPISupport.CreateOneOff
api_type:
- COM
ms.assetid: ee57d6e0-9de0-4427-97ce-371c1c01f3de
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9571d51e01c2d58d9b8a9a913ba2c210ae0bd44d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411997"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="04cff-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="04cff-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="04cff-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="04cff-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="04cff-105">Создает идентификатор записи для разовый адрес.</span><span class="sxs-lookup"><span data-stu-id="04cff-105">Creates an entry identifier for a one-off address.</span></span>
  
```cpp
HRESULT CreateOneOff(
  LPSTR lpszName,
  LPSTR lpszAdrType,
  LPSTR lpszAddress,
  ULONG ulFlags,
  ULONG FAR * lpcbEntryID,
  LPENTRYID FAR * lppEntryID
);
```

## <a name="parameters"></a><span data-ttu-id="04cff-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="04cff-106">Parameters</span></span>

 <span data-ttu-id="04cff-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="04cff-107">_lpszName_</span></span>
  
> <span data-ttu-id="04cff-108">[in] Указатель на отображаемого имени получателя, **PR_DISPLAY_NAME** ([PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="04cff-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="04cff-109">Параметр  _lpszName может_ иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="04cff-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="04cff-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="04cff-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="04cff-111">[in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя.</span><span class="sxs-lookup"><span data-stu-id="04cff-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="04cff-112">Параметр  _lpszAdrType не_ может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="04cff-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="04cff-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="04cff-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="04cff-114">[in] Указатель на адрес сообщения получателя.</span><span class="sxs-lookup"><span data-stu-id="04cff-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="04cff-115">Параметр  _lpszAddress не_ может иметь NULL.</span><span class="sxs-lookup"><span data-stu-id="04cff-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="04cff-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="04cff-116">_ulFlags_</span></span>
  
> <span data-ttu-id="04cff-117">[in] Битоваяmas флагов, влияемая на одного получателя.</span><span class="sxs-lookup"><span data-stu-id="04cff-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="04cff-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="04cff-118">The following flags can be set:</span></span>
    
<span data-ttu-id="04cff-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="04cff-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="04cff-120">Получатель не может обрабатывать отформатированный контент сообщения.</span><span class="sxs-lookup"><span data-stu-id="04cff-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="04cff-121">Если MAPI_SEND_NO_RICH_INFO задан, MAPI устанавливает для свойства **PR_SEND_RICH_INFO** получателя [(PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false.</span><span class="sxs-lookup"><span data-stu-id="04cff-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="04cff-122">Если MAPI_SEND_NO_RICH_INFO не заданная, MAPI устанавливает для этого свойства true, если адрес получателя сообщений, на который указывает  _lpszAddress,_ не интерпретируется как адрес Интернета.</span><span class="sxs-lookup"><span data-stu-id="04cff-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="04cff-123">В этом случае MAPI **PR_SEND_RICH_INFO** false.</span><span class="sxs-lookup"><span data-stu-id="04cff-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="04cff-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="04cff-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="04cff-125">Отображаемого имени, типа адреса и адреса в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="04cff-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="04cff-126">Если флаг MAPI_UNICODE не установлен, эти строки имеют формат ANSI.</span><span class="sxs-lookup"><span data-stu-id="04cff-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="04cff-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="04cff-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="04cff-128">[out] Указатель на количество в идентификаторе записи, на которые указывает параметр _lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="04cff-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="04cff-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="04cff-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="04cff-130">[out] Указатель на указатель на идентификатор записи для одного получателя.</span><span class="sxs-lookup"><span data-stu-id="04cff-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="04cff-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="04cff-131">Return value</span></span>

<span data-ttu-id="04cff-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="04cff-132">S_OK</span></span> 
  
> <span data-ttu-id="04cff-133">Идентификатор однорахой записи успешно создан.</span><span class="sxs-lookup"><span data-stu-id="04cff-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="04cff-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="04cff-134">Remarks</span></span>

<span data-ttu-id="04cff-135">Метод **IMAPISupport::CreateOneOff** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="04cff-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="04cff-136">Поставщики услуг звонят **в CreateOneOff,** чтобы создать идентификатор записи для одного получателя (получателя, который не принадлежит ни одному из контейнеров ни от одного из текущих загруженных поставщиков адресной книги).</span><span class="sxs-lookup"><span data-stu-id="04cff-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="04cff-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="04cff-137">Notes to callers</span></span>

<span data-ttu-id="04cff-138">После завершения использования идентификатора записи, возвращаемого **CreateOneOff,** освободите память, выделенную для идентификатора записи, с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="04cff-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="04cff-139">Примечания для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="04cff-139">Notes to Transport Providers</span></span>

<span data-ttu-id="04cff-140">Поддержка формата TNEF и использование значения свойства **PR_SEND_RICH_INFO,** чтобы определить, следует ли использовать формат TNEF при транспортировке сообщения.</span><span class="sxs-lookup"><span data-stu-id="04cff-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="04cff-141">Не поддерживает формат TNEF или не отправляет сообщение в этом формате при запросе, может быть проблемой для клиентов на основе форм, которые требуют настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="04cff-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="04cff-142">Это необходимо, поскольку TNEF обычно используется для отправки настраиваемой свойства для настраиваемой классы сообщений.</span><span class="sxs-lookup"><span data-stu-id="04cff-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="04cff-143">См. также</span><span class="sxs-lookup"><span data-stu-id="04cff-143">See also</span></span>



[<span data-ttu-id="04cff-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="04cff-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="04cff-145">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="04cff-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="04cff-146">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="04cff-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="04cff-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="04cff-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

