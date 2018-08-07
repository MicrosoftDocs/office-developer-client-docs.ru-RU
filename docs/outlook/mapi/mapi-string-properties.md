---
title: Строковые свойства MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 63d7360a-e3a3-4365-9d46-50df1c715bde
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3cf118866bbc305678201a42a9a91998334f5cb0
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809844"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="2a8fc-103">Строковые свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="2a8fc-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="2a8fc-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="2a8fc-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="2a8fc-105">MAPI предоставляет три различных типа свойств для описания строковые свойства:</span><span class="sxs-lookup"><span data-stu-id="2a8fc-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="2a8fc-106">PT_TSTRING</span><span class="sxs-lookup"><span data-stu-id="2a8fc-106">PT_TSTRING</span></span>
  
<span data-ttu-id="2a8fc-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="2a8fc-107">PT_STRING8</span></span>
  
<span data-ttu-id="2a8fc-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="2a8fc-108">PT_UNICODE</span></span>
  
<span data-ttu-id="2a8fc-109">Строка чаще всего определены как PT_TSTRING.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="2a8fc-110">Тип свойства PT_TSTRING условно компилирует к одному из других типов свойств строку, в зависимости от того, в зависимости от того, было определено ли макрос Юникод.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="2a8fc-111">PT_STRING8 описывает 8-разрядных символом null строк в формате ANSI. PT_UNICODE описание символом null двухбайтовой строк.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="2a8fc-112">Либо клиента или поставщика услуг или клиента и поставщика можно выбрать для поддержки знаков Юникод.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="2a8fc-113">Не требуется.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-113">It is not required.</span></span> <span data-ttu-id="2a8fc-114">Клиент, который поддерживает только PT_STRING8 строк может работать с поставщиком, который поддерживает Юникод и наоборот.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="2a8fc-115">Чтобы включить этот взаимодействие, клиентов и поставщиков услуг передайте флаг, флаг MAPI_UNICODE для указания поддержки Юникод в методах, в которых используются exchange строк символов.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="2a8fc-116">Предположим, например, клиент поддерживает Юникод и требуется получить отображаемое имя папки.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="2a8fc-117">Все свойства PT_TSTRING клиента компилируются в введите PT_UNICODE.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="2a8fc-118">Если клиент вызывает метод [IMAPIProp::GetProps](imapiprop-getprops.md) папки для получения его свойство **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), он передает флаг MAPI_UNICODE для запроса возвращение строку отображаемое имя в формате Юникод .</span><span class="sxs-lookup"><span data-stu-id="2a8fc-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="2a8fc-119">Клиенты и поставщики услуг следует знать, определяющее набор символов в вызове метода представляет собой запрос.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="2a8fc-120">Поддержка одного или обоих наборов знаков — специалист по реализации объекта.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="2a8fc-121">Тем не менее поставщиков услуг, рекомендуется для поддержки оба набора символов, так как он позволяет добиться более распространенными рассылки более поставщиков, которые поддерживают только один набор.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="2a8fc-122">Строковые свойства при изменении быть большого как двоичные свойства — свойства, используйте свойство введите PT_BINARY.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="2a8fc-123">Для облегчения работы с большой свойств MAPI позволяет поставщиков услуг Установка этих свойств для принудительного применения ограничения размера.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="2a8fc-124">Эти ограничения могут различаться, в зависимости от:</span><span class="sxs-lookup"><span data-stu-id="2a8fc-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="2a8fc-125">Выполняется ли свойства для чтения или записи.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="2a8fc-126">Как поставщик услуг реализует методы **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="2a8fc-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="2a8fc-127">Вопросы среды выполнения, в том числе объемом доступной памяти.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="2a8fc-128">Проблемы преобразования наборов символов.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="2a8fc-129">Ограничения на размер можно разместить на строку и двоичные свойства, если они используются в столбце задан таблицы, так как в некоторых случаях невозможно отобразить все значения для крупных свойства.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="2a8fc-130">Многие поставщики услуг усекать больших строка или двоичные свойства, используемые в таблицах до 255 байт.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="2a8fc-131">Когда клиент вызывает метод **GetProps** или **SetProps** объекта для работы с большой строку или двоичного свойства и завершается неудачно из-за размера свойства, метод возвращает значение ошибки MAPI_E_NOT_ENOUGH_MEMORY.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="2a8fc-132">Если это ошибочных для конкретного свойства **GetProps** клиента можно восстановить путем вызова [IMAPIProp::OpenProperty](imapiprop-openproperty.md) и разрешения на запрос **IStream** для доступа, указав в качестве идентификатора интерфейса IID_IStream.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="2a8fc-133">С помощью **OpenProperty**, можно получить большой свойства с помощью интерфейса, таких как **IStream** , который лучше всего подходит для работы с большой свойства.</span><span class="sxs-lookup"><span data-stu-id="2a8fc-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2a8fc-134">См. также</span><span class="sxs-lookup"><span data-stu-id="2a8fc-134">See also</span></span>



[<span data-ttu-id="2a8fc-135">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="2a8fc-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

