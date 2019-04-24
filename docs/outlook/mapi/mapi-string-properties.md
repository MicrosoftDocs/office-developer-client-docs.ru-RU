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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309522"
---
# <a name="mapi-string-properties"></a><span data-ttu-id="4eb84-103">Свойства строки MAPI</span><span class="sxs-lookup"><span data-stu-id="4eb84-103">MAPI String Properties</span></span>

  
  
<span data-ttu-id="4eb84-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="4eb84-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="4eb84-105">В ИНТЕРФЕЙСе MAPI предусмотрены три различных типа свойств, описывающих свойства String:</span><span class="sxs-lookup"><span data-stu-id="4eb84-105">MAPI provides three different property types to describe string properties:</span></span>
  
<span data-ttu-id="4eb84-106">ПТ_ТСТРИНГ</span><span class="sxs-lookup"><span data-stu-id="4eb84-106">PT_TSTRING</span></span>
  
<span data-ttu-id="4eb84-107">PT_STRING8</span><span class="sxs-lookup"><span data-stu-id="4eb84-107">PT_STRING8</span></span>
  
<span data-ttu-id="4eb84-108">PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="4eb84-108">PT_UNICODE</span></span>
  
<span data-ttu-id="4eb84-109">Строковые свойства чаще всего определяются как ПТ_ТСТРИНГ.</span><span class="sxs-lookup"><span data-stu-id="4eb84-109">String properties are most commonly defined as PT_TSTRING.</span></span> <span data-ttu-id="4eb84-110">Тип свойства ПТ_ТСТРИНГ условно компилируется в один из других типов строковых свойств в зависимости от того, был ли определен макрос UNICODE.</span><span class="sxs-lookup"><span data-stu-id="4eb84-110">The PT_TSTRING property type conditionally compiles to one of the other string property types, depending depending on whether the UNICODE macro has been defined.</span></span> <span data-ttu-id="4eb84-111">PT_STRING8 описывает 8 – битовые строки символов, заканчивающиеся нулем, в формате ANSI; ПТ_УНИКОДЕ описывает строки двухбайтовых символов, заканчивающихся нулем.</span><span class="sxs-lookup"><span data-stu-id="4eb84-111">PT_STRING8 describes 8-bit null-terminated character strings in the ANSI format; PT_UNICODE describes double-byte null-terminated character strings.</span></span> 
  
<span data-ttu-id="4eb84-112">Как клиент, так и поставщик услуг или как клиент, так и поставщик могут поддерживать строки символов Юникода.</span><span class="sxs-lookup"><span data-stu-id="4eb84-112">Either a client or a service provider, or both client and provider can choose to support Unicode character strings.</span></span> <span data-ttu-id="4eb84-113">Он не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="4eb84-113">It is not required.</span></span> <span data-ttu-id="4eb84-114">Клиент, поддерживающий только строки PT_STRING8, может работать с поставщиком, поддерживающим Юникод и наоборот.</span><span class="sxs-lookup"><span data-stu-id="4eb84-114">A client that supports only PT_STRING8 strings can operate with a provider that supports Unicode and vice versa.</span></span> <span data-ttu-id="4eb84-115">Чтобы обеспечить это взаимодействие, клиенты и поставщики услуг передают флаг, флаг МАПИ_УНИКОДЕ, чтобы указать, что Юникод поддерживается в методах, использующих обмен символьных строк.</span><span class="sxs-lookup"><span data-stu-id="4eb84-115">To enable this interoperability, clients and service providers pass a flag, the MAPI_UNICODE flag, to indicate that Unicode is supported in methods that involve the exchange of character strings.</span></span> 
  
<span data-ttu-id="4eb84-116">Например, предположим, что клиент поддерживает Юникод и требуется получить отображаемое имя папки.</span><span class="sxs-lookup"><span data-stu-id="4eb84-116">For example, suppose a client supports Unicode and needs to retrieve the display name of a folder.</span></span> <span data-ttu-id="4eb84-117">Все свойства ПТ_ТСТРИНГ клиента компилируются в тип ПТ_УНИКОДЕ.</span><span class="sxs-lookup"><span data-stu-id="4eb84-117">All of the client's PT_TSTRING properties are compiled to type PT_UNICODE.</span></span> <span data-ttu-id="4eb84-118">Когда клиент вызывает метод [IMAPIProp::](imapiprop-getprops.md) -PROPS папки для получения свойства **пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)), он передает флаг мапи_уникоде, чтобы запросить возврат строки отображаемого имени в формате Юникод .</span><span class="sxs-lookup"><span data-stu-id="4eb84-118">When the client calls the folder's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve its **PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) property, it passes the MAPI_UNICODE flag to request that the display name string be returned in the Unicode format.</span></span> 
  
