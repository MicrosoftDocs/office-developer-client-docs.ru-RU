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
ms.openlocfilehash: fa9d6afcaf1b360f37e8c8873c9d1a823fcd4888
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328548"
---
# <a name="property-names-and-property-sets"></a><span data-ttu-id="61e04-103">Имена свойств и наборы свойств</span><span class="sxs-lookup"><span data-stu-id="61e04-103">Property Names and Property Sets</span></span>

  
  
<span data-ttu-id="61e04-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="61e04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="61e04-105">Имя каждого именованного свойства состоит из двух частей:</span><span class="sxs-lookup"><span data-stu-id="61e04-105">The name of every named property has two parts:</span></span>
  
- <span data-ttu-id="61e04-106">Глобальный уникальный идентификатор (GUID), который указывает набор свойств.</span><span class="sxs-lookup"><span data-stu-id="61e04-106">A globally unique identifier, or GUID, that specifies a property set.</span></span>
    
- <span data-ttu-id="61e04-107">Строка символов Юникода или 32 — разрядное числовое значение.</span><span class="sxs-lookup"><span data-stu-id="61e04-107">A Unicode character string or 32-bit numeric value.</span></span> 
    
<span data-ttu-id="61e04-108">Имена именованных свойств описаны с помощью структуры [мапинамеид](mapinameid.md) .</span><span class="sxs-lookup"><span data-stu-id="61e04-108">Names of named properties are described using a [MAPINAMEID](mapinameid.md) structure.</span></span> <span data-ttu-id="61e04-109">Эта структура содержит элемент набора свойств, член для указания имени в числовом или строковом формате, а также член для определения используемого формата.</span><span class="sxs-lookup"><span data-stu-id="61e04-109">This structure contains a property set member, a member for specifying the name in either numeric or string format, and a member for identifying which format is used.</span></span> <span data-ttu-id="61e04-110">Так как набор свойств является частью имени свойства, он не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="61e04-110">Because the property set is part of the property's name, it is not optional.</span></span> <span data-ttu-id="61e04-111">В ИНТЕРФЕЙСе MAPI определено несколько наборов свойств для использования клиентами и поставщиками услуг, но если существующий набор свойств не подходит, можно определить новый набор свойств.</span><span class="sxs-lookup"><span data-stu-id="61e04-111">MAPI has defined several property sets for use by clients and service providers, but if an existing property set is inappropriate, a new property set can be defined.</span></span> <span data-ttu-id="61e04-112">Клиенты и поставщики услуг могут определять собственные наборы свойств, вызывая функцию [кокреатегуид](https://msdn.microsoft.com/library/ms688568.aspx) .</span><span class="sxs-lookup"><span data-stu-id="61e04-112">Clients and service providers can define their own property sets by calling [CoCreateGUID](https://msdn.microsoft.com/library/ms688568.aspx) function.</span></span> <span data-ttu-id="61e04-113">Как правило, эти наборы свойств создаются для пользовательских клиентских приложений.</span><span class="sxs-lookup"><span data-stu-id="61e04-113">Typically these property sets are created for custom client applications.</span></span> 
  
<span data-ttu-id="61e04-114">Наборы свойств MAPI представлены следующими константами:</span><span class="sxs-lookup"><span data-stu-id="61e04-114">MAPI's property sets are represented by the following constants:</span></span>
  
<span data-ttu-id="61e04-115">ПС_МАПИ</span><span class="sxs-lookup"><span data-stu-id="61e04-115">PS_MAPI</span></span>
  
<span data-ttu-id="61e04-116">ПС_ПУБЛИК_СТРИНГС</span><span class="sxs-lookup"><span data-stu-id="61e04-116">PS_PUBLIC_STRINGS</span></span>
  
<span data-ttu-id="61e04-117">ПС_РАУТИНГ_ЕМАИЛ_АДДРЕССЕС</span><span class="sxs-lookup"><span data-stu-id="61e04-117">PS_ROUTING_EMAIL_ADDRESSES</span></span>
  
<span data-ttu-id="61e04-118">ПС_РАУТИНГ_АДДРТИПЕ</span><span class="sxs-lookup"><span data-stu-id="61e04-118">PS_ROUTING_ADDRTYPE</span></span>
  
