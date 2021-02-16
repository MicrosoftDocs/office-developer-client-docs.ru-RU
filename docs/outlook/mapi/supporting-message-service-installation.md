---
title: Поддержка установки службы сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 822e07bc-0bca-4485-8938-2264315161e2
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 328884e8758e679eb1c9d968547cba02c01d4d47
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33404703"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="2ecce-103">Поддержка установки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="2ecce-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="2ecce-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ecce-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ecce-105">Программа установки для установки службы сообщений должна сделать следующее:</span><span class="sxs-lookup"><span data-stu-id="2ecce-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="2ecce-106">Копирование файлов службы сообщений, таких как DLL службы сообщений и поставщиков услуг, с компакт-диска или диска на локальный диск на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="2ecce-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="2ecce-107">Файлы, которые необходимо скопировать, зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ecce-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="2ecce-108">Как правило, вы копируете по крайней мере одну DLL-</span><span class="sxs-lookup"><span data-stu-id="2ecce-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="2ecce-109">Добавьте записи в файл конфигурации Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="2ecce-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="2ecce-110">Дополнительные сведения об изменении этого файла для поддержки поставщиков услуг в службе сообщений см. в формате файла [MapiSvc.inf.](file-format-of-mapisvc-inf.md)</span><span class="sxs-lookup"><span data-stu-id="2ecce-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="2ecce-111">При необходимости добавьте записи в системный реестр для служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="2ecce-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="2ecce-112">Дополнительные сведения о том, как записи должны отображаться в системных реестрах, см. в подсистеме [MAPI.](installing-the-mapi-subsystem.md)</span><span class="sxs-lookup"><span data-stu-id="2ecce-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="2ecce-113">Создайте профиль по умолчанию, если он еще не существует, используя один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="2ecce-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="2ecce-114">Мастер профилей для создания профиля с помощью взаимодействия с пользователем с помощью ряда диалогов.</span><span class="sxs-lookup"><span data-stu-id="2ecce-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="2ecce-115">Дополнительные сведения об использовании мастера профилей см. в теме ["Создание профиля с помощью мастера профилей".](creating-a-profile-by-using-the-profile-wizard.md)</span><span class="sxs-lookup"><span data-stu-id="2ecce-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="2ecce-116">Панель управления для создания профиля с помощью взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="2ecce-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="2ecce-117">Панель управления предоставляет пользователю большую гибкость, чем мастер профилей для настройки служб сообщений и настройки свойств профиля.</span><span class="sxs-lookup"><span data-stu-id="2ecce-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="2ecce-118">Поместите программу установки в выделенный общедоступный каталог.</span><span class="sxs-lookup"><span data-stu-id="2ecce-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="2ecce-119">Это важно, так как большинство клиентов конфигурации, таких как панель управления, требуют, чтобы пользователи введите имя каталога.</span><span class="sxs-lookup"><span data-stu-id="2ecce-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="2ecce-120">Панель управления вызывает программу установки, когда пользователь  нажимает кнопку  "Добавить", вызывает диалоговое окно "На диске" и указывает путь к программе.</span><span class="sxs-lookup"><span data-stu-id="2ecce-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="2ecce-121">Панель управления запускает программу и вызывает функцию точки входа службы сообщений с параметром  _ulContext,_ MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="2ecce-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="2ecce-122">Так как профили являются частью архитектуры MAPI, убедитесь, что программа установки не хранит в профиле по умолчанию ничего, что было бы трудно воссоздать.</span><span class="sxs-lookup"><span data-stu-id="2ecce-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="2ecce-123">Не существует программ для восстановления профилей, перемещения профилей с одного компьютера на другой, для резервного копирования вне сети или для отдельного или глобального восстановления из резервных копий.</span><span class="sxs-lookup"><span data-stu-id="2ecce-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="2ecce-124">См. также</span><span class="sxs-lookup"><span data-stu-id="2ecce-124">See also</span></span>



[<span data-ttu-id="2ecce-125">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="2ecce-125">Message Service Implementation</span></span>](message-service-implementation.md)

