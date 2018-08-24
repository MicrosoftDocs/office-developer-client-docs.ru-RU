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
ms.openlocfilehash: 0272464d9a397f169b27aa15c80a17b49a3e9977
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22571831"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="768d6-103">Имена свойств и наборы свойств</span><span class="sxs-lookup"><span data-stu-id="768d6-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="768d6-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="768d6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="768d6-105">Имя каждого именованного свойства состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="768d6-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="768d6-106">Глобальный уникальный идентификатор, или идентификатор GUID, определяющий набор свойств.</span><span class="sxs-lookup"><span data-stu-id="768d6-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="768d6-107">Строка Юникода символ или числовое значение 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="768d6-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="768d6-108">Имена именованных свойств, описаны с помощью структуры [MAPINAMEID](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="768d6-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="768d6-109">Эта структура содержит членом набора свойств, члена для указания имени в формате числовое или строковое и члена для идентификации используется формат.</span><span class="sxs-lookup"><span data-stu-id="768d6-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="768d6-110">Так как набор свойств является частью имя свойства, не необязательно.</span><span class="sxs-lookup"><span data-stu-id="768d6-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="768d6-111">MAPI определил несколько наборов свойств для использования клиентами и поставщиков услуг, но если существующий набором свойств не подходит, можно определить новый набор свойств.</span><span class="sxs-lookup"><span data-stu-id="768d6-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="768d6-112">Клиенты и поставщиков услуг можно определить собственные наборы свойств с помощью вызова функции [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="768d6-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](http://msdn.microsoft.com/en-us/library/ms688568.aspx) function.</span></span> <span data-ttu-id="768d6-113">Обычно эти наборы свойств создаются для пользовательских клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="768d6-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="768d6-114">Наборы свойств MAPI представлены следующие константы:</span><span class="sxs-lookup"><span data-stu-id="768d6-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="768d6-115">PS_MAPI</span><span class="sxs-lookup"><span data-stu-id="768d6-115">PS_MAPI</span></span>
  
<span data-ttu-id="768d6-116">PS_PUBLIC_STRINGS</span><span class="sxs-lookup"><span data-stu-id="768d6-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="768d6-117">PS_ROUTING_EMAIL_ADDRESSES</span><span class="sxs-lookup"><span data-stu-id="768d6-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="768d6-118">PS_ROUTING_ADDRTYPE</span><span class="sxs-lookup"><span data-stu-id="768d6-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="768d6-119">PS_ROUTING_SEARCH_KEY</span><span class="sxs-lookup"><span data-stu-id="768d6-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="768d6-120">PS_ROUTING_DISPLAY_NAME</span><span class="sxs-lookup"><span data-stu-id="768d6-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="768d6-121">PS_ROUTING_ENTRYID</span><span class="sxs-lookup"><span data-stu-id="768d6-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="768d6-122">Набор свойств PS_MAPI зарезервирован; используется поставщиками услуг для создания имен для свойств с идентификаторами ниже диапазона именованное свойство.</span><span class="sxs-lookup"><span data-stu-id="768d6-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="768d6-123">Набор свойств PS_PUBLIC_STRINGS используется клиентами для именованных свойств сообщения IPM.</span><span class="sxs-lookup"><span data-stu-id="768d6-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="768d6-124">Так как имя свойства в набор свойств PS_PUBLIC_STRINGS отображаются в пользовательский интерфейс клиента, невидимый сообщения, такие как те, которые относятся к классу сообщения производственных Издержек следует избегать создания именованных свойств с набором свойств.</span><span class="sxs-lookup"><span data-stu-id="768d6-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="768d6-125">Вместо этого они создают свойства в диапазоне конкретного класса сообщений, 0x6800 через 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="768d6-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="768d6-126">Другие наборы свойств удержание именованного свойства, описывающие получателей, которые обычно являются членами маршрутизации списка.</span><span class="sxs-lookup"><span data-stu-id="768d6-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="768d6-127">Содержащий же тип данных как свойства, связанные со свойствами получателя списка свойств в эти наборы свойств распознаются шлюзов требуется сопоставление для целевой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="768d6-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="768d6-128">Поскольку существует пять типов данных, содержащие свойства, MAPI определенные наборы пяти различных свойств.</span><span class="sxs-lookup"><span data-stu-id="768d6-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="768d6-129">Задает отправке сообщение, в котором необходимо включить для его маршрутизации элементы списка адресов и тип адреса назначает именованного свойства для каждого элемента в PS_ROUTING_EMAIL_ADDRESSES и свойство PS_ROUTING_ADDRTYPE клиента.</span><span class="sxs-lookup"><span data-stu-id="768d6-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="768d6-130">Это гарантирует, что адрес и тип адреса остаются приемлемым при отправке внешнюю систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="768d6-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="768d6-131">См. также</span><span class="sxs-lookup"><span data-stu-id="768d6-131">See also</span></span>



[<span data-ttu-id="768d6-132">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="768d6-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

