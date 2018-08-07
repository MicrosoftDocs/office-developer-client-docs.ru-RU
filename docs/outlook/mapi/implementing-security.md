---
title: Реализация системы безопасности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 62db34a0-887c-4607-94ad-d8cae68b35c2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f09d96fd8b35df6cafa81b3830642cf6d67806e7
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19809330"
---
# <a name="implementing-security"></a><span data-ttu-id="87b5e-103">Реализация системы безопасности</span><span class="sxs-lookup"><span data-stu-id="87b5e-103">Implementing Security</span></span>

  
  
<span data-ttu-id="87b5e-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="87b5e-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="87b5e-105">Если это требуется системы обмена сообщениями, поставщика транспорта несет ответственность за внедрение необходимый уровень безопасности для доступа к системе обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="87b5e-105">If the messaging system requires it, the transport provider is responsible for implementing an appropriate level of security for access to the messaging system.</span></span> <span data-ttu-id="87b5e-106">Каждый входящих или исходящих сообщений, отправленных диспетчер очереди MAPI через поставщика транспорта обрабатывается в контексте сеанса входа в систему поставщика.</span><span class="sxs-lookup"><span data-stu-id="87b5e-106">Each incoming or outgoing message sent through a transport provider by the MAPI spooler is handled in the context of a provider logon session.</span></span> <span data-ttu-id="87b5e-107">Поставщика транспорта можно отобразить диалоговое окно входа в систему для пользователя, который запрашивает учетные данные пользователя до установления такое подключение.</span><span class="sxs-lookup"><span data-stu-id="87b5e-107">The transport provider can display a logon dialog box to the user that prompts for a user's credentials before establishing such a connection.</span></span> <span data-ttu-id="87b5e-108">Кроме того поставщика транспорта можно хранить ранее введенных учетных данных пользователя в диапазоне безопасной свойства в разделе профилей и использовать их для доступа без запроса.</span><span class="sxs-lookup"><span data-stu-id="87b5e-108">Alternatively, the transport provider can store the user's previously entered credentials in the secure property range within a profile section and use them for access without prompting.</span></span>
  
<span data-ttu-id="87b5e-109">При реализации поставщика транспорта безопасности, необходимо учитывайте следующее:</span><span class="sxs-lookup"><span data-stu-id="87b5e-109">When implementing your transport provider's security, consider the following:</span></span>
  
- <span data-ttu-id="87b5e-110">С несколькими поставщиками установленной службы может существовать множество имена и пароли, связанный с пользователем.</span><span class="sxs-lookup"><span data-stu-id="87b5e-110">With multiple installed service providers, there can be a multitude of names and passwords associated with a user.</span></span>
    
- <span data-ttu-id="87b5e-111">MAPI позволяет нескольких сеансов с несколькими удостоверениями.</span><span class="sxs-lookup"><span data-stu-id="87b5e-111">MAPI allows multiple sessions with multiple identities.</span></span> <span data-ttu-id="87b5e-112">Поставщики, рекомендуется для поддержки нескольких сеансов, но это не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="87b5e-112">Providers are encouraged to support multiple sessions but are not required to do so.</span></span>
    
- <span data-ttu-id="87b5e-113">Каждого сеанса с помощью поставщика транспорта связана с MAPI точечные раздел в профиль пользователя.</span><span class="sxs-lookup"><span data-stu-id="87b5e-113">Each session with a transport provider is associated by MAPI with a discrete section in the user's profile.</span></span> <span data-ttu-id="87b5e-114">Поставщика транспорта можно использовать метод [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) для получения доступа к этому разделу, которую можно использовать для хранения какие-либо сведения, связанные с этой сеанса, включая учетные данные.</span><span class="sxs-lookup"><span data-stu-id="87b5e-114">The transport provider can use the [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) method to gain access to this section, which can be used to store any information associated with this session, including credentials.</span></span> 
    
- <span data-ttu-id="87b5e-115">С несколькими поставщиками установленных транспорта не обязательно содержит значение true, пользователь имеет только отдельный адрес электронной почты.</span><span class="sxs-lookup"><span data-stu-id="87b5e-115">With multiple installed transport providers, it is not necessarily true that the user only has a single email address.</span></span> <span data-ttu-id="87b5e-116">Пользователь может иметь отдельный адрес для каждого поставщика установленных транспорта или могут иметь разные адреса для каждого сеанса на одного поставщика.</span><span class="sxs-lookup"><span data-stu-id="87b5e-116">A user can have a separate email address for each installed transport provider or can have a different address for each session on a single provider.</span></span>
    
<span data-ttu-id="87b5e-117">Дополнительные сведения о хранении учетных данных в разделах профилей в разделе [службы сообщений и профили](message-services-and-profiles.md) и [IProfSect: IMAPIProp](iprofsectimapiprop.md).</span><span class="sxs-lookup"><span data-stu-id="87b5e-117">For more information about storing credentials in profile sections, see [Message Services and Profiles](message-services-and-profiles.md) and [IProfSect : IMAPIProp](iprofsectimapiprop.md).</span></span>
  

