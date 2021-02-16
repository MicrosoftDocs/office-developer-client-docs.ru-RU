---
title: Свойства строки MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 9720b649eadecc73d84d98926674a1786796ba70
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431395"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="e9071-103">Свойства строки MAPI</span><span class="sxs-lookup"><span data-stu-id="e9071-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="e9071-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9071-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9071-105">MAPI предоставляет три различных типа свойств для описания свойств строки:</span><span class="sxs-lookup"><span data-stu-id="e9071-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="e9071-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="e9071-106">PT_TSTRING</span></span>
  
<span data-ttu-id="e9071-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e9071-107">PT_STRING8</span></span>
  
<span data-ttu-id="e9071-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e9071-108">PT_UNICODE</span></span>
  
<span data-ttu-id="e9071-109">Свойства строки чаще всего определяются как PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e9071-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="e9071-110">Тип PT_TSTRING условно компилируются в один из других типов строки в зависимости от того, определен ли макрос UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e9071-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="e9071-111">PT_STRING8 в формате ANSI описываются 8-битные строки символов, оканчивые нулями; PT_UNICODE двухбайтовую строку символов с символами с нулью.</span><span class="sxs-lookup"><span data-stu-id="e9071-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="e9071-112">Клиент или поставщик услуг или оба клиента и поставщик могут выбрать поддержку строк символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="e9071-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="e9071-113">Это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="e9071-113">It is not required.</span></span> <span data-ttu-id="e9071-114">Клиент, который поддерживает только PT_STRING8 строк, может работать с поставщиком, который поддерживает Юникод и наоборот.</span><span class="sxs-lookup"><span data-stu-id="e9071-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="e9071-115">Чтобы обеспечить такое взаимозаменяемость, клиенты и поставщики услуг передают флаг MAPI_UNICODE, чтобы указать, что Юникод поддерживается в методах, в которые включается обмен строками символов.</span><span class="sxs-lookup"><span data-stu-id="e9071-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="e9071-116">Например, предположим, что клиент поддерживает Юникод и должен получить отображаемого имени папки.</span><span class="sxs-lookup"><span data-stu-id="e9071-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="e9071-117">Все свойства PT_TSTRING клиента компилются для PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e9071-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="e9071-118">Когда клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) папки для получения свойства **PR_DISPLAY_NAME** ([PidTagDisplayName),](pidtagdisplayname-canonical-property.md)он передает флаг MAPI_UNICODE, чтобы запросить возврат строки отображаемого имени в формате Юникод.</span><span class="sxs-lookup"><span data-stu-id="e9071-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="e9071-119">Клиенты и поставщики услуг должны знать, что указание набора символов в вызове метода — это только запрос.</span><span class="sxs-lookup"><span data-stu-id="e9071-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="e9071-120">Поддержка одного или обоих наборов символов определяется реализацией объекта.</span><span class="sxs-lookup"><span data-stu-id="e9071-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="e9071-121">Однако поставщикам услуг рекомендуется поддерживать оба набора символов, так как это позволяет им обеспечить более широкое распространение, чем поставщики, которые поддерживают только один набор.</span><span class="sxs-lookup"><span data-stu-id="e9071-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="e9071-122">Строки могут быть довольно большими, как и двоичные свойства— свойства, которые используют тип свойства PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="e9071-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="e9071-123">Чтобы упростить работу с большими свойствами, MAPI позволяет поставщикам услуг устанавливать эти свойства для применения ограничений размера.</span><span class="sxs-lookup"><span data-stu-id="e9071-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="e9071-124">Эти ограничения могут отличаться в зависимости от:</span><span class="sxs-lookup"><span data-stu-id="e9071-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="e9071-125">Является ли чтение или написание свойств.</span><span class="sxs-lookup"><span data-stu-id="e9071-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="e9071-126">Способ реализации методов **IMAPIProp** поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="e9071-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="e9071-127">Вопросы, связанные со временем работы, например ограничения памяти.</span><span class="sxs-lookup"><span data-stu-id="e9071-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="e9071-128">Проблемы перевода наборов символов.</span><span class="sxs-lookup"><span data-stu-id="e9071-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="e9071-129">Ограничения размера также можно установить на строку и двоичные свойства, если они используются в наборе столбцов таблицы, так как иногда невозможно сделать видимым все значения большого свойства.</span><span class="sxs-lookup"><span data-stu-id="e9071-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="e9071-130">Многие поставщики услуг утесируют большие строковые или двоичные свойства, используемые в таблицах, до 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="e9071-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="e9071-131">Когда клиент вызывает метод **GetProps** или **SetProps** объекта для работы с большой строкой или двоичным свойством и вызов не удается из-за размера свойства, метод возвращает значение ошибки MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="e9071-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="e9071-132">Если для определенного свойства не удается получить запрос **GetProps,** клиент может восстановиться, вызывая [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и запрашивая доступ к **IStream,** указав IID_IStream в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e9071-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="e9071-133">С **помощью OpenProperty** клиент может получить большое свойство с помощью такого интерфейса, как **IStream,** который лучше подходит для работы с большими свойствами.</span><span class="sxs-lookup"><span data-stu-id="e9071-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e9071-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e9071-134">See also</span></span>



[<span data-ttu-id="e9071-135">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="e9071-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

