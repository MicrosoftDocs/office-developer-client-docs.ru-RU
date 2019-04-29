---
title: Имаписуппорткреатеонеофф
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
# <a name="imapisupportcreateoneoff"></a><span data-ttu-id="207d6-103">IMAPISupport::CreateOneOff</span><span class="sxs-lookup"><span data-stu-id="207d6-103">IMAPISupport::CreateOneOff</span></span>

  
  
<span data-ttu-id="207d6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="207d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="207d6-105">Создает идентификатор записи для одного адреса.</span><span class="sxs-lookup"><span data-stu-id="207d6-105">Creates an entry identifier for a one-off address.</span></span>
  
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

## <a name="parameters"></a><span data-ttu-id="207d6-106">Параметры</span><span class="sxs-lookup"><span data-stu-id="207d6-106">Parameters</span></span>

 <span data-ttu-id="207d6-107">_Лпсзнаме_</span><span class="sxs-lookup"><span data-stu-id="207d6-107">_lpszName_</span></span>
  
> <span data-ttu-id="207d6-108">возврата Указатель на отображаемое имя получателя, свойство **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="207d6-108">[in] A pointer to the display name of the recipient the **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property.</span></span> <span data-ttu-id="207d6-109">Параметр _лпсзнаме_ может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="207d6-109">The  _lpszName_ parameter can be NULL.</span></span> 
    
 <span data-ttu-id="207d6-110">_Лпсзадртипе_</span><span class="sxs-lookup"><span data-stu-id="207d6-110">_lpszAdrType_</span></span>
  
> <span data-ttu-id="207d6-111">возврата Указатель на тип адреса (например, FAX, SMTP или X500) получателя.</span><span class="sxs-lookup"><span data-stu-id="207d6-111">[in] A pointer to the address type (such as FAX, SMTP, or X500) of the recipient.</span></span> <span data-ttu-id="207d6-112">Параметр _лпсзадртипе_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="207d6-112">The  _lpszAdrType_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="207d6-113">_Лпсзаддресс_</span><span class="sxs-lookup"><span data-stu-id="207d6-113">_lpszAddress_</span></span>
  
> <span data-ttu-id="207d6-114">возврата Указатель на адрес обмена сообщениями получателя.</span><span class="sxs-lookup"><span data-stu-id="207d6-114">[in] A pointer to the messaging address of the recipient.</span></span> <span data-ttu-id="207d6-115">Параметр _лпсзаддресс_ не может иметь значение null.</span><span class="sxs-lookup"><span data-stu-id="207d6-115">The  _lpszAddress_ parameter cannot be NULL.</span></span> 
    
 <span data-ttu-id="207d6-116">_ulFlags_</span><span class="sxs-lookup"><span data-stu-id="207d6-116">_ulFlags_</span></span>
  
> <span data-ttu-id="207d6-117">возврата Битовая маска флагов, влияющих на одного получателя.</span><span class="sxs-lookup"><span data-stu-id="207d6-117">[in] A bitmask of flags that affects the one-off recipient.</span></span> <span data-ttu-id="207d6-118">Можно задать следующие флаги:</span><span class="sxs-lookup"><span data-stu-id="207d6-118">The following flags can be set:</span></span>
    
<span data-ttu-id="207d6-119">МАПИ_СЕНД_НО_РИЧ_ИНФО</span><span class="sxs-lookup"><span data-stu-id="207d6-119">MAPI_SEND_NO_RICH_INFO</span></span> 
  
