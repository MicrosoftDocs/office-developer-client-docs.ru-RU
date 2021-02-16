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
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="c7c71-103">Поддержка настройки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="c7c71-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="c7c71-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7c71-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7c71-105">Для поддержки конфигурации службы сообщений используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="c7c71-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="c7c71-106">Реализуют функцию точки входа, которая соответствует [прототипу MSGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="c7c71-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="c7c71-107">Функции точки входа службы сообщений управляют доступом к данным конфигурации и вызваны в следующих случаях:</span><span class="sxs-lookup"><span data-stu-id="c7c71-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="c7c71-108">Когда клиент входит в систему, чтобы получить сведения для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c7c71-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="c7c71-109">Когда клиент хочет просмотреть или изменить свойство конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c7c71-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="c7c71-110">Хотя большинство служб сообщений предоставляют функции точки входа, они не являются строгой обязательной.</span><span class="sxs-lookup"><span data-stu-id="c7c71-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="c7c71-111">Службы сообщений могут предоставлять доступ к данным конфигурации другими способами.</span><span class="sxs-lookup"><span data-stu-id="c7c71-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="c7c71-112">Однако использование функции точки входа стандартизирует и упрощает процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="c7c71-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="c7c71-113">MAPI ожидает, что все функции точки входа службы сообщений смогут хранить и извлекать свойства из разделов профиля, связанных со службой сообщений.</span><span class="sxs-lookup"><span data-stu-id="c7c71-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="c7c71-114">Вы можете поддерживать эту функцию в интерактивном, программных или как интерактивном, так и в программных рамках.</span><span class="sxs-lookup"><span data-stu-id="c7c71-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="c7c71-115">Для поддержки интерактивной конфигурации необходимо предоставить лист свойств, отображающий свойства, участвующие в настройке службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c7c71-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="c7c71-116">В качестве варианта можно также предоставить листы свойств для каждого настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="c7c71-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="c7c71-117">Некоторые службы сообщений ограничивают пользователей представлением свойств конфигурации только для чтения; другие службы сообщений позволяют пользователям вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="c7c71-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="c7c71-118">Для поддержки программной конфигурации функция точки входа службы сообщений должна работать без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7c71-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="c7c71-119">Если служба сообщений может быть вызвана мастером профилей, необходимо поддерживать программную настройку.</span><span class="sxs-lookup"><span data-stu-id="c7c71-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="c7c71-120">Если служба сообщений не позволяет настраивать себя с помощью мастера профилей, можно выбрать, следует ли поддерживать программную конфигурацию.</span><span class="sxs-lookup"><span data-stu-id="c7c71-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="c7c71-121">Дополнительные сведения о поддержке конфигурации в функции точки входа службы сообщений см. в [msGSERVICEENTRY.](msgserviceentry.md)</span><span class="sxs-lookup"><span data-stu-id="c7c71-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="c7c71-122">Опубликуйте имя функции точки входа службы сообщений в файле конфигурации Mapisvc.inf, включив следующую запись в раздел службы сообщений:</span><span class="sxs-lookup"><span data-stu-id="c7c71-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="c7c71-123">Создайте одно или несколько диалоговых окно листа свойств для отображения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="c7c71-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="c7c71-124">Чтобы разрешить мастеру профилей настраивать службу сообщений, выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="c7c71-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="c7c71-125">Реализуют функцию точки входа, которая соответствует [прототипу WIZARDENTRY.](wizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="c7c71-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="c7c71-126">Реализуйте стандартную процедуру диалоговых окон Windows, которая соответствует прототипу [SERVICEWIZARDDLGPROC.](servicewizarddlgproc.md)</span><span class="sxs-lookup"><span data-stu-id="c7c71-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="c7c71-127">Улучшайте функцию точки входа службы сообщений для реагирования на дополнительные события.</span><span class="sxs-lookup"><span data-stu-id="c7c71-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c7c71-128">См. также</span><span class="sxs-lookup"><span data-stu-id="c7c71-128">See also</span></span>

- [<span data-ttu-id="c7c71-129">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="c7c71-129">Message Service Implementation</span></span>](message-service-implementation.md)

