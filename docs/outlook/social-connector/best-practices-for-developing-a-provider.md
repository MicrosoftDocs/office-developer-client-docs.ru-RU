---
title: Рекомендации по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'Следует придерживаться следующих методов при разработке поставщика Outlook Social Connector 2013 (OSC):'
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425920"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="b6357-103">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="b6357-103">Best practices for developing a provider</span></span>

<span data-ttu-id="b6357-104">Следует придерживаться следующих методов при разработке поставщика Outlook Social Connector 2013 (OSC):</span><span class="sxs-lookup"><span data-stu-id="b6357-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="b6357-105">В целях безопасности поставщикам, которые взаимодействуют с серверами через Интернет, следует использовать протокол HTTPS (Протокол передачи гипертекстов (HTTP) с протоколом Secure Socket Layer (SSL)).</span><span class="sxs-lookup"><span data-stu-id="b6357-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="b6357-106">В противном случае существует риск того, что адреса электронной почты, действия социальных сетей и другие данные пользователей могут быть перехвачены или выставлены во время транзита.</span><span class="sxs-lookup"><span data-stu-id="b6357-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="b6357-107">Если вы разрабатываете поставщика OSC для сторонних социальных сетей, ваш поставщик должен придерживаться условий службы социальной сети.</span><span class="sxs-lookup"><span data-stu-id="b6357-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="b6357-108">Чтобы свести к минимуму размер пакета загрузки поставщика, создайте поставщика с помощью родного компиляторов, таких как C++ или любого другого средства, который может создать компонент COM.</span><span class="sxs-lookup"><span data-stu-id="b6357-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="b6357-109">В своем поставщике создайте уникальный агент пользователя, который отправляется в социальную сеть для отслеживания звонков, сделанных поставщиком в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b6357-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="b6357-110">Метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) не должен полагаться на вызов социальной сети через Интернет, чтобы получить возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="b6357-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="b6357-111">Например, пользователи могут запускать Outlook в автономном режиме; если osC вызывает **GetCapabilities** и нет сетевого подключения, вызов **GetCapabilities** не возвращает допустимые **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="b6357-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="b6357-112">Лучше всего хранить возможности **XML** в качестве ресурса в поставщике.</span><span class="sxs-lookup"><span data-stu-id="b6357-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="b6357-113">Поставщик osc может генерировать значительный объем звонков в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b6357-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="b6357-114">В зависимости от условий службы для вашей социальной сети рассмотрите возможность кэшинга друзей в папку Outlook, чтобы уменьшить количество вызовов из OSC к поставщику и, в свою очередь, от поставщика в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="b6357-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="b6357-115">Office 2013 доступен в 32-битных и 64-битных версиях.</span><span class="sxs-lookup"><span data-stu-id="b6357-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="b6357-116">Версии Office до Office 2010 года доступны только в 32-битной версии.</span><span class="sxs-lookup"><span data-stu-id="b6357-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="b6357-117">По умолчанию установка Office 2013 г. на 64-Windows 32-битная.</span><span class="sxs-lookup"><span data-stu-id="b6357-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="b6357-118">Если вы собираетесь поддерживать 64-битную версию OSC, установленную с 64-битной Office 2013 г., необходимо также выпустить 64-битную версию поставщика.</span><span class="sxs-lookup"><span data-stu-id="b6357-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="b6357-119">См. также</span><span class="sxs-lookup"><span data-stu-id="b6357-119">See also</span></span>

- [<span data-ttu-id="b6357-120">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="b6357-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="b6357-121">Разработка поставщика с помощью схемы XML OSC</span><span class="sxs-lookup"><span data-stu-id="b6357-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="b6357-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="b6357-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="b6357-123">Начало работы с разработкой Outlook поставщика социальных соединители</span><span class="sxs-lookup"><span data-stu-id="b6357-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

