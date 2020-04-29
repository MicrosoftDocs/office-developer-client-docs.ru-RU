---
title: Поддержка настройки службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: aa1a433e90eda24f1199783bc604e047deb03ecd
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418997"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="29a91-103">Поддержка настройки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="29a91-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="29a91-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="29a91-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="29a91-105">Для поддержки конфигурации службы сообщений используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="29a91-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="29a91-106">Реализуйте функцию точки входа, которая соответствует прототипу [мсгсервицеентри](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="29a91-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="29a91-107">Функции точки входа службы сообщений управляют доступом к данным конфигурации и вызываются в следующих обстоятельствах:</span><span class="sxs-lookup"><span data-stu-id="29a91-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="29a91-108">Когда клиент входит в систему для получения сведений о настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="29a91-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="29a91-109">Когда клиент хочет просмотреть или изменить свойство конфигурации.</span><span class="sxs-lookup"><span data-stu-id="29a91-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="29a91-110">Несмотря на то, что большинство служб сообщений предоставляют точки входа, они, как правило, не являются строго обязательными.</span><span class="sxs-lookup"><span data-stu-id="29a91-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="29a91-111">Службы сообщений могут предоставлять доступ к данным конфигурации другими способами.</span><span class="sxs-lookup"><span data-stu-id="29a91-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="29a91-112">Однако использование функции точки входа стандартизации и упрощает процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="29a91-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="29a91-113">MAPI ожидает, что все функции точки входа службы сообщений будут иметь возможность сохранять и извлекать свойства из разделов профиля, связанных со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="29a91-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="29a91-114">Вы можете поддерживать эту функцию в интерактивном режиме, программно или в интерактивном режиме, и программным способом.</span><span class="sxs-lookup"><span data-stu-id="29a91-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="29a91-115">Для поддержки интерактивной конфигурации предоставьте страницу свойств, в которой отображаются свойства, используемые при настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="29a91-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="29a91-116">В качестве параметра можно также указать страницы свойств для каждого настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="29a91-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="29a91-117">Некоторые службы сообщений ограничивают пользователям представление свойств конфигурации, доступное только для чтения; другие службы сообщений позволяют пользователям вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="29a91-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="29a91-118">Для поддержки программной конфигурации функция точки входа службы сообщений должна иметь возможность работать без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="29a91-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="29a91-119">Если служба сообщений может вызываться мастером профилей, необходимо поддерживать программную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="29a91-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="29a91-120">Если служба сообщений не позволяет настраивать конфигурацию с помощью мастера профилей, вы можете выбрать, следует ли поддерживать программную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="29a91-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="29a91-121">Дополнительные сведения о поддержке конфигурации в функции точки входа службы сообщений можно найти в разделе [мсгсервицеентри](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="29a91-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="29a91-122">Опубликуйте имя функции точки входа службы сообщений в файле конфигурации Mapisvc. INF, включив следующую запись в раздел Служба сообщений:</span><span class="sxs-lookup"><span data-stu-id="29a91-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="29a91-123">Создайте одно или несколько диалоговых окон страницы свойств для отображения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="29a91-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="29a91-124">Если вы хотите разрешить мастеру профилей настраивать службу сообщений, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="29a91-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="29a91-125">Реализуйте функцию точки входа, которая соответствует прототипу [визардентри](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="29a91-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="29a91-126">Реализуйте стандартную процедуру диалогового окна Windows, которая соответствует прототипу [сервицевизарддлгпрок](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="29a91-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="29a91-127">Улучшите функцию точки входа службы сообщений, чтобы реагировать на дополнительные события.</span><span class="sxs-lookup"><span data-stu-id="29a91-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="29a91-128">См. также</span><span class="sxs-lookup"><span data-stu-id="29a91-128">See also</span></span>

- [<span data-ttu-id="29a91-129">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="29a91-129">Message Service Implementation</span></span>](message-service-implementation.md)