> <span data-ttu-id="207d6-120">Получатель не может обрабатывать форматированное содержимое сообщения.</span><span class="sxs-lookup"><span data-stu-id="207d6-120">The recipient cannot handle formatted message content.</span></span> <span data-ttu-id="207d6-121">Если задано значение МАПИ_СЕНД_НО_РИЧ_ИНФО, MAPI задает для свойства **пр_сенд_рич_инфо** ([PIDTAGSENDRICHINFO](pidtagsendrichinfo-canonical-property.md)) получателя значение false.</span><span class="sxs-lookup"><span data-stu-id="207d6-121">If MAPI_SEND_NO_RICH_INFO is set, MAPI sets the recipient's **PR_SEND_RICH_INFO** ([PidTagSendRichInfo](pidtagsendrichinfo-canonical-property.md)) property to FALSE.</span></span> <span data-ttu-id="207d6-122">Если МАПИ_СЕНД_НО_РИЧ_ИНФО не задано, MAPI задает для этого свойства значение TRUE, если адрес обмена сообщениями получателя, на который указывает _лпсзаддресс_ , интерпретируется как адрес в Интернете.</span><span class="sxs-lookup"><span data-stu-id="207d6-122">If MAPI_SEND_NO_RICH_INFO is not set, MAPI sets this property to TRUE unless the recipient's messaging address pointed to by  _lpszAddress_ is interpreted to be an Internet address.</span></span> <span data-ttu-id="207d6-123">В этом случае MAPI устанавливает для **ПР_СЕНД_РИЧ_ИНФО** значение false.</span><span class="sxs-lookup"><span data-stu-id="207d6-123">In this case, MAPI sets **PR_SEND_RICH_INFO** to FALSE.</span></span> 
    
<span data-ttu-id="207d6-124">MAPI_UNICODE</span><span class="sxs-lookup"><span data-stu-id="207d6-124">MAPI_UNICODE</span></span> 
  
> <span data-ttu-id="207d6-125">Отображаемое имя, тип адреса и адрес имеют формат Юникод.</span><span class="sxs-lookup"><span data-stu-id="207d6-125">The display name, address type, and address are in Unicode format.</span></span> <span data-ttu-id="207d6-126">Если флаг МАПИ_УНИКОДЕ не установлен, эти строки представлены в формате ANSI.</span><span class="sxs-lookup"><span data-stu-id="207d6-126">If the MAPI_UNICODE flag is not set, these strings are in ANSI format.</span></span>
    
 <span data-ttu-id="207d6-127">_Лпкбентрид_</span><span class="sxs-lookup"><span data-stu-id="207d6-127">_lpcbEntryID_</span></span>
  
> <span data-ttu-id="207d6-128">вышли Указатель на число байтов в идентификаторе записи, на который указывает параметр _лппентрид_ .</span><span class="sxs-lookup"><span data-stu-id="207d6-128">[out] A pointer to the count of bytes in the entry identifier pointed to by the  _lppEntryID_ parameter.</span></span> 
    
 <span data-ttu-id="207d6-129">_Лппентрид_</span><span class="sxs-lookup"><span data-stu-id="207d6-129">_lppEntryID_</span></span>
  
> <span data-ttu-id="207d6-130">вышли Указатель на указатель на идентификатор записи для одноразового получателя.</span><span class="sxs-lookup"><span data-stu-id="207d6-130">[out] A pointer to a pointer to the entry identifier for the one-off recipient.</span></span>
    
## <a name="return-value"></a><span data-ttu-id="207d6-131">Возвращаемое значение</span><span class="sxs-lookup"><span data-stu-id="207d6-131">Return value</span></span>

<span data-ttu-id="207d6-132">S_OK</span><span class="sxs-lookup"><span data-stu-id="207d6-132">S_OK</span></span> 
  
> <span data-ttu-id="207d6-133">Успешно создан идентификатор одноразовой записи.</span><span class="sxs-lookup"><span data-stu-id="207d6-133">The one-off entry identifier was successfully created.</span></span>
    
## <a name="remarks"></a><span data-ttu-id="207d6-134">Примечания</span><span class="sxs-lookup"><span data-stu-id="207d6-134">Remarks</span></span>

