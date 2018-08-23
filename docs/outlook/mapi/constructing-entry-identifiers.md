---
title: Составление идентификаторов записей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bc2a9116-948e-4da3-96b8-26d73bcd63c4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f15749077596bd6c89828eb730cadd5624a75fe1
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22564586"
---
# <a name="constructing-entry-identifiers"></a><span data-ttu-id="a6fb5-103">Составление идентификаторов записей</span><span class="sxs-lookup"><span data-stu-id="a6fb5-103">Constructing Entry Identifiers</span></span>

  
  
<span data-ttu-id="a6fb5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="a6fb5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="a6fb5-105">Идентификаторы записей, созданные со структурой [ENTRYID](entryid.md) .</span><span class="sxs-lookup"><span data-stu-id="a6fb5-105">Entry identifiers are constructed with the [ENTRYID](entryid.md) structure.</span></span> <span data-ttu-id="a6fb5-106">Структура **ENTRYID** состоит из флаг, описывающий атрибуты идентификатор записи и идентификатор фактический записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-106">The **ENTRYID** structure is composed of a flag that describes the attributes of the entry identifier and the actual entry identifier.</span></span> 
  
## <a name="entryid-structure"></a><span data-ttu-id="a6fb5-107">Идентификатор записи структуры</span><span class="sxs-lookup"><span data-stu-id="a6fb5-107">ENTRYID Structure</span></span>

<span data-ttu-id="a6fb5-108">Структура **ENTRYID** определяется следующим образом:</span><span class="sxs-lookup"><span data-stu-id="a6fb5-108">The **ENTRYID** structure is defined as follows:</span></span> 
  
```cpp
typedef struct
{
    BYTE        abFlags[4];
    BYTE        ab[MAPI_DIM];
}  ENTRYID, FAR *LPENTRYID;
 
```

<span data-ttu-id="a6fb5-109">MAPI_DIM — это константа, определенные в файле заголовка MapiDefs.h.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-109">MAPI_DIM is a constant that is defined in the MapiDefs.h header file.</span></span> 
  
<span data-ttu-id="a6fb5-110">Получения первого байта член 4-байтных **abFlags** описывает тип и использовать запись идентификатора и может принимать следующие значения:</span><span class="sxs-lookup"><span data-stu-id="a6fb5-110">The first byte of the 4-byte **abFlags** member describes the type and use of the entry identifier and can have the following values:</span></span> 
  
- <span data-ttu-id="a6fb5-111">MAPI_NOTRECI — Указывает идентификатор записи не может использоваться в качестве получателей на сообщение.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-111">MAPI_NOTRECI — Indicates the entry identifier cannot be used as a recipient on a message.</span></span>
    
- <span data-ttu-id="a6fb5-112">MAPI_NOTRESERVED — Указывает, что другие пользователи не могут получить доступ к идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-112">MAPI_NOTRESERVED — Indicates that other users cannot access the entry identifier.</span></span>
    
- <span data-ttu-id="a6fb5-113">MAPI_NOW — Указывает, что идентификатор записи не может использоваться в других случаях.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-113">MAPI_NOW — Indicates that the entry identifier cannot be used at other times.</span></span>
    
- <span data-ttu-id="a6fb5-114">MAPI_SHORTTERM — Указывает, что идентификатор записи краткосрочных.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-114">MAPI_SHORTTERM — Indicates that the entry identifier is short-term.</span></span> <span data-ttu-id="a6fb5-115">Все значения в этом байтов должно иметь значение, если не разрешены других способов использования идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-115">All other values in this byte must be set unless other uses of the entry identifier are allowed.</span></span>
    
- <span data-ttu-id="a6fb5-116">MAPI_THISSESSION — Указывает, что идентификатор записи не может использоваться для других сеансов.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-116">MAPI_THISSESSION — Indicates that the entry identifier cannot be used on other sessions.</span></span>
    
- <span data-ttu-id="a6fb5-117">MAPI_NOTRESERVED — Указывает, что идентификатор записи можно использовать другие поставщики услуг для других объектов.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-117">MAPI_NOTRESERVED — Indicates that the entry identifier can be used by other service providers for other objects.</span></span>
    
<span data-ttu-id="a6fb5-118">Член **ab** идентификаторов запись, которая создается по поставщиков хранилища адресной книги и сообщения состоит из двух частей: структура [MAPIUID](mapiuid.md) 16-битное, определяет поставщик услуг и фрагмент для идентификации объекта.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-118">The **ab** member of entry identifiers that is created by address book and message store providers is composed of two pieces: a 16-byte [MAPIUID](mapiuid.md) structure that identifies the service provider, and a piece to identify the object.</span></span> <span data-ttu-id="a6fb5-119">**MAPIUID** — это структура, содержащая идентификатор GUID, или идентификатор GUID.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-119">**MAPIUID** is a structure that contains a globally unique identifier, or GUID.</span></span> <span data-ttu-id="a6fb5-120">GUID — это идентификатор байтов порядке независимо, можно создать с помощью Microsoft Visual Studio*Создать GUID*\* средство.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-120">A GUID is a byte-order-independent identifier that can be created by using the Microsoft Visual Studio*Create GUID*\* tool.</span></span> 
  
