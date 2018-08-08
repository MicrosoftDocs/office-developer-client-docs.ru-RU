---
title: Рекомендации по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: 'При разработке поставщика Outlook Social Connector 2013 (OSC) следует придерживаться следующих правил:'
ms.openlocfilehash: a6ee9d54f33bbc855d178aba844a8f65ec92f964
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812704"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="f97e2-103">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="f97e2-103">Best practices for developing a provider</span></span>

<span data-ttu-id="f97e2-104">При разработке поставщика Outlook Social Connector 2013 (OSC) следует придерживаться следующих правил:</span><span class="sxs-lookup"><span data-stu-id="f97e2-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="f97e2-105">По соображениям безопасности поставщиков, которые взаимодействуют с серверами через Интернет следует использовать протокол HTTPS (протокол HTTP (Hypertext Transfer) с помощью Secure сокетов протокол SSL).</span><span class="sxs-lookup"><span data-stu-id="f97e2-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="f97e2-106">В противном случае есть риск, адреса электронной почты, действия социальной сети и других пользователей, могут быть перехвачены или предоставляемые в процессе передачи данных.</span><span class="sxs-lookup"><span data-stu-id="f97e2-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="f97e2-107">При создании поставщика OSC для социальных сетей стороннего поставщика, должна придерживаться социальной сети условия использования службы.</span><span class="sxs-lookup"><span data-stu-id="f97e2-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="f97e2-108">Чтобы уменьшить размер пакета загрузки поставщика, построение поставщика с использованием собственного компилятора C++ или других средств, можно создать компонент COM.</span><span class="sxs-lookup"><span data-stu-id="f97e2-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="f97e2-109">В ваш поставщик создайте агент уникальных пользователей, которое отправляется в социальной сети для отслеживания вызовов, сделанных поставщиком для социальных сетей.</span><span class="sxs-lookup"><span data-stu-id="f97e2-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="f97e2-110">Метод [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) не следует полагаться на вызов социальных сетей в Интернете для получения возможностей поставщика.</span><span class="sxs-lookup"><span data-stu-id="f97e2-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="f97e2-111">Например пользователи могут запустить Outlook в автономном режиме; Если OSC вызывает **GetCapabilities** и нет сетевого подключения, **GetCapabilities** вызов не будет возвращен допустимый **возможности** XML.</span><span class="sxs-lookup"><span data-stu-id="f97e2-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="f97e2-112">Рекомендуется хранить **возможности** XML в качестве ресурса в поставщике.</span><span class="sxs-lookup"><span data-stu-id="f97e2-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="f97e2-113">У поставщика OSC можно создать значительного объема звонков в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="f97e2-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="f97e2-114">В зависимости от условия использования службы для социальных сетей рассмотрите возможность кэширования друзья папки Outlook сократить количество вызовов из OSC к поставщику и, в свою очередь, у поставщика в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="f97e2-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="f97e2-115">Office 2013 доступна в 32-разрядной и 64-разрядных версиях.</span><span class="sxs-lookup"><span data-stu-id="f97e2-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="f97e2-116">Версии Office до Office 2010, доступны только в 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="f97e2-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="f97e2-117">По умолчанию при установке Office 2013 на 64-разрядной ОС Windows — 32-разрядная версия.</span><span class="sxs-lookup"><span data-stu-id="f97e2-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="f97e2-118">Если планируется поддерживать 64-разрядная версия OSC, который устанавливается вместе с 64-разрядная версия Office 2013, необходимо также освободить 64-разрядная версия поставщика.</span><span class="sxs-lookup"><span data-stu-id="f97e2-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="f97e2-119">См. также</span><span class="sxs-lookup"><span data-stu-id="f97e2-119">See also</span></span>

- [<span data-ttu-id="f97e2-120">Типичные последовательности вызовов OSC</span><span class="sxs-lookup"><span data-stu-id="f97e2-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="f97e2-121">Разработка поставщика с использованием схемы XML для OSC</span><span class="sxs-lookup"><span data-stu-id="f97e2-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="f97e2-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="f97e2-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="f97e2-123">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="f97e2-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

