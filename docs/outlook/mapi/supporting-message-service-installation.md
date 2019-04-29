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
# <a name="supporting-message-service-installation"></a><span data-ttu-id="7c914-103">Поддержка установки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="7c914-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="7c914-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="7c914-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="7c914-105">Программа установки для установки службы сообщений должна выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="7c914-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="7c914-106">Скопируйте файлы службы сообщений, например библиотеки DLL службы сообщений и поставщика услуг, с компакт-диска или диска на локальный диск рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="7c914-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="7c914-107">Файлы, которые необходимо скопировать, зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="7c914-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="7c914-108">Как правило, необходимо скопировать по крайней мере одну БИБЛИОТЕКУ DLL.</span><span class="sxs-lookup"><span data-stu-id="7c914-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="7c914-109">Добавьте записи в файл конфигурации Mapisvc. INF.</span><span class="sxs-lookup"><span data-stu-id="7c914-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="7c914-110">Дополнительные сведения о том, как изменить этот файл для поддержки поставщиков услуг в службе сообщений, можно найти в разделе [Формат файла MapiSvc. INF](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="7c914-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="7c914-111">Добавьте необходимые записи в системный реестр для служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="7c914-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="7c914-112">Для получения дополнительных сведений о том, как записи должны отображаться в системном реестре, ознакомьтесь со статьей [Установка подсистемы MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="7c914-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="7c914-113">Создайте профиль по умолчанию, если он еще не существует, используя один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="7c914-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="7c914-114">Мастер профилей для создания профиля с помощью взаимодействия с пользователем через ряд диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="7c914-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="7c914-115">Более подробную информацию об использовании мастера профилей можно узнать в статье [Создание профиля с помощью мастера профилей](creating-a-profile-by-using-the-profile-wizard.md).</span><span class="sxs-lookup"><span data-stu-id="7c914-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="7c914-116">Панель управления для создания профиля с помощью взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="7c914-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="7c914-117">Панель управления предоставляет пользователю более гибкие возможности, чем мастер профилей для настройки служб сообщений и настройки свойств профиля.</span><span class="sxs-lookup"><span data-stu-id="7c914-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="7c914-118">Поместите программу установки в назначенный общедоступный каталог.</span><span class="sxs-lookup"><span data-stu-id="7c914-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="7c914-119">Это важно, так как большинство клиентов конфигурации, таких как панель управления, требуют, чтобы пользователи вводили имя каталога.</span><span class="sxs-lookup"><span data-stu-id="7c914-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="7c914-120">Панель управления вызывает программу установки, когда пользователь нажимает кнопку **Добавить** , вызывает диалоговое окно " **с диском** " и задает путь к программе.</span><span class="sxs-lookup"><span data-stu-id="7c914-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="7c914-121">Панель управления запускает программу и вызывает функцию точки входа службы сообщений с параметром _улконтекст_ , равным мсг_сервице_инсталл.</span><span class="sxs-lookup"><span data-stu-id="7c914-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="7c914-122">Так как профили являются возможной частью архитектуры MAPI, убедитесь, что программа установки не сохраняет ничего в профиле по умолчанию, который трудно воссоздать.</span><span class="sxs-lookup"><span data-stu-id="7c914-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="7c914-123">Для перемещения профилей с одного компьютера на другой, для автономного резервного копирования или для отдельного или глобального восстановления из резервных копий нет служебных программ для восстановления профилей.</span><span class="sxs-lookup"><span data-stu-id="7c914-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="7c914-124">См. также</span><span class="sxs-lookup"><span data-stu-id="7c914-124">See also</span></span>



[<span data-ttu-id="7c914-125">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="7c914-125">Message Service Implementation</span></span>](message-service-implementation.md)

