---
title: Реализация безопасности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c430160ee508a86f36d840c7916c0516cfc10fbd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33417289"
---
# <a name="implementing-security"></a><span data-ttu-id="c26fa-103">Реализация безопасности</span><span class="sxs-lookup"><span data-stu-id="c26fa-103">Implementing Security</span></span>

  
  
<span data-ttu-id="c26fa-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c26fa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c26fa-105">Если это требуется для системы обмена сообщениями, поставщик транспорта несет ответственность за реализацию соответствующего уровня безопасности для доступа к системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="c26fa-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="c26fa-106">Каждое входящее или исходящее сообщение, отправляемое через поставщик транспорта с помощью диспетчера очереди MAPI, обрабатывается в контексте сеанса входа поставщика.</span><span class="sxs-lookup"><span data-stu-id="c26fa-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="c26fa-107">Поставщик транспорта может отобразить диалоговое окно входа в систему для пользователя, который запрашивает учетные данные пользователя, прежде чем устанавливать такое подключение.</span><span class="sxs-lookup"><span data-stu-id="c26fa-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="c26fa-108">Кроме того, поставщик транспорта может хранить введенные ранее учетные данные пользователя в диапазоне свойств безопасности в разделе профиля и использовать их для доступа без запросов.</span><span class="sxs-lookup"><span data-stu-id="c26fa-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="c26fa-109">При реализации безопасности поставщика транспорта учитывайте следующие возможности.</span><span class="sxs-lookup"><span data-stu-id="c26fa-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="c26fa-110">С несколькими установленными поставщиками услуг может быть множество имен и паролей, связанных с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c26fa-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="c26fa-111">MAPI разрешает несколько сеансов с несколькими удостоверениями.</span><span class="sxs-lookup"><span data-stu-id="c26fa-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="c26fa-112">Поставщики должны поддерживать несколько сеансов, но это необязательно.</span><span class="sxs-lookup"><span data-stu-id="c26fa-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="c26fa-113">Каждый сеанс с поставщиком транспорта связан MAPI с дискретным разделом в профиле пользователя.</span><span class="sxs-lookup"><span data-stu-id="c26fa-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="c26fa-114">Поставщик транспорта может использовать метод [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) для получения доступа к этому разделу, который можно использовать для хранения любых сведений, связанных с этим сеансом, в том числе учетных данных.</span><span class="sxs-lookup"><span data-stu-id="c26fa-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="c26fa-115">Если у вас есть несколько установленных поставщиков транспорта, это не обязательно означает, что у пользователя есть только один адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="c26fa-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="c26fa-116">У пользователя может быть отдельный адрес электронной почты для каждого установленного поставщика транспорта или другой адрес для каждого сеанса на одном поставщике.</span><span class="sxs-lookup"><span data-stu-id="c26fa-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="c26fa-117">Для получения дополнительных сведений о хранении учетных данных в разделах профилей, ознакомьтесь со статьей [службы и профили сообщений](message-services-and-profiles.md) и [ипрофсект: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="c26fa-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

