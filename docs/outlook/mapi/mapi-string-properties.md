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
# <a name="mapi-string-properties"></a><span data-ttu-id="e3ab5-103">Свойства строки MAPI</span><span class="sxs-lookup"><span data-stu-id="e3ab5-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="e3ab5-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e3ab5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e3ab5-105">MAPI предоставляет три различных типа свойств для описания свойств строк:</span><span class="sxs-lookup"><span data-stu-id="e3ab5-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="e3ab5-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="e3ab5-106">PT_TSTRING</span></span>
  
<span data-ttu-id="e3ab5-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="e3ab5-107">PT_STRING8</span></span>
  
<span data-ttu-id="e3ab5-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="e3ab5-108">PT_UNICODE</span></span>
  
<span data-ttu-id="e3ab5-109">Свойства строки чаще всего определяются как PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="e3ab5-110">Тип PT_TSTRING условно компилирует один из других типов свойств строк в зависимости от того, определен ли макрос UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="e3ab5-111">PT_STRING8 описывает 8-битные null-terminated строки символов в формате ANSI; PT_UNICODE описывает строки символов с двойным byte null-terminated.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="e3ab5-112">Клиент или поставщик услуг или как клиент, так и поставщик могут выбрать для поддержки строк символов Юникод.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="e3ab5-113">Это не обязательно.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-113">It is not required.</span></span> <span data-ttu-id="e3ab5-114">Клиент, который поддерживает только PT_STRING8 строки, может работать с поставщиком, который поддерживает Юникод и наоборот.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="e3ab5-115">Чтобы включить эту интероперабельность, клиенты и поставщики услуг передают флаг , флаг MAPI_UNICODE, чтобы указать, что Юникод поддерживается методами, которые включают обмен строками символов.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="e3ab5-116">Например, предположим, что клиент поддерживает Юникод и должен получить отображаемую папку.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="e3ab5-117">Все свойства клиента PT_TSTRING, чтобы ввести PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="e3ab5-118">Когда клиент вызывает [IMAPIProp::GetProps](imapiprop-getprops.md) для получения свойства **PR_DISPLAY_NAME** [(PidTagDisplayName),](pidtagdisplayname-canonical-property.md)он передает флаг MAPI_UNICODE, чтобы попросить вернуть строку имени отображения в формате Unicode.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="e3ab5-119">Клиенты и поставщики услуг должны знать, что указание набора символов в методовом вызове — это только запрос.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="e3ab5-120">Поддержка одного или обоих наборов символов — это решение для реализации объекта.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="e3ab5-121">Однако поставщикам услуг рекомендуется поддерживать оба набора символов, так как это позволяет им добиваться более широкого распространения, чем поставщики, которые поддерживают только один набор.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="e3ab5-122">Свойства строки могут быть довольно большими, как и двоичные свойства — свойства, которые используют тип свойства PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="e3ab5-123">Чтобы облегчить работу с большими свойствами, MAPI позволяет поставщикам услуг устанавливать эти свойства для применения ограничений размера.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="e3ab5-124">Эти ограничения могут отличаться в зависимости от:</span><span class="sxs-lookup"><span data-stu-id="e3ab5-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="e3ab5-125">Читают ли свойства или пишутся.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="e3ab5-126">Как поставщик услуг реализует методы **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="e3ab5-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="e3ab5-127">Соображения, связанные с временем работы, например ограничения памяти.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="e3ab5-128">Проблемы перевода набора символов.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="e3ab5-129">Ограничения размера также могут быть размещены на свойствах строк и двоичных объектов, когда они используются в наборе столбцов таблицы, так как иногда невозможно сделать все значение большого свойства видимым.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="e3ab5-130">Многие поставщики услуг усечены большими строками или двоичными свойствами, используемыми в таблицах, до 255 bytes.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="e3ab5-131">Когда клиент вызывает метод **GetProps** или **SetProps** объекта для работы с большим свойством строки или двоичного свойства и вызов не удается из-за размера свойства, метод возвращает значение ошибки MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="e3ab5-132">Если для определенного свойства не удается **получитьПропс,** клиент может восстановиться, позвонив [в IMAPIProp::OpenProperty](imapiprop-openproperty.md) и запросив доступ к **IStream,** указав IID_IStream в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="e3ab5-133">С **помощью OpenProperty** клиент может получить большое свойство с помощью интерфейса, например **IStream,** который лучше подходит для работы с большими свойствами.</span><span class="sxs-lookup"><span data-stu-id="e3ab5-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="e3ab5-134">См. также</span><span class="sxs-lookup"><span data-stu-id="e3ab5-134">See also</span></span>



[<span data-ttu-id="e3ab5-135">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="e3ab5-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

