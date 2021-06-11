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
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="1830c-103">Поддержка настройки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="1830c-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="1830c-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="1830c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="1830c-105">Чтобы поддерживать конфигурацию службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="1830c-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="1830c-106">Реализация функции точки входа, соответствующей прототипу [MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="1830c-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="1830c-107">Функции точки входа службы сообщений управляют доступом к данным конфигурации и вызваны в следующих обстоятельствах:</span><span class="sxs-lookup"><span data-stu-id="1830c-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="1830c-108">Когда клиент входит в систему для получения сведений для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="1830c-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="1830c-109">Если клиент хочет просмотреть или изменить свойство конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1830c-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="1830c-110">Хотя большинство служб сообщений предоставляют функции точеки входа, как и по необходимости, эти функции не требуются строго.</span><span class="sxs-lookup"><span data-stu-id="1830c-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="1830c-111">Службы сообщений могут предоставлять доступ к данным конфигурации другими способами.</span><span class="sxs-lookup"><span data-stu-id="1830c-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="1830c-112">Однако использование функции точки входа стандартизирует и упрощает процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="1830c-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="1830c-113">MAPI ожидает, что все функции точки входа службы сообщений смогут хранить и извлекать свойства из разделов профилей, связанных с их службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="1830c-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="1830c-114">Эту функцию можно поддерживать интерактивно, программным или интерактивным и программным образом.</span><span class="sxs-lookup"><span data-stu-id="1830c-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="1830c-115">Чтобы поддерживать интерактивную конфигурацию, устройте лист свойств, отображающий свойства, связанные с настройкой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="1830c-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="1830c-116">В качестве параметра можно также предоставить листы свойств для каждого настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="1830c-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="1830c-117">Некоторые службы сообщений ограничивают пользователей просмотром свойств конфигурации только для чтения; другие службы сообщений позволяют пользователям вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="1830c-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="1830c-118">Чтобы поддерживать программную конфигурацию, ваша функция точки входа службы сообщений должна работать без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="1830c-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="1830c-119">Если служба сообщений может быть вызвана мастером профилей, необходимо поддерживать программную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1830c-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="1830c-120">Если служба сообщений не позволяет настраивать себя с помощью мастера профилей, вы можете выбрать, следует ли поддерживать программную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="1830c-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="1830c-121">Дополнительные сведения о поддержке конфигурации в функции точки входа службы сообщений см. в [сообщении MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="1830c-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="1830c-122">Опубликуйте имя функции точки входа службы сообщений в файле конфигурации Mapisvc.inf, включив следующую запись в раздел служба сообщений:</span><span class="sxs-lookup"><span data-stu-id="1830c-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="1830c-123">Создайте один или несколько диалоговых ящиков листа свойств для отображения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="1830c-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="1830c-124">Выполните следующие задачи, если вы хотите разрешить мастеру профилей настроить службу сообщений:</span><span class="sxs-lookup"><span data-stu-id="1830c-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="1830c-125">Реализация функции точки входа, соответствующей [прототипу WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="1830c-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="1830c-126">Реализуйте стандартную процедуру Windows диалоговом окне, которая соответствует прототипу [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="1830c-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="1830c-127">Расширение функции точки входа службы сообщений для реагирования на дополнительные события.</span><span class="sxs-lookup"><span data-stu-id="1830c-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="1830c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="1830c-128">See also</span></span>

- [<span data-ttu-id="1830c-129">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="1830c-129">Message Service Implementation</span></span>](message-service-implementation.md)

