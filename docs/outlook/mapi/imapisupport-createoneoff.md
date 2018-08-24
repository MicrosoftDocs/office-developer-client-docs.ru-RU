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
ms.openlocfilehash: 1526ed54fd3773856b009c7c3570064f5a66df28
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22594945"
---
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="b8864-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="b8864-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="b8864-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b8864-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b8864-105">Создает запись идентификатор указывает адрес.</span><span class="sxs-lookup"><span data-stu-id="b8864-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="b8864-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="b8864-106">Parameters</span></span>

 <span data-ttu-id="b8864-107">_lpszName_</span><span class="sxs-lookup"><span data-stu-id="b8864-107">_lpszName_</span></span>
  
> <span data-ttu-id="b8864-108">[in] Указатель на отображаемое имя получателя, свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b8864-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="b8864-109">Параметр _lpszName_ может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b8864-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="b8864-110">_lpszAdrType_</span><span class="sxs-lookup"><span data-stu-id="b8864-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="b8864-111">[in] Указатель на тип адреса (например, ФАКС, SMTP или X500) получателя.</span><span class="sxs-lookup"><span data-stu-id="b8864-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="b8864-112">Параметр _lpszAdrType_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b8864-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b8864-113">_lpszAddress_</span><span class="sxs-lookup"><span data-stu-id="b8864-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="b8864-114">[in] Указатель на обмена сообщениями адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="b8864-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="b8864-115">Параметр _lpszAddress_ не может быть NULL.</span><span class="sxs-lookup"><span data-stu-id="b8864-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="b8864-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="b8864-116">_ulFlags_</span></span>
  
> <span data-ttu-id="b8864-117">[in] Битовая маска флаги, влияющей на одноразовых получателя.</span><span class="sxs-lookup"><span data-stu-id="b8864-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="b8864-118">Можно задать следующие флажки:</span><span class="sxs-lookup"><span data-stu-id="b8864-118">The following flags can be set:</span></span>
    
<span data-ttu-id="b8864-119">MAPI_SEND_NO_RICH_INFO</span><span class="sxs-lookup"><span data-stu-id="b8864-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="b8864-120">Получатель не может обрабатывать сообщения Форматированный контент.</span><span class="sxs-lookup"><span data-stu-id="b8864-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="b8864-121">Если значение MAPI_SEND_NO_RICH_INFO, MAPI свойству получателя **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) присваивается значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b8864-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="b8864-122">Если MAPI_SEND_NO_RICH_INFO не задано, MAPI этому свойству значение TRUE, если адрес получателя обмена мгновенными сообщениями, на который указывает _lpszAddress_ интерпретируется быть адрес в Интернете.</span><span class="sxs-lookup"><span data-stu-id="b8864-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="b8864-123">В этом случае MAPI задает **PR_SEND_RICH_INFO** значение FALSE.</span><span class="sxs-lookup"><span data-stu-id="b8864-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="b8864-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="b8864-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="b8864-125">Отображаемое имя, тип адреса и адрес находятся в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="b8864-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="b8864-126">Если флаг MAPI_UNICODE не установлен, эти строки находятся в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="b8864-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="b8864-127">_lpcbEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8864-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="b8864-128">[out] Указатель на число байт в идентификаторе запись указывает параметр _lppEntryID_ .</span><span class="sxs-lookup"><span data-stu-id="b8864-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="b8864-129">_lppEntryID_</span><span class="sxs-lookup"><span data-stu-id="b8864-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="b8864-130">[out] Указатель на указатель на идентификатор записи для одноразовых получателя.</span><span class="sxs-lookup"><span data-stu-id="b8864-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="b8864-131">������������ ��������</span><span class="sxs-lookup"><span data-stu-id="b8864-131">Return value</span></span>

<span data-ttu-id="b8864-132">ЗНАЧЕНИЕ S_OK</span><span class="sxs-lookup"><span data-stu-id="b8864-132">S_OK</span></span> 
  
> <span data-ttu-id="b8864-133">Идентификатор единичных записей успешно создан.</span><span class="sxs-lookup"><span data-stu-id="b8864-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="b8864-134">Замечания</span><span class="sxs-lookup"><span data-stu-id="b8864-134">Remarks</span></span>

<span data-ttu-id="b8864-135">Метод **IMAPISupport::CreateOneOff** применяется для всех объектов поддержки поставщика службы.</span><span class="sxs-lookup"><span data-stu-id="b8864-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="b8864-136">Поставщики услуг вызова **CreateOneOff** для создания записи идентификатора для одноразовых получателя (получателя, не принадлежащие ни контейнеры из любого из поставщиками в настоящее время загрузки адресной книги).</span><span class="sxs-lookup"><span data-stu-id="b8864-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="b8864-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="b8864-137">Notes to callers</span></span>

<span data-ttu-id="b8864-138">При завершении с помощью идентификатора записи, возвращаемых **CreateOneOff**освободите память, выделенная для идентификатор записи с помощью функции [MAPIFreeBuffer](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="b8864-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="b8864-139">Примечания для поставщиками транспорта</span><span class="sxs-lookup"><span data-stu-id="b8864-139">Notes to Transport Providers</span></span>

<span data-ttu-id="b8864-140">Поддержку транспорта Neutral Encapsulation формата TNEF и использовать значение свойства **PR_SEND_RICH_INFO** для определения необходимости использовать TNEF при передачи сообщения.</span><span class="sxs-lookup"><span data-stu-id="b8864-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="b8864-141">Не поддерживает формат TNEF или не отправлять сообщения в формате запросу может вызвать проблемы для клиентов на основе форм или клиентов, которым требуется настраиваемых свойств MAPI.</span><span class="sxs-lookup"><span data-stu-id="b8864-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="b8864-142">Это, так как TNEF обычно используется для отправки настраиваемых свойств для пользовательских классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="b8864-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="b8864-143">См. также</span><span class="sxs-lookup"><span data-stu-id="b8864-143">See also</span></span>



[<span data-ttu-id="b8864-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="b8864-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="b8864-145">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="b8864-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="b8864-146">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="b8864-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="b8864-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="b8864-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

