---
title: Имена свойств и наборы свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: cb216f5c-c965-4372-a15b-82090a410266
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c586d70054542e8d20c90a8caceafabbbb408de8
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812108"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="75bba-103">Имена свойств и наборы свойств</span><span class="sxs-lookup"><span data-stu-id="75bba-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="75bba-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="75bba-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="75bba-105">Имя каждого именованного свойства состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="75bba-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="75bba-106">Глобальный уникальный идентификатор, или идентификатор GUID, определяющий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="75bba-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="75bba-107">Строка Юникода символ или числовое значение 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="75bba-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="75bba-108">Имена именованных свойств, описаны с помощью структуры [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="75bba-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="75bba-109">Эта структура содержит членом набора свойств, члена для указания имени в формате числовое или строковое и члена для идентификации используется формат.</span><span class="sxs-lookup"><span data-stu-id="75bba-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="75bba-110">Так как набор свойств является частью имя свойства, не необязательно.</span><span class="sxs-lookup"><span data-stu-id="75bba-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="75bba-111">MAPI определил несколько наборов свойств для использования клиентами и поставщиков услуг, но если существующий набором свойств не подходит, можно определить новый набор свойств.</span><span class="sxs-lookup"><span data-stu-id="75bba-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="75bba-112">Клиенты и поставщиков услуг можно определить собственные наборы свойств с помощью вызова функции [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="75bba-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) function.</span></span> <span data-ttu-id="75bba-113">Обычно эти наборы свойств создаются для пользовательских клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="75bba-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="75bba-114">Наборы свойств MAPI представлены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="75bba-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="75bba-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="75bba-115">PS_MAPI</span></span>
  
<span data-ttu-id="75bba-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="75bba-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="75bba-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="75bba-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="75bba-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="75bba-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="75bba-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="75bba-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="75bba-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="75bba-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="75bba-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="75bba-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="75bba-122">Набор свойств PS_MAPI зарезервирован; используется поставщиками услуг для создания имен для свойств с идентификаторами ниже диапазона именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="75bba-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="75bba-123">Набор свойств PS_PUBLIC_STRINGS используется клиентами для именованных свойств сообщения IPM.</span><span class="sxs-lookup"><span data-stu-id="75bba-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="75bba-124">Так как имя свойства в набор свойств PS_PUBLIC_STRINGS отображаются в пользовательский интерфейс клиента, невидимый сообщения, такие как те, которые относятся к классу сообщения производственных Издержек следует избегать создания именованных свойств с набором свойств.</span><span class="sxs-lookup"><span data-stu-id="75bba-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="75bba-125">Вместо этого они создают свойства в диапазоне конкретного класса сообщений, 0x6800 через 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="75bba-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="75bba-126">Другие наборы свойств удержание именованного свойства, описывающие получателей, которые обычно являются членами маршрутизации списка.</span><span class="sxs-lookup"><span data-stu-id="75bba-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="75bba-127">Содержащий же тип данных как свойства, связанные со свойствами получателя списка свойств в эти наборы свойств распознаются шлюзов требуется сопоставление для целевой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="75bba-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="75bba-128">Поскольку существует пять типов данных, содержащие свойства, MAPI определенные наборы пяти различных свойств.</span><span class="sxs-lookup"><span data-stu-id="75bba-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="75bba-129">Задает отправке сообщение, в котором необходимо включить для его маршрутизации элементы списка адресов и тип адреса назначает именованного свойства для каждого элемента в PS_ROUTING_EMAIL_ADDRESSES и свойство PS_ROUTING_ADDRTYPE клиента.</span><span class="sxs-lookup"><span data-stu-id="75bba-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="75bba-130">Это гарантирует, что адрес и тип адреса остаются приемлемым при отправке внешнюю систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="75bba-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="75bba-131">См. также</span><span class="sxs-lookup"><span data-stu-id="75bba-131">See also</span></span>



[<span data-ttu-id="75bba-132">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="75bba-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