<span data-ttu-id="207d6-135">Метод **имаписуппорт:: креатеонеофф** реализован для всех объектов поддержки поставщика услуг.</span><span class="sxs-lookup"><span data-stu-id="207d6-135">The **IMAPISupport::CreateOneOff** method is implemented for all service provider support objects.</span></span> <span data-ttu-id="207d6-136">Поставщики услуг вызывают **креатеонеофф** для создания идентификатора записи для одноразового получателя (получателя, не относящегося к какому-либо из контейнеров из загруженных в текущий момент поставщиков адресной книги).</span><span class="sxs-lookup"><span data-stu-id="207d6-136">Service providers call **CreateOneOff** to create an entry identifier for a one-off recipient (a recipient that does not belong to any of the containers from any of the currently loaded address book providers).</span></span> 
  
## <a name="notes-to-callers"></a><span data-ttu-id="207d6-137">Примечания для вызывающих методов</span><span class="sxs-lookup"><span data-stu-id="207d6-137">Notes to callers</span></span>

<span data-ttu-id="207d6-138">По завершении использования идентификатора записи, возвращенного функцией **креатеонеофф**, освободите память, выделенную для идентификатора записи, с помощью функции [мапифрибуффер](mapifreebuffer.md) .</span><span class="sxs-lookup"><span data-stu-id="207d6-138">When you are finished using the entry identifier returned by **CreateOneOff**, free the memory allocated for the entry identifier by using the [MAPIFreeBuffer](mapifreebuffer.md) function.</span></span> 
  
## <a name="notes-to-transport-providers"></a><span data-ttu-id="207d6-139">Примечания для поставщиков транспорта</span><span class="sxs-lookup"><span data-stu-id="207d6-139">Notes to Transport Providers</span></span>

<span data-ttu-id="207d6-140">Поддерживает формат TNEF и используйте значение свойства **пр_сенд_рич_инфо** , чтобы определить, следует ли использовать TNEF при передаче сообщения.</span><span class="sxs-lookup"><span data-stu-id="207d6-140">Support the Transport Neutral Encapsulation Format (TNEF) and use the value of the **PR_SEND_RICH_INFO** property to determine whether to use TNEF when you transport a message.</span></span> <span data-ttu-id="207d6-141">Не поддерживает формат TNEF или не отправляется сообщение в этом формате при его запросе может быть проблемой для клиентов на основе форм или клиентов, которым требуются настраиваемые свойства MAPI.</span><span class="sxs-lookup"><span data-stu-id="207d6-141">Not supporting TNEF or not sending a message in this format when it is requested can be a problem for form-based clients or clients that require custom MAPI properties.</span></span> <span data-ttu-id="207d6-142">Это связано с тем, что TNEF обычно используется для отправки настраиваемых свойств настраиваемых классов сообщений.</span><span class="sxs-lookup"><span data-stu-id="207d6-142">This is because TNEF is typically used to send custom properties for custom message classes.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="207d6-143">См. также</span><span class="sxs-lookup"><span data-stu-id="207d6-143">See also</span></span>



[<span data-ttu-id="207d6-144">MAPIFreeBuffer</span><span class="sxs-lookup"><span data-stu-id="207d6-144">MAPIFreeBuffer</span></span>](mapifreebuffer.md)
  
[<span data-ttu-id="207d6-145">Каноническое свойство PidTagDisplayName</span><span class="sxs-lookup"><span data-stu-id="207d6-145">PidTagDisplayName Canonical Property</span></span>](pidtagdisplayname-canonical-property.md)
  
[<span data-ttu-id="207d6-146">Каноническое свойство PidTagSendRichInfo</span><span class="sxs-lookup"><span data-stu-id="207d6-146">PidTagSendRichInfo Canonical Property</span></span>](pidtagsendrichinfo-canonical-property.md)
  
[<span data-ttu-id="207d6-147">IMAPISupport: IUnknown</span><span class="sxs-lookup"><span data-stu-id="207d6-147">IMAPISupport : IUnknown</span></span>](imapisupportiunknown.md)

