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
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="de467-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="de467-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="de467-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de467-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de467-105">Создает идентификатор записи для разового адреса.</span><span class="sxs-lookup"><span data-stu-id="de467-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="de467-106">Parameters</span><span class="sxs-lookup"><span data-stu-id="de467-106">Parameters</span></span>

 <span data-ttu-id="de467-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="de467-107">_lpszName_</span></span>
  
> <span data-ttu-id="de467-108">[in] Указатель на имя отображения получателя **свойства PR_DISPLAY_NAME** [(PidTagDisplayName).](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="de467-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="de467-109">Параметр  _lpszName может_ быть NULL.</span><span class="sxs-lookup"><span data-stu-id="de467-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="de467-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="de467-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="de467-111">[in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя.</span><span class="sxs-lookup"><span data-stu-id="de467-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="de467-112">Параметр  _lpszAdrType_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="de467-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="de467-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="de467-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="de467-114">[in] Указатель на адрес сообщения получателя.</span><span class="sxs-lookup"><span data-stu-id="de467-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="de467-115">Параметр  _lpszAddress не_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="de467-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="de467-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="de467-116">_ulFlags_</span></span>
  
> <span data-ttu-id="de467-117">[in] Битмашка флагов, которая влияет на разовую получатель.</span><span class="sxs-lookup"><span data-stu-id="de467-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="de467-118">Можно установить следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="de467-118">The following flags can be set:</span></span>
    
<span data-ttu-id="de467-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="de467-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="de467-120">Получатель не может обрабатывать отформатированный контент сообщения.</span><span class="sxs-lookup"><span data-stu-id="de467-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="de467-121">Если MAPI_SEND_NO_RICH_INFO установлено, MAPI задает свойство  [PR_SEND_RICH_INFO (PidTagSendRichInfo)](pidtagsendrichinfo-canonical-property.md)false.</span><span class="sxs-lookup"><span data-stu-id="de467-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="de467-122">Если MAPI_SEND_NO_RICH_INFO не установлено, MAPI задает это свойство true, если адрес обмена сообщениями получателя, на который указывает  _lpszAddress,_ не интерпретируется как интернет-адрес.</span><span class="sxs-lookup"><span data-stu-id="de467-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="de467-123">В этом случае MAPI задает **PR_SEND_RICH_INFO** false.</span><span class="sxs-lookup"><span data-stu-id="de467-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="de467-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="de467-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="de467-125">Имя отображения, тип адреса и адрес находятся в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="de467-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="de467-126">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="de467-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="de467-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="de467-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="de467-128">[вышел] Указатель на количество bytes в идентификаторе записи, указываемом _параметром lppEntryID._</span><span class="sxs-lookup"><span data-stu-id="de467-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="de467-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="de467-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="de467-130">[вышел] Указатель на указатель на идентификатор записи для разового получателя.</span><span class="sxs-lookup"><span data-stu-id="de467-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="de467-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="de467-131">Return value</span></span>

<span data-ttu-id="de467-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="de467-132">S_OK</span></span> 
  
> <span data-ttu-id="de467-133">Идентификатор одноавтной записи был успешно создан.</span><span class="sxs-lookup"><span data-stu-id="de467-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="de467-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="de467-134">Remarks</span></span>

<span data-ttu-id="de467-135">Метод **IMAPISupport::CreateOneOff** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="de467-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="de467-136">Поставщики услуг звонят **в CreateOneOff** для создания идентификатора входа для разового получателя (получателя, который не принадлежит ни одному из контейнеров от любого из загруженных поставщиков адресных книг).</span><span class="sxs-lookup"><span data-stu-id="de467-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="de467-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="de467-137">Notes to callers</span></span>

<span data-ttu-id="de467-138">После завершения использования идентификатора записи, возвращенного **CreateOneOff,** освободите память, выделенную для идентификатора записи, с помощью функции [MAPIFreeBuffer.](mapifreebuffer.md)</span><span class="sxs-lookup"><span data-stu-id="de467-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="de467-139">Заметки поставщикам транспорта</span><span class="sxs-lookup"><span data-stu-id="de467-139">Notes to Transport Providers</span></span>

<span data-ttu-id="de467-140">Поддержка формата транспортной нейтральной инкапсуляции (TNEF) и использование значения свойства PR_SEND_RICH_INFO, чтобы определить, следует ли использовать TNEF при транспортировке сообщения. </span><span class="sxs-lookup"><span data-stu-id="de467-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="de467-141">Не поддержка TNEF или не отправка сообщения в этом формате при запросе может быть проблемой для клиентов или клиентов на основе форм, которые требуют настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="de467-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="de467-142">Это потому, что TNEF обычно используется для отправки пользовательских свойств для настраиваемых классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="de467-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="de467-143">См. также</span><span class="sxs-lookup"><span data-stu-id="de467-143">See also</span></span>



[<span data-ttu-id="de467-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="de467-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="de467-145">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="de467-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="de467-146">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="de467-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="de467-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="de467-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

