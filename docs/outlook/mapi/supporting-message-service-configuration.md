---
title: Поддержка конфигурации службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: bb6ab537-2876-474b-be7a-84734ace2bae
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e1782f3c20c1741e0e4b1859f1b29d835444009c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812407"
---
# <a name="supporting-message-service-configuration"></a><span data-ttu-id="fee9c-103">Поддержка конфигурации службы сообщений</span><span class="sxs-lookup"><span data-stu-id="fee9c-103">Supporting message service configuration</span></span>
  
<span data-ttu-id="fee9c-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="fee9c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="fee9c-105">Чтобы обеспечить поддержку конфигурации службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="fee9c-105">To support message service configuration, use the following procedure:</span></span>
  
1. <span data-ttu-id="fee9c-106">Реализуйте функцию точки входа, соответствующие прототип [MSGSERVICEENTRY](msgserviceentry.md) .</span><span class="sxs-lookup"><span data-stu-id="fee9c-106">Implement an entry point function that conforms to the [MSGSERVICEENTRY](msgserviceentry.md) prototype.</span></span> <span data-ttu-id="fee9c-107">Сообщение службы запись точки функции управления доступом к данным конфигурации и вызывается при следующих обстоятельствах:</span><span class="sxs-lookup"><span data-stu-id="fee9c-107">Message service entry point functions manage access to configuration data and are called in the following circumstances:</span></span> 
    
   - <span data-ttu-id="fee9c-108">При входе клиента нужно извлечь данные для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="fee9c-108">When a client logs on to retrieve information to configure your message service.</span></span>
    
   - <span data-ttu-id="fee9c-109">Когда клиенту требуется просмотреть или изменить свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fee9c-109">When a client wants to view or change a configuration property.</span></span> 
    
   <span data-ttu-id="fee9c-110">Хотя большинство служб сообщение будет предоставлять функции точки входа, как это и должно, эти функции не обязательно.</span><span class="sxs-lookup"><span data-stu-id="fee9c-110">Although most message services will provide entry point functions, as they should, these functions are not strictly required.</span></span> <span data-ttu-id="fee9c-111">Службы сообщений можно предоставить доступ к данным конфигурации по-другому.</span><span class="sxs-lookup"><span data-stu-id="fee9c-111">Message services can provide access to configuration data in other ways.</span></span> <span data-ttu-id="fee9c-112">Тем не менее используя функцию стандартизированы и упрощает процесс настройки.</span><span class="sxs-lookup"><span data-stu-id="fee9c-112">However, using an entry point function standardizes and simplifies the process of configuration.</span></span>
    
   <span data-ttu-id="fee9c-113">MAPI ожидает, что все функции сообщения службы запись точки должны иметь возможность хранения и извлечения свойств из раздела профилей, связанных с их службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="fee9c-113">MAPI expects all message service entry point functions to be able to store and retrieve properties from the profile sections that are associated with their message service.</span></span> <span data-ttu-id="fee9c-114">Сможет поддерживать эту функцию интерактивно, программным способом, или оба интерактивно и программными средствами.</span><span class="sxs-lookup"><span data-stu-id="fee9c-114">You can support this functionality interactively, programmatically, or both interactively and programmatically.</span></span>
    
   <span data-ttu-id="fee9c-115">Для поддержки интерактивных конфигурации, предоставляют свойств, которая отображает свойства, необходимые для настройки службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="fee9c-115">To support interactive configuration, provide a property sheet that displays the properties involved in configuring your message service.</span></span> <span data-ttu-id="fee9c-116">Как вариант можно также предоставить свойств для каждого настраиваемого поставщика.</span><span class="sxs-lookup"><span data-stu-id="fee9c-116">As an option, you can also supply property sheets for each configurable provider.</span></span> <span data-ttu-id="fee9c-117">Некоторые службы сообщений ограничить пользователей к представлению только для чтения свойства конфигурации; другие службы сообщений пользователи могут вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="fee9c-117">Some message services restrict users to a read-only view of configuration properties; other message services allow users to make changes.</span></span>
    
   <span data-ttu-id="fee9c-118">Для поддержки программной конфигурации, ваше сообщение функции точки входа службы необходимо иметь возможность работать без вмешательства пользователя.</span><span class="sxs-lookup"><span data-stu-id="fee9c-118">To support programmatic configuration, your message service entry point function must be able to work without user intervention.</span></span> <span data-ttu-id="fee9c-119">Если сообщение службы может вызываться с помощью мастера профилей, должна поддерживать программной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fee9c-119">If your message service can be called by the Profile Wizard, you must support programmatic configuration.</span></span> <span data-ttu-id="fee9c-120">Если службы сообщений не позволяет так, чтобы настроить с помощью мастера профилей, можно ли поддерживать программной конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fee9c-120">If your message service does not allow itself to be configured by using the Profile Wizard, you can choose whether or not to support programmatic configuration.</span></span>
    
   <span data-ttu-id="fee9c-121">Дополнительные сведения о поддержке конфигурации в записи службы сообщений точки функция см [MSGSERVICEENTRY](msgserviceentry.md).</span><span class="sxs-lookup"><span data-stu-id="fee9c-121">For more information about how to support configuration in a message service entry point function, see [MSGSERVICEENTRY](msgserviceentry.md).</span></span>
    
2. <span data-ttu-id="fee9c-122">Публикация имя вашего функции точки входа службы сообщений в файле конфигурации Mapisvc.inf, включая следующую запись в разделе служба сообщений:</span><span class="sxs-lookup"><span data-stu-id="fee9c-122">Publish the name of your message service entry point function in the Mapisvc.inf configuration file by including the following entry in the message service section:</span></span>
    
   `PR_SERVICE_ENTRY_NAME=<name of message service>`
    
3. <span data-ttu-id="fee9c-123">Создание одного или нескольких свойств листа диалоговые окна для отображения данных конфигурации.</span><span class="sxs-lookup"><span data-stu-id="fee9c-123">Create one or more property sheet dialog boxes for displaying configuration data.</span></span>
    
4. <span data-ttu-id="fee9c-124">Если вы хотите разрешить мастер профиля для настройки службы сообщений выполните следующие задачи:</span><span class="sxs-lookup"><span data-stu-id="fee9c-124">Perform the following tasks if you want to allow the Profile Wizard to configure your message service:</span></span>
    
   - <span data-ttu-id="fee9c-125">Реализуйте функцию точки входа, соответствующие прототип [WIZARDENTRY](wizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="fee9c-125">Implement an entry point function that conforms to the [WIZARDENTRY](wizardentry.md) prototype.</span></span> 
    
   - <span data-ttu-id="fee9c-126">Реализация стандартная процедура поле диалоговое окно Windows, который соответствует прототип [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) .</span><span class="sxs-lookup"><span data-stu-id="fee9c-126">Implement a standard Windows dialog box procedure that conforms to the [SERVICEWIZARDDLGPROC](servicewizarddlgproc.md) prototype.</span></span> 
    
   - <span data-ttu-id="fee9c-127">Улучшите ваше сообщение службы функцию точки входа реагировать на дополнительные события.</span><span class="sxs-lookup"><span data-stu-id="fee9c-127">Enhance your message service entry point function to respond to additional events.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="fee9c-128">См. также</span><span class="sxs-lookup"><span data-stu-id="fee9c-128">See also</span></span>

- [<span data-ttu-id="fee9c-129">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="fee9c-129">Message Service Implementation</span></span>](message-service-implementation.md)

