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
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="22993-103">Создание идентификаторов записей</span><span class="sxs-lookup"><span data-stu-id="22993-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="22993-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="22993-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="22993-105">Идентификаторы записей построены с помощью структуры [ENTRYID.](entryid.md)</span><span class="sxs-lookup"><span data-stu-id="22993-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="22993-106">Структура **ENTRYID** состоит из флага, который описывает атрибуты идентификатора записи и фактического идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="22993-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="22993-107">Структура ENTRYID</span><span class="sxs-lookup"><span data-stu-id="22993-107">ENTRYID Structure</span></span>

<span data-ttu-id="22993-108">Структура **ENTRYID** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="22993-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="22993-109">MAPI_DIM это константа, заданная в файле загона MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="22993-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="22993-110">Первый byte из 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span><span class="sxs-lookup"><span data-stu-id="22993-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="22993-111">MAPI_NOTRECI — указывает, что идентификатор записи нельзя использовать в качестве получателя сообщения.</span><span class="sxs-lookup"><span data-stu-id="22993-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="22993-112">MAPI_NOTRESERVED — указывает, что другие пользователи не могут получить доступ к идентификатору записи.</span><span class="sxs-lookup"><span data-stu-id="22993-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="22993-113">MAPI_NOW — указывает, что идентификатор записи нельзя использовать в другое время.</span><span class="sxs-lookup"><span data-stu-id="22993-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="22993-114">MAPI_SHORTTERM — указывает, что идентификатор записи является краткосрочным.</span><span class="sxs-lookup"><span data-stu-id="22993-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="22993-115">Все остальные значения в этом byte необходимо устанавливать, если не разрешено другое использование идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="22993-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="22993-116">MAPI_THISSESSION — указывает, что идентификатор записи нельзя использовать в других сеансах.</span><span class="sxs-lookup"><span data-stu-id="22993-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="22993-117">MAPI_NOTRESERVED — указывает, что идентификатор записи может использоваться другими поставщиками служб для других объектов.</span><span class="sxs-lookup"><span data-stu-id="22993-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="22993-118">Элемент **ab** идентификаторов записей, созданный поставщиками адресной книги и магазина сообщений, состоит из двух частей: 16-байтовой структуры [MAPIUID,](mapiuid.md) которая идентифицирует поставщика услуг, и фрагмента для идентификации объекта.</span><span class="sxs-lookup"><span data-stu-id="22993-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="22993-119">**MAPIUID** — это структура, которая содержит глобальный уникальный идентификатор или GUID.</span><span class="sxs-lookup"><span data-stu-id="22993-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="22993-120">GUID — это независимый от порядка в порядке использования идентификатор, который можно создать с помощью средства Microsoft Visual Studio \*Create GUID\*\*.</span><span class="sxs-lookup"><span data-stu-id="22993-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio *Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="22993-121">Поставщик услуг регистрирует свою структуру **MAPIUID** с помощью MAPI во время процесса регистрации в вызове метода [IMAPISupport::SetProviderUID.](imapisupport-setprovideruid.md)</span><span class="sxs-lookup"><span data-stu-id="22993-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="22993-122">Когда клиент вызывает метод **OpenEntry** для доступа к объекту, MAPI использует структуру **MAPIUID,** чтобы определить, какой поставщик услуг может предоставить такой доступ.</span><span class="sxs-lookup"><span data-stu-id="22993-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="22993-123">Поставщики услуг должны использовать ту же **структуру MAPIUID** для всех версий своих DLL.</span><span class="sxs-lookup"><span data-stu-id="22993-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="22993-124">Это позволяет клиентам с более новой версией реагировать на сообщения, отправленные и сохраненные в более старой версии.</span><span class="sxs-lookup"><span data-stu-id="22993-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="22993-125">Остальная часть **ab-члена** после 16-byte **MAPIUID** содержит двоичные данные поставщика услуг для идентификации определенных объектов.</span><span class="sxs-lookup"><span data-stu-id="22993-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="22993-126">Для этой части идентификатора записи фиксированный размер не существует.</span><span class="sxs-lookup"><span data-stu-id="22993-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="22993-127">Это может быть любой размер по причине.</span><span class="sxs-lookup"><span data-stu-id="22993-127">It can be any size, within reason.</span></span> <span data-ttu-id="22993-128">Поставщик услуг обычно включает в эту часть идентификаторов записей следующие сведения:</span><span class="sxs-lookup"><span data-stu-id="22993-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="22993-129">Сведения о версии — так как поставщик службы часто меняет формат идентификаторов записей с версии на версию, хранение сведений о версии позволяет быстро определить способ расшифровки любого идентификатора записи.</span><span class="sxs-lookup"><span data-stu-id="22993-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="22993-130">Сведения о расположении — это данные, которые дают поставщику услуг индикатор того, как найти объект, представленный идентификатором записи.</span><span class="sxs-lookup"><span data-stu-id="22993-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="22993-131">Например, поставщик службы может сохранить смещение диска для последнего места в файле данных, в который был сохранен объект.</span><span class="sxs-lookup"><span data-stu-id="22993-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="22993-132">Поскольку этот тип информации может со временем изменяться, поставщики услуг должны предоставлять несколько способов для размещения объектов в идентификаторах записей.</span><span class="sxs-lookup"><span data-stu-id="22993-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="22993-133">Хотя поставщики услуг могут перезахламить свои идентификаторы записей, следует избегать этой практики.</span><span class="sxs-lookup"><span data-stu-id="22993-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="22993-134">Если необходимо повторно использовать идентификатор записи, поставщики услуг должны сделать период времени между первоначальным использованием и повторное использование как можно больше.</span><span class="sxs-lookup"><span data-stu-id="22993-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="22993-135">Кроме того, идентификатор записи должен быть перена назначен другому объекту того же типа.</span><span class="sxs-lookup"><span data-stu-id="22993-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="22993-136">То есть определенный идентификатор записи не должен быть связан сначала с сообщением, а затем с папкой.</span><span class="sxs-lookup"><span data-stu-id="22993-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22993-137">См. также</span><span class="sxs-lookup"><span data-stu-id="22993-137">See also</span></span>



[<span data-ttu-id="22993-138">Идентификаторы записей MAPI</span><span class="sxs-lookup"><span data-stu-id="22993-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

