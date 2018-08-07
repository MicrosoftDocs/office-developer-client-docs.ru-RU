---
title: XML для возможностей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: edad1223-a55f-4e4a-8e90-3471f2f559ac
description: 'Элемент capabilities в XML-схеме поставщика (OSC) позволяет поставщика OSC указать его функциональные возможности. Такая функциональная возможность включает в себя следующее:'
ms.openlocfilehash: 8192c4d559ae656cfc3b12cd8f50f7d4acd5ed5f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812838"
---
# <a name="xml-for-capabilities"></a><span data-ttu-id="a89a2-104">XML для возможностей</span><span class="sxs-lookup"><span data-stu-id="a89a2-104">XML for capabilities</span></span>

<span data-ttu-id="a89a2-105">Элемент **capabilities** в XML-схеме поставщика (OSC) позволяет поставщика OSC указать его функциональные возможности.</span><span class="sxs-lookup"><span data-stu-id="a89a2-105">The **capabilities** element in the (OSC) provider XML schema allows an OSC provider to specify its functionality.</span></span> <span data-ttu-id="a89a2-106">Такая функциональная возможность включает в себя следующее:</span><span class="sxs-lookup"><span data-stu-id="a89a2-106">Such functionality includes the following:</span></span> 
  
- <span data-ttu-id="a89a2-107">Поддерживает ли поставщик начало, кэширование или динамически поиск друзей и действия из социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="a89a2-107">Whether the provider supports getting, caching, or dynamically looking up friends and activities from the social network.</span></span>
    
- <span data-ttu-id="a89a2-108">OSC отображение определенных пользовательских интерфейсов входа в систему.</span><span class="sxs-lookup"><span data-stu-id="a89a2-108">How the OSC should display certain logon user interfaces.</span></span>
    
- <span data-ttu-id="a89a2-109">Ли OSC следует использовать проверку подлинности на основе форм или автоматической настройки социальной сети и журналы на пользователя в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="a89a2-109">Whether the OSC should use forms-based authentication or automatically configure the social network and logs on the user on the social network.</span></span>
    
<span data-ttu-id="a89a2-110">XML-схемы для **возможности** крайне важна, так как он определяет для OSC функциональных возможностей, поддерживаемых поставщиком.</span><span class="sxs-lookup"><span data-stu-id="a89a2-110">The XML schema for **capabilities** is critical because it identifies to the OSC the functionality supported by the provider.</span></span> <span data-ttu-id="a89a2-111">Поставщика OSC необходимо реализовать метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) , который возвращает _результирующую_ строку.</span><span class="sxs-lookup"><span data-stu-id="a89a2-111">An OSC provider must implement the [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method that returns a  _result_ string.</span></span> <span data-ttu-id="a89a2-112">OSC вызывает **ISocialProvider::GetCapabilities** для получения сведений о возможностях поставщика OSC в _результирующую_ строку, которой соответствует определение схемы XML для элемента **capabilities** .</span><span class="sxs-lookup"><span data-stu-id="a89a2-112">The OSC calls **ISocialProvider::GetCapabilities** to obtain information about the capabilities of the OSC provider in the  _result_ string, which complies with the XML schema definition for the **capabilities** element.</span></span> <span data-ttu-id="a89a2-113">Эта информация включает последующие вызовы из OSC поставщика OSC для правильной работы.</span><span class="sxs-lookup"><span data-stu-id="a89a2-113">This information enables subsequent calls from the OSC to the OSC provider to operate correctly.</span></span> 
  
<span data-ttu-id="a89a2-114">Чтобы указать возможности поставщика OSC в качестве выходного параметра метода **ISocialProvider::GetCapabilities** , должен соответствовать типу схемы XML возможности расширения поставщика OSC.</span><span class="sxs-lookup"><span data-stu-id="a89a2-114">To specify capabilities of an OSC provider as an output parameter of the **ISocialProvider::GetCapabilities** method, you must conform to the OSC provider extensibility XML schema.</span></span> <span data-ttu-id="a89a2-115">На следующем рисунке показана XML-структура **возможностей** .</span><span class="sxs-lookup"><span data-stu-id="a89a2-115">The following figure shows the **capabilities** XML structure.</span></span> 
  
<span data-ttu-id="a89a2-116">**На рисунке 1. \<возможности\> XML-структура**</span><span class="sxs-lookup"><span data-stu-id="a89a2-116">**Figure 1. \<capabilities\> XML structure**</span></span>

![XML-структура возможностей](media/ol14oscref_Specifyingxmlforcapabilities_image1.gif)
  
<span data-ttu-id="a89a2-118">Подробное описание дочерние элементы элемента **capabilities** в разделе [Возможности XML-элементы](capabilities-xml-elements.md).</span><span class="sxs-lookup"><span data-stu-id="a89a2-118">For detailed descriptions of child elements of the **capabilities** element, see [Capabilities XML Elements](capabilities-xml-elements.md).</span></span> <span data-ttu-id="a89a2-119">[Пример XML возможности](capabilities-xml-example.md) **возможности** XML, см.</span><span class="sxs-lookup"><span data-stu-id="a89a2-119">For an example of **capabilities** XML, see [Capabilities XML Example](capabilities-xml-example.md).</span></span> <span data-ttu-id="a89a2-120">Полное определение схемы XML поставщика OSC, включая, какие элементы являются обязательный или необязательный см в [Outlook Social Connector поставщика XML-схему](outlook-social-connector-provider-xml-schema.md).</span><span class="sxs-lookup"><span data-stu-id="a89a2-120">For a complete definition of the OSC provider XML schema, including which elements are required or optional, see [Outlook Social Connector Provider XML Schema](outlook-social-connector-provider-xml-schema.md).</span></span>
  
## <a name="see-also"></a><span data-ttu-id="a89a2-121">См. также</span><span class="sxs-lookup"><span data-stu-id="a89a2-121">See also</span></span>

- [<span data-ttu-id="a89a2-122">Пример возможности XML</span><span class="sxs-lookup"><span data-stu-id="a89a2-122">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="a89a2-123">Синхронизация друзей и действия</span><span class="sxs-lookup"><span data-stu-id="a89a2-123">Synchronizing Friends and Activities</span></span>](synchronizing-friends-and-activities.md)  
- [<span data-ttu-id="a89a2-124">XML-код для друзей</span><span class="sxs-lookup"><span data-stu-id="a89a2-124">XML for Friends</span></span>](xml-for-friends.md)  
- [<span data-ttu-id="a89a2-125">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="a89a2-125">XML for Activities</span></span>](xml-for-activities.md)
- [<span data-ttu-id="a89a2-126">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="a89a2-126">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)

