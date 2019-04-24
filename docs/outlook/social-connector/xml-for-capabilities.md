---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в схеме XML поставщика (OSC) позволяет поставщику OSC указать его функциональность. К таким функциям относятся следующие:'
ms.openlocfilehash: ff6abbd4d99eb542a11e3d64a2015fc0585fca79
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356449"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="22a06-104">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="22a06-104">XML for capabilities</span></span>

<span data-ttu-id="22a06-105">Элемент **capabilities** в схеме XML поставщика (OSC) позволяет поставщику OSC указать его функциональность.</span><span class="sxs-lookup"><span data-stu-id="22a06-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="22a06-106">К таким функциям относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="22a06-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="22a06-107">Поддерживает ли поставщик возможность получения, кэширования или динамического поиска друзей и действий из социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="22a06-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="22a06-108">Как OSC должен отображать определенные пользовательские интерфейсы входа в систему.</span><span class="sxs-lookup"><span data-stu-id="22a06-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="22a06-109">Должен ли OSC использовать проверку подлинности на основе форм или автоматически настраивать социальные сети и выполнять вход в систему пользователя в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="22a06-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="22a06-110">Схема XML для **возможностей** очень важна, так как она указывает на OSC функции, поддерживаемые поставщиком.</span><span class="sxs-lookup"><span data-stu-id="22a06-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="22a06-111">Поставщик OSC должен реализовать метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) , который возвращает строку _результата_ .</span><span class="sxs-lookup"><span data-stu-id="22a06-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="22a06-112">OSC вызывает метод **исоЦиалпровидер::-Capabilities** для получения сведений о возможностях поставщика OSC в результирующей __ строке, которая соответствует определению схемы XML для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="22a06-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="22a06-113">Эта информация позволяет последующим вызовам из OSC в поставщик OSC работать правильно.</span><span class="sxs-lookup"><span data-stu-id="22a06-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="22a06-114">Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **исоЦиалпровидер::-Capabilities** , необходимо соответствовать схеме расширяемости поставщика OSC XML.</span><span class="sxs-lookup"><span data-stu-id="22a06-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="22a06-115">На следующем рисунке показана структура XML **возможностей** .</span><span class="sxs-lookup"><span data-stu-id="22a06-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="22a06-116">**Рис. 1. \<структура\> XML возможностей**</span><span class="sxs-lookup"><span data-stu-id="22a06-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="22a06-118">Подробное описание дочерних элементов элемента **capabilities** представлено в статье [Elements XML Elements](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="22a06-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="22a06-119">Пример XML-кода **возможностей** представлен в статье [пример возможностей XML](capabilities-xml-example.md).</span><span class="sxs-lookup"><span data-stu-id="22a06-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="22a06-120">Полное определение XML-схемы поставщика OSC, в том числе элементов, обязательных или необязательных, можно найти в статье [схема XML поставщика социальных соединителЕй Outlook](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="22a06-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="22a06-121">См. также</span><span class="sxs-lookup"><span data-stu-id="22a06-121">See also</span></span>

- [<span data-ttu-id="22a06-122">Пример XML-кода возможностей</span><span class="sxs-lookup"><span data-stu-id="22a06-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="22a06-123">Синхронизация друзей и действий</span><span class="sxs-lookup"><span data-stu-id="22a06-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="22a06-124">XML для друзей</span><span class="sxs-lookup"><span data-stu-id="22a06-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="22a06-125">XML для действий</span><span class="sxs-lookup"><span data-stu-id="22a06-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="22a06-126">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="22a06-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