<span data-ttu-id="a6fb5-121">При входе в вызов метода [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) поставщика услуг регистрирует его структуры **MAPIUID** MAPI.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-121">A service provider registers its **MAPIUID** structure with MAPI during the logon process in a call to the [IMAPISupport::SetProviderUID](imapisupport-setprovideruid.md) method.</span></span> <span data-ttu-id="a6fb5-122">Когда клиент вызывает метод **OpenEntry** для доступа к объекту, MAPI использует структуру **MAPIUID** для определения, какой службе поставщика можно обеспечить доступа.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-122">When a client calls an **OpenEntry** method to access an object, MAPI uses the **MAPIUID** structure to determine which service provider can provide that access.</span></span> <span data-ttu-id="a6fb5-123">Поставщики услуг следует использовать одну и ту же структуру **MAPIUID** для всех версий их DLL.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-123">Service providers should use the same **MAPIUID** structure for all versions of their DLL.</span></span> <span data-ttu-id="a6fb5-124">Это позволяет клиентам с новой версией отвечать на сообщения, отправленные и сохранения с более ранними версиями.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-124">This enables clients with the newer version to respond to messages sent and saved with the older version.</span></span> 
  
<span data-ttu-id="a6fb5-125">Остальная часть член **ab** после 16-битное **MAPIUID** содержит двоичные данные службы поставщика для идентификации определенных объектов.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-125">The rest of the **ab** member after the 16-byte **MAPIUID** contains service-provider-specific binary data for identifying particular objects.</span></span> <span data-ttu-id="a6fb5-126">Нет нет фиксированного размера для этой части идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-126">There is no fixed size for this portion of the entry identifier.</span></span> <span data-ttu-id="a6fb5-127">Она может быть любого размера, в рамках причине.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-127">It can be any size, within reason.</span></span> <span data-ttu-id="a6fb5-128">Поставщик службы обычно включает в себя следующие сведения в этой части его идентификаторы записей:</span><span class="sxs-lookup"><span data-stu-id="a6fb5-128">A service provider typically includes the following information in this part of its entry identifiers:</span></span> 
  
- <span data-ttu-id="a6fb5-129">Сведения о версии, поскольку типичные для поставщика услуг для изменения формата его идентификаторы записей из одной версии на другую, хранение сведений о версии позволяет быстро определить, как для дешифрования любой идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-129">Version information — Because it is common for a service provider to change the format of its entry identifiers from version to version, storing version information makes it possible to quickly determine how to decipher any entry identifier.</span></span>
    
- <span data-ttu-id="a6fb5-130">Сведения о расположении — сведения о расположении — данные, задающей поставщика услуг показывает, как найти объекта, представленного идентификатор записи.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-130">Location information — Location information is data that gives a service provider an indicator of how to locate the object represented by the entry identifier.</span></span> <span data-ttu-id="a6fb5-131">Например поставщик службы можно хранить диска смещение для последнего позицию в файл данных, что объект был сохранен.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-131">For example, a service provider can store the disk offset for the last place in a data file that the object was stored.</span></span> <span data-ttu-id="a6fb5-132">Так как этот тип данных можно изменить со временем, поставщиков услуг следует предоставить несколько способов для поиска объектов в их идентификаторы записей.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-132">Because this type of information can change over time, service providers should provide multiple ways for locating objects in their entry identifiers.</span></span>
    
<span data-ttu-id="a6fb5-133">Хотя для поставщиков услуг может повторно их идентификаторы записей, их следует избегать этого практического занятия.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-133">Although service providers can recycle their entry identifiers, they should avoid this practice.</span></span> <span data-ttu-id="a6fb5-134">Если это необходимо для повторного использования идентификатор входа, поставщиков услуг должна потратить между начальной использования и повторного использования, в течение периода времени.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-134">If it is necessary to reuse an entry identifier, service providers should make the time period that elapses between the initial use and the reuse as long as possible.</span></span> <span data-ttu-id="a6fb5-135">Кроме того идентификатор записи должен быть назначен другой объект того же типа.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-135">Also, the entry identifier should be reassigned to another object of the same type.</span></span> <span data-ttu-id="a6fb5-136">То есть идентификатор конкретной записи не должны быть связаны сначала с сообщением, а затем с папкой.</span><span class="sxs-lookup"><span data-stu-id="a6fb5-136">That is, a particular entry identifier should not be associated first with a message and then with a folder.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a6fb5-137">См. также</span><span class="sxs-lookup"><span data-stu-id="a6fb5-137">See also</span></span>



[<span data-ttu-id="a6fb5-138">Идентификаторы MAPI записей</span><span class="sxs-lookup"><span data-stu-id="a6fb5-138">MAPI Entry Identifiers</span></span>](mapi-entry-identifiers.md)

