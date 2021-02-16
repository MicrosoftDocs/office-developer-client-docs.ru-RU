---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в XML-схеме поставщика OSC позволяет поставщику OSC указывать его функции. К таким функциям относятся следующие:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435007"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="55e1a-104">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="55e1a-104">XML for capabilities</span></span>

<span data-ttu-id="55e1a-105">Элемент **capabilities** в XML-схеме поставщика OSC позволяет поставщику OSC указывать его функции.</span><span class="sxs-lookup"><span data-stu-id="55e1a-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="55e1a-106">К таким функциям относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="55e1a-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="55e1a-107">Поддерживает ли поставщик получение, кэшинг или динамический поиск друзей и действий из социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55e1a-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="55e1a-108">Как OSC должен отображать определенные пользовательские интерфейсы для логотипа.</span><span class="sxs-lookup"><span data-stu-id="55e1a-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="55e1a-109">Должен ли OSC использовать проверку подлинности на основе форм или автоматически настраивать социальные сети и журналы пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="55e1a-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="55e1a-110">Схема XML для  возможностей имеет критическое значение, так как она определяет для OSC функции, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="55e1a-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="55e1a-111">Поставщик OSC должен реализовать метод [ISocialProvider::GetCapabilities,](isocialprovider-getcapabilities.md) который возвращает строку _результата._</span><span class="sxs-lookup"><span data-stu-id="55e1a-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="55e1a-112">OsC вызывает **ISocialProvider::GetCapabilities** для получения сведений о возможностях  поставщика OSC в строке результата, которая соответствует определению схемы XML для элемента **возможностей.**</span><span class="sxs-lookup"><span data-stu-id="55e1a-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="55e1a-113">Эти сведения обеспечивают правильную работу последующих вызовов из OSC к поставщику OSC.</span><span class="sxs-lookup"><span data-stu-id="55e1a-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="55e1a-114">Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **ISocialProvider::GetCapabilities,** необходимо соблюдать XML-схему extensibility поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="55e1a-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="55e1a-115">На следующем рисунке **показана XML-структура** возможностей.</span><span class="sxs-lookup"><span data-stu-id="55e1a-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="55e1a-116">**Рисунок 1. \<capabilities \> Структура XML**</span><span class="sxs-lookup"><span data-stu-id="55e1a-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="55e1a-118">Подробные описания child elements элемента **capabilities** см. в описании [XML-элементов Capabilities.](capabilities-xml-elements.md)</span><span class="sxs-lookup"><span data-stu-id="55e1a-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="55e1a-119">Пример возможностей XML **см. в** [XML-примере](capabilities-xml-example.md)возможностей.</span><span class="sxs-lookup"><span data-stu-id="55e1a-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="55e1a-120">Полное определение XML-схемы поставщика OSC, включая элементы, которые являются обязательными или необязательными, см. в XML-схеме поставщика [Outlook Social Connector.](outlook-social-connector-provider-xml-schema.md)</span><span class="sxs-lookup"><span data-stu-id="55e1a-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="55e1a-121">См. также</span><span class="sxs-lookup"><span data-stu-id="55e1a-121">See also</span></span>

- [<span data-ttu-id="55e1a-122">XML-пример возможностей</span><span class="sxs-lookup"><span data-stu-id="55e1a-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="55e1a-123">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="55e1a-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="55e1a-124">XML для друзей</span><span class="sxs-lookup"><span data-stu-id="55e1a-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="55e1a-125">XML для действий</span><span class="sxs-lookup"><span data-stu-id="55e1a-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="55e1a-126">Разработка поставщика с помощью схемы OSC XML</span><span class="sxs-lookup"><span data-stu-id="55e1a-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