<span data-ttu-id="61e04-119">ПС_РАУТИНГ_СЕАРЧ_КЭЙ</span><span class="sxs-lookup"><span data-stu-id="61e04-119">PS_ROUTING_SEARCH_KEY</span></span>
  
<span data-ttu-id="61e04-120">ПС_РАУТИНГ_ДИСПЛАЙ_НАМЕ</span><span class="sxs-lookup"><span data-stu-id="61e04-120">PS_ROUTING_DISPLAY_NAME</span></span>
  
<span data-ttu-id="61e04-121">ПС_РАУТИНГ_ЕНТРИД</span><span class="sxs-lookup"><span data-stu-id="61e04-121">PS_ROUTING_ENTRYID</span></span>
  
<span data-ttu-id="61e04-122">Значение свойства ПС_МАПИ зарезервировано; Он используется поставщиками услуг для создания имен свойств с идентификаторами под именованным свойством Range.</span><span class="sxs-lookup"><span data-stu-id="61e04-122">The PS_MAPI property set is reserved; it is used by service providers to generate names for properties with identifiers below the named property range.</span></span> <span data-ttu-id="61e04-123">Набор свойств ПС_ПУБЛИК_СТРИНГС используется клиентами для именованных свойств сообщений IPM.</span><span class="sxs-lookup"><span data-stu-id="61e04-123">The PS_PUBLIC_STRINGS property set is used by clients for named properties of IPM messages.</span></span> <span data-ttu-id="61e04-124">Так как именованные свойства в наборе свойств ПС_ПУБЛИК_СТРИНГС отображаются в пользовательском интерфейсе клиента, невидимые сообщения, например те, которые относятся к классу сообщений IPC, не должны создавать именованные свойства с этим набором свойств.</span><span class="sxs-lookup"><span data-stu-id="61e04-124">Because named properties in the PS_PUBLIC_STRINGS property set appear in a client's user interface, nonvisible messages such as those that belong to the IPC message class should avoid creating named properties with this property set.</span></span> <span data-ttu-id="61e04-125">Вместо этого они должны создавать свойства в диапазоне, определяемом классом Message, в 0x6800 до 0x7FFF.</span><span class="sxs-lookup"><span data-stu-id="61e04-125">Instead, they should create properties in the message class-specific range, 0x6800 through 0x7FFF.</span></span>
  
<span data-ttu-id="61e04-126">В других наборах свойств хранятся именованные свойства, описывающие получателей, которые обычно являются участниками списка маршрутизации.</span><span class="sxs-lookup"><span data-stu-id="61e04-126">The other property sets hold named properties describing recipients that are typically members of a routing list.</span></span> <span data-ttu-id="61e04-127">Содержит сведения того же типа, что и свойства, связанные со свойствами списка получателей, свойства в этих наборах свойств, понятные шлюзам, требуют сопоставления для целевой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="61e04-127">Containing the same type of information as the properties that are associated with recipient list properties, properties in these property sets are understood by gateways to require mapping for a target messaging system.</span></span> <span data-ttu-id="61e04-128">Так как для описания свойств используется пять типов информации, в MAPI определено пять различных наборов свойств.</span><span class="sxs-lookup"><span data-stu-id="61e04-128">Because there are five types of information for describing properties, MAPI has defined five different property sets.</span></span> <span data-ttu-id="61e04-129">Клиент, отправляющий сообщение, которое должно содержать адрес и тип адреса для членов списка маршрутизации, назначает именованное свойство для каждого элемента в наборах свойств ПС_РАУТИНГ_ЕМАИЛ_АДДРЕССЕС и ПС_РАУТИНГ_АДДРТИПЕ.</span><span class="sxs-lookup"><span data-stu-id="61e04-129">A client sending a message that must include an address and address type for its routing list members assigns a named property for each member in the PS_ROUTING_EMAIL_ADDRESSES and PS_ROUTING_ADDRTYPE property sets.</span></span> <span data-ttu-id="61e04-130">Это гарантирует, что адрес и тип адреса оставались действительными при отправке в инородную систему обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="61e04-130">This ensures that the address and address type remain viable when sent to a foreign messaging system.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="61e04-131">См. также</span><span class="sxs-lookup"><span data-stu-id="61e04-131">See also</span></span>



[<span data-ttu-id="61e04-132">Именованные свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="61e04-132">MAPI Named Properties</span></span>](mapi-named-properties.md)

