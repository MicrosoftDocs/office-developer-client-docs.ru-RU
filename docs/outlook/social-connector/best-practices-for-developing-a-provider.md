---
title: Рекомендации по разработке поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: 22e3de8a-c4f2-41a4-a5b1-c5b1bf06f724
description: При разработке поставщика Outlook Social Connector 2013 (OSC) следует следовать приведенным ниже рекомендациям.
ms.openlocfilehash: 6a48a56d8065fb9a176ca6527340c99551cdb52a
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33425920"
---
# <a name="best-practices-for-developing-a-provider"></a><span data-ttu-id="db06b-103">Рекомендации по разработке поставщика</span><span class="sxs-lookup"><span data-stu-id="db06b-103">Best practices for developing a provider</span></span>

<span data-ttu-id="db06b-104">При разработке поставщика Outlook Social Connector 2013 (OSC) следует следовать приведенным ниже рекомендациям.</span><span class="sxs-lookup"><span data-stu-id="db06b-104">You should adhere to the following practices when you develop an Outlook Social Connector 2013 (OSC) provider:</span></span>
  
- <span data-ttu-id="db06b-105">Из соображений безопасности поставщики, которые обмениваются данными с серверами через Интернет, должны использовать протокол HTTPS (протокол передачи гипертекста (HTTP) и протокол SSL (Secure Socket Layer)).</span><span class="sxs-lookup"><span data-stu-id="db06b-105">For security reasons, providers that communicate with servers over the Internet should use the HTTPS (Hypertext Transfer Protocol (HTTP) with Secure Socket Layer (SSL)) protocol.</span></span> <span data-ttu-id="db06b-106">В противном случае существует риск перехвата или передачи электронных адресов, активности социальных сетей и других пользовательских данных во время передачи.</span><span class="sxs-lookup"><span data-stu-id="db06b-106">Otherwise, there is a risk that email addresses, social network activities, and other user data could be intercepted or exposed while in transit.</span></span>
    
- <span data-ttu-id="db06b-107">Если вы разрабатываете поставщик OSC для сторонней социальной сети, ваш поставщик должен соблюдать условия обслуживания в социальных сетях.</span><span class="sxs-lookup"><span data-stu-id="db06b-107">If you are developing an OSC provider for a third-party social network, your provider must adhere to the social network's terms of service.</span></span>
    
- <span data-ttu-id="db06b-108">Чтобы свести к минимуму размер пакета загрузки поставщика, создайте поставщик с помощью собственного компилятора, такого как C++, или любого другого средства, которое может создать COM-компонент.</span><span class="sxs-lookup"><span data-stu-id="db06b-108">To minimize the size of the provider download package, build the provider by using a native compiler such as C++ or any other tool that can build a COM component.</span></span>
    
- <span data-ttu-id="db06b-109">В поставщике Создайте уникальный агент пользователя, который отправляется в социальную сеть для отслеживания звонков, выполненных поставщиком в социальной сети.</span><span class="sxs-lookup"><span data-stu-id="db06b-109">In your provider, create a unique user agent that is sent to the social network to track calls made by the provider to the social network.</span></span>
    
- <span data-ttu-id="db06b-110">Метод [исоЦиалпровидер:: Capabilities](isocialprovider-getcapabilities.md) не должен полагаться на вызов социальных сетей через Интернет, чтобы получить возможности поставщика.</span><span class="sxs-lookup"><span data-stu-id="db06b-110">The [ISocialProvider::GetCapabilities](isocialprovider-getcapabilities.md) method should not rely on calling the social network over the Internet to get the capabilities of the provider.</span></span> <span data-ttu-id="db06b-111">Например, пользователи могут запускать Outlook в автономном режиме; Если с помощью OSC вызываются **функции** и отсутствует сетевое подключение, при **вызове метода capabilities не** возвращается допустимый XML-код **возможности** .</span><span class="sxs-lookup"><span data-stu-id="db06b-111">For example, users can start Outlook offline; if the OSC calls **GetCapabilities** and there is no network connection, the **GetCapabilities** call will not return valid **capabilities** XML.</span></span> <span data-ttu-id="db06b-112">Рекомендуется хранить XML-код **возможностей** в качестве ресурса в поставщике.</span><span class="sxs-lookup"><span data-stu-id="db06b-112">The best practice is to store **capabilities** XML as a resource in your provider.</span></span> 
    
- <span data-ttu-id="db06b-113">Ваш поставщик OSC может создавать значительный объем звонков в социальную сеть.</span><span class="sxs-lookup"><span data-stu-id="db06b-113">Your OSC provider can generate a significant volume of calls to a social network.</span></span> <span data-ttu-id="db06b-114">В зависимости от условий предоставления услуг для социальной сети рассмотрите возможность кэширования друзей в папке Outlook, чтобы уменьшить количество вызовов с OSC до поставщика и, в свою очередь, от поставщика к социальной сети.</span><span class="sxs-lookup"><span data-stu-id="db06b-114">Depending on the terms of service for your social network, consider caching friends to an Outlook folder to reduce the number of calls from the OSC to your provider and, in turn, from your provider to the social network.</span></span>
    
- <span data-ttu-id="db06b-115">Office 2013 доступен как в 32-разрядной, так и в 64-разрядной версиях.</span><span class="sxs-lookup"><span data-stu-id="db06b-115">Office 2013 is available in both 32-bit and 64-bit versions.</span></span> <span data-ttu-id="db06b-116">Версии Office до Office 2010 доступны только в 32 – разрядной версии.</span><span class="sxs-lookup"><span data-stu-id="db06b-116">Versions of Office prior to Office 2010 are available only in a 32-bit version.</span></span> <span data-ttu-id="db06b-117">По умолчанию для установки Office 2013 на 64-разрядной версии Windows устанавливается 32 —-разрядный выпуск.</span><span class="sxs-lookup"><span data-stu-id="db06b-117">The default installation of Office 2013 on 64-bit Windows is 32-bit.</span></span> <span data-ttu-id="db06b-118">Если вы планируете поддерживать 64-разрядную версию файла OSC, установленного с 64-разрядной версией Office 2013, также необходимо выпустить 64-разрядную версию поставщика.</span><span class="sxs-lookup"><span data-stu-id="db06b-118">If you intend to support the 64-bit version of the OSC that is installed with 64-bit Office 2013, you must also release a 64-bit version of your provider.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="db06b-119">См. также</span><span class="sxs-lookup"><span data-stu-id="db06b-119">See also</span></span>

- [<span data-ttu-id="db06b-120">Переosc типичные последовательности вызовов</span><span class="sxs-lookup"><span data-stu-id="db06b-120">OSC Typical Calling Sequences</span></span>](osc-typical-calling-sequences.md)  
- [<span data-ttu-id="db06b-121">Разработка поставщика с помощью XML-схемы OSC</span><span class="sxs-lookup"><span data-stu-id="db06b-121">Developing a Provider with the OSC XML Schema</span></span>](developing-a-provider-with-the-osc-xml-schema.md)  
- [<span data-ttu-id="db06b-122">Развертывание поставщика</span><span class="sxs-lookup"><span data-stu-id="db06b-122">Deploying a Provider</span></span>](deploying-a-provider.md)  
- [<span data-ttu-id="db06b-123">Начало разработки поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="db06b-123">Getting Started with Developing an Outlook Social Connector Provider</span></span>](getting-started-with-developing-an-outlook-social-connector-provider.md)

