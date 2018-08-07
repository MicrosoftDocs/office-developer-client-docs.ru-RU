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
ms.openlocfilehash: bf3e79ad32801a659df2c68016167d3b547ddc6f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812422"
---
# <a name="supporting-message-service-installation"></a><span data-ttu-id="c645b-103">Поддержка установки службы сообщений</span><span class="sxs-lookup"><span data-stu-id="c645b-103">Supporting Message Service Installation</span></span>

  
  
<span data-ttu-id="c645b-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="c645b-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="c645b-105">Программы установки для установки службы сообщений необходимо реализовать следующее:</span><span class="sxs-lookup"><span data-stu-id="c645b-105">The setup program for installing your message service should do the following:</span></span>
  
1. <span data-ttu-id="c645b-106">Скопируйте файлы службы сообщений, такие как служба сообщений и поставщика услуг библиотеки DLL, с компакт-диска или на другой диск, на локальный диск на рабочей станции.</span><span class="sxs-lookup"><span data-stu-id="c645b-106">Copy message service files, such as the message service and service provider DLLs, from a CD or disk, to a local drive on the workstation.</span></span> <span data-ttu-id="c645b-107">Файлы, которые необходимо скопировать зависят от службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c645b-107">The files that need to be copied depend on your message service.</span></span> <span data-ttu-id="c645b-108">Обычно выполняется копирование по крайней мере один DLL.</span><span class="sxs-lookup"><span data-stu-id="c645b-108">Typically you will copy at least one DLL.</span></span>
    
2. <span data-ttu-id="c645b-109">Добавление записей в файл конфигурации Mapisvc.inf.</span><span class="sxs-lookup"><span data-stu-id="c645b-109">Add entries to the Mapisvc.inf configuration file.</span></span> <span data-ttu-id="c645b-110">Дополнительные сведения об изменении этого файла для поддержки поставщиков услуг в службе сообщений можно [Файл формата MapiSvc.inf](file-format-of-mapisvc-inf.md).</span><span class="sxs-lookup"><span data-stu-id="c645b-110">For more information about how to modify this file to support the service providers in your message service, see [File Format of MapiSvc.inf](file-format-of-mapisvc-inf.md).</span></span>
    
3. <span data-ttu-id="c645b-111">Добавление записей, соответствующих системного реестра для службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="c645b-111">Add entries, as appropriate, to the system registry for message services.</span></span> <span data-ttu-id="c645b-112">Дополнительные сведения о отображения записей системного реестра содержатся в разделе [Установка подсистемы MAPI](installing-the-mapi-subsystem.md).</span><span class="sxs-lookup"><span data-stu-id="c645b-112">For more information about how the entries should appear in the system registry, see [Installing the MAPI Subsystem](installing-the-mapi-subsystem.md).</span></span>
    
4. <span data-ttu-id="c645b-113">Создание профиля по умолчанию, если один еще не существует, используя один из следующих элементов:</span><span class="sxs-lookup"><span data-stu-id="c645b-113">Create a default profile if one does not yet exist by using one of the following items:</span></span>
    
  - <span data-ttu-id="c645b-114">Мастер профиля, чтобы создать профиль с помощью взаимодействия с пользователем через ряд диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="c645b-114">The Profile Wizard to create a profile by using user interaction through a series of dialog boxes.</span></span> <span data-ttu-id="c645b-115">Дополнительные сведения об использовании мастера профилей [профилей с помощью мастера профилей](creating-a-profile-by-using-the-profile-wizard.md)см.</span><span class="sxs-lookup"><span data-stu-id="c645b-115">For more information about using the Profile Wizard, see [Creating a Profile by Using the Profile Wizard](creating-a-profile-by-using-the-profile-wizard.md).</span></span>
    
  - <span data-ttu-id="c645b-116">Панель управления, чтобы создать профиль с помощью взаимодействия с пользователем.</span><span class="sxs-lookup"><span data-stu-id="c645b-116">The Control Panel to create a profile by using user interaction.</span></span> <span data-ttu-id="c645b-117">Панель управления обеспечивает большую гибкость, чем мастер профиля для настройки службы сообщений и установка свойств профиля пользователя.</span><span class="sxs-lookup"><span data-stu-id="c645b-117">The Control Panel offers the user more flexibility than the Profile Wizard for configuring the message services and setting profile properties.</span></span> 
    
<span data-ttu-id="c645b-118">Размещение программы установки в заданный общедоступный каталог.</span><span class="sxs-lookup"><span data-stu-id="c645b-118">Place the setup program in a designated public directory.</span></span> <span data-ttu-id="c645b-119">Это важно, так как большинство клиентов конфигурации, например, панель управления, обязать пользователей вводить имя каталога.</span><span class="sxs-lookup"><span data-stu-id="c645b-119">This is important because most configuration clients, such as the Control Panel, require that users enter the name of the directory.</span></span> <span data-ttu-id="c645b-120">Панель управления вызывает программы установки, когда пользователь нажимает кнопку **Добавить** , вызывает диалоговое окно **Установить с диска** и указывает путь к файлу программы.</span><span class="sxs-lookup"><span data-stu-id="c645b-120">The Control Panel invokes a setup program when a user clicks the **Add** button, invokes the **Have Disk** dialog box, and specifies the path to the program.</span></span> <span data-ttu-id="c645b-121">Панели управления программы и вызывает функцию точки входа службы сообщений вместе с параметром _ulContext_ , равным MSG_SERVICE_INSTALL.</span><span class="sxs-lookup"><span data-stu-id="c645b-121">The Control Panel runs the program and calls your message service's entry point function with the  _ulContext_ parameter set to MSG_SERVICE_INSTALL.</span></span> 
  
> [!CAUTION]
> <span data-ttu-id="c645b-122">Так как профили являются невосстановимыми частью архитектуры MAPI, убедитесь, что, что программа установки не сохраняет все действия в профиль по умолчанию, рекомендуется использовать для восстановления.</span><span class="sxs-lookup"><span data-stu-id="c645b-122">Because profiles are an expendable part of the MAPI architecture, be sure that your installation program does not store anything in the default profile that would be difficult to recreate.</span></span> <span data-ttu-id="c645b-123">Существует нет программы для восстановления профиля, по перемещению профили с одного компьютера на другой, автономный резервного копирования или для отдельных пользователей или глобальных восстановление из резервных копий.</span><span class="sxs-lookup"><span data-stu-id="c645b-123">There are no utilities for profile recovery, for moving profiles from one computer to another, for off-line backup, or for individual or global restoration from backup copies.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="c645b-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c645b-124">See also</span></span>



[<span data-ttu-id="c645b-125">Реализация службы сообщений</span><span class="sxs-lookup"><span data-stu-id="c645b-125">Message Service Implementation</span></span>](message-service-implementation.md)