<span data-ttu-id="4eb84-119">Клиенты и поставщики услуг должны знать, что при указании набора символов в вызове метода используется только запрос.</span><span class="sxs-lookup"><span data-stu-id="4eb84-119">Clients and service providers need to be aware that specifying a character set in a method call is only a request.</span></span> <span data-ttu-id="4eb84-120">Поддержка одного или обоих наборов знаков осуществляется разработчиком объекта.</span><span class="sxs-lookup"><span data-stu-id="4eb84-120">Supporting one or both character sets is up to the implementer of the object.</span></span> <span data-ttu-id="4eb84-121">Однако поставщикам услуг рекомендуется поддерживать оба набора символов, так как они позволяют им добиться более широкого распространения, чем поставщики, поддерживающие только один набор.</span><span class="sxs-lookup"><span data-stu-id="4eb84-121">However, service providers are encouraged to support both character sets because it allows them to achieve more widespread distribution than providers that support only one set.</span></span> 
  
<span data-ttu-id="4eb84-122">Строковые свойства могут увеличиваться до очень большого размера, как и двоичные свойства — свойства, использующие тип свойства ПТ_БИНАРИ.</span><span class="sxs-lookup"><span data-stu-id="4eb84-122">String properties can grow to be quite large as can binary properties — properties that use the property type PT_BINARY.</span></span> <span data-ttu-id="4eb84-123">Для упрощения работы с большими свойствами MAPI позволяет поставщикам услуг настроить эти свойства для применения ограниченности размеров.</span><span class="sxs-lookup"><span data-stu-id="4eb84-123">To ease working with large properties, MAPI allows service providers setting these properties to enforce size limits.</span></span> <span data-ttu-id="4eb84-124">Эти пределы могут различаться в зависимости от следующих условий:</span><span class="sxs-lookup"><span data-stu-id="4eb84-124">These limits can vary, depending on:</span></span>
  
- <span data-ttu-id="4eb84-125">Сведения о том, считываются ли свойства или записываются.</span><span class="sxs-lookup"><span data-stu-id="4eb84-125">Whether the properties are being read or written.</span></span>
    
- <span data-ttu-id="4eb84-126">Как поставщик услуг реализует методы **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="4eb84-126">How the service provider implements the **IMAPIProp** methods.</span></span> 
    
- <span data-ttu-id="4eb84-127">Рекомендации среды выполнения, такие как ограничения памяти.</span><span class="sxs-lookup"><span data-stu-id="4eb84-127">Runtime considerations, such as memory constraints.</span></span>
    
- <span data-ttu-id="4eb84-128">Проблемы с преобразованием набора символов.</span><span class="sxs-lookup"><span data-stu-id="4eb84-128">Character set translation issues.</span></span> 
    
<span data-ttu-id="4eb84-129">Кроме того, при использовании в наборе столбцов таблицы для свойств String и binary можно установить предельные значения размера, так как иногда невозможно сделать видимым все значения больших свойств.</span><span class="sxs-lookup"><span data-stu-id="4eb84-129">Size limits can also be placed on string and binary properties when they are used in the column set of a table because it is sometimes impossible to make all of a large property's value visible.</span></span> <span data-ttu-id="4eb84-130">Многие поставщики услуг усекаются большие строковые или двоичные свойства, используемые в таблицах до 255 байт.</span><span class="sxs-lookup"><span data-stu-id="4eb84-130">Many service providers truncate large string or binary properties that are used in tables to 255 bytes.</span></span> 
  
<span data-ttu-id="4eb84-131">Когда клиент вызывает метод GetProperty или метод \*\*\*\* **SetProps** для работы с большим строковым или двоичным свойством, а вызов завершается со сбоем из-за размера свойства, метод возвращает значение ошибки мапи_е_нот_енаугх_мемори.</span><span class="sxs-lookup"><span data-stu-id="4eb84-131">When a client calls an object's **GetProps** or **SetProps** method to work with a large string or binary property and the call fails because of the property size, the method returns the error value MAPI_E_NOT_ENOUGH_MEMORY.</span></span> <span data-ttu-id="4eb84-132">Если это **PROPS** , который отдает отказ для определенного свойства, клиент может выполнить восстановление, вызвав [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) и запрашивая интерфейс **IStream** для доступа, указав иид_истреам в качестве идентификатора интерфейса.</span><span class="sxs-lookup"><span data-stu-id="4eb84-132">If it is **GetProps** that is failing for a specific property, the client can recover by calling [IMAPIProp::OpenProperty](imapiprop-openproperty.md) and requesting the **IStream** for access by specifying IID_IStream as the interface identifier.</span></span> <span data-ttu-id="4eb84-133">С помощью **опенпроперти**клиент может получить большое свойство с помощью интерфейса **IStream** , который лучше всего подходит для работы с большими свойствами.</span><span class="sxs-lookup"><span data-stu-id="4eb84-133">Using **OpenProperty**, the client can retrieve a large property using an interface such as **IStream** that is better suited for working with large properties.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="4eb84-134">См. также</span><span class="sxs-lookup"><span data-stu-id="4eb84-134">See also</span></span>



[<span data-ttu-id="4eb84-135">Обзор свойств MAPI</span><span class="sxs-lookup"><span data-stu-id="4eb84-135">MAPI Property Overview</span></span>](mapi-property-overview.md)

