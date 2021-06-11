---
title: Создание идентификаторов записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8d48c2584fa5b7e862102e401ea8165821607f77
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427950"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="10e83-103">Создание идентификаторов записей</span><span class="sxs-lookup"><span data-stu-id="10e83-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="10e83-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="10e83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="10e83-105">Идентификаторы записи построены со структурой [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="10e83-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="10e83-106">Структура **ENTRYID** состоит из флага, который описывает атрибуты идентификатора записи и фактического идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="10e83-107">Структура ENTRYID</span><span class="sxs-lookup"><span data-stu-id="10e83-107">ENTRYID Structure</span></span>

<span data-ttu-id="10e83-108">Структура **ENTRYID** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="10e83-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="10e83-109">MAPI_DIM — это константа, определяемая в файле загона MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="10e83-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="10e83-110">Первый бит участника **abFlags** с 4-byte описывает тип и использование идентификатора записи и может иметь следующие значения:</span><span class="sxs-lookup"><span data-stu-id="10e83-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="10e83-111">MAPI_NOTRECI — указывает, что идентификатор записи не может использоваться в качестве получателя в сообщении.</span><span class="sxs-lookup"><span data-stu-id="10e83-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="10e83-112">MAPI_NOTRESERVED — указывает, что другие пользователи не могут получить доступ к идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="10e83-113">MAPI_NOW — указывает, что идентификатор записи не может использоваться в другое время.</span><span class="sxs-lookup"><span data-stu-id="10e83-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="10e83-114">MAPI_SHORTTERM — указывает, что идентификатор записи является краткосрочным.</span><span class="sxs-lookup"><span data-stu-id="10e83-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="10e83-115">Все другие значения в этом byte должны быть заданной, если не разрешено другое использование идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="10e83-116">MAPI_THISSESSION — указывает, что идентификатор записи нельзя использовать на других сеансах.</span><span class="sxs-lookup"><span data-stu-id="10e83-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="10e83-117">MAPI_NOTRESERVED — указывает, что идентификатор записи может использоваться другими поставщиками услуг для других объектов.</span><span class="sxs-lookup"><span data-stu-id="10e83-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="10e83-118">Аб-элемент идентификаторов записи, созданный поставщиками адресной книги и магазина сообщений, состоит из двух частей: структуры [MAPIUID](mapiuid.md) с 16 байтами, идентифицируемой поставщиком услуг, и фрагмента для идентификации объекта. </span><span class="sxs-lookup"><span data-stu-id="10e83-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="10e83-119">**MAPIUID** — это структура, которая содержит глобальный уникальный идентификатор или GUID.</span><span class="sxs-lookup"><span data-stu-id="10e83-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="10e83-120">GUID — это идентификатор, независимый от byte-order, который можно создать с помощью средства Microsoft Visual Studio *GUID*.\*</span><span class="sxs-lookup"><span data-stu-id="10e83-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="10e83-121">Поставщик услуг регистрирует свою структуру **MAPIUID** в MAPI во время процесса логона в вызове метода [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="10e83-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="10e83-122">Когда клиент вызывает метод **OpenEntry** для доступа к объекту, MAPI использует структуру **MAPIUID,** чтобы определить, какой поставщик услуг может предоставить такой доступ.</span><span class="sxs-lookup"><span data-stu-id="10e83-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="10e83-123">Поставщики услуг должны использовать ту же **структуру MAPIUID** для всех версий их DLL.</span><span class="sxs-lookup"><span data-stu-id="10e83-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="10e83-124">Это позволяет клиентам с более новой версией отвечать на сообщения, отправленные и сохраненные в более старой версии.</span><span class="sxs-lookup"><span data-stu-id="10e83-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="10e83-125">Остальные члены **ab** после 16-byte **MAPIUID** содержат двоичные данные, определенные поставщиком услуг для идентификации определенных объектов.</span><span class="sxs-lookup"><span data-stu-id="10e83-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="10e83-126">Для этой части идентификатора записи не существует фиксированного размера.</span><span class="sxs-lookup"><span data-stu-id="10e83-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="10e83-127">Это может быть любой размер, в пределах причины.</span><span class="sxs-lookup"><span data-stu-id="10e83-127">It can be any size, within reason.</span></span> <span data-ttu-id="10e83-128">Поставщик услуг обычно содержит следующие сведения в этой части идентификаторов записи:</span><span class="sxs-lookup"><span data-stu-id="10e83-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="10e83-129">Сведения о версии . Поскольку поставщик услуг часто меняет формат идентификаторов записи с версии на версию, хранение сведений о версиях позволяет быстро определить, как расшифровать любой идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="10e83-130">Сведения о расположении — это данные, которые дают поставщику услуг индикатор поиска объекта, представленного идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="10e83-131">Например, поставщик служб может хранить смещение диска для последнего места в файле данных, который был сохранен объектом.</span><span class="sxs-lookup"><span data-stu-id="10e83-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="10e83-132">Поскольку этот тип информации может изменяться со временем, поставщики услуг должны предоставить несколько способов для размещения объектов в идентификаторах записи.</span><span class="sxs-lookup"><span data-stu-id="10e83-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="10e83-133">Хотя поставщики услуг могут повторно использовать идентификаторы записей, они должны избегать этой практики.</span><span class="sxs-lookup"><span data-stu-id="10e83-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="10e83-134">Если требуется повторное использование идентификатора записи, поставщики услуг должны сделать период времени между начальным использованием и повторное использование как можно более длительным.</span><span class="sxs-lookup"><span data-stu-id="10e83-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="10e83-135">Кроме того, идентификатор записи должен быть повторно назначен другому объекту того же типа.</span><span class="sxs-lookup"><span data-stu-id="10e83-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="10e83-136">То есть определенный идентификатор записи не должен быть связан сначала с сообщением, а затем с папкой.</span><span class="sxs-lookup"><span data-stu-id="10e83-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="10e83-137">См. также</span><span class="sxs-lookup"><span data-stu-id="10e83-137">See also</span></span>



[<span data-ttu-id="10e83-138">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="10e83-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

