---
title: Создание профиля с помощью мастера профилей
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 4b611818-f99f-43a2-9f6b-1aa5b9564d1d
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: a93cfb05d8abfffc9f55a7ea48efc3c3451dddbb
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411738"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="5ec04-103">Создание профиля с помощью мастера профилей</span><span class="sxs-lookup"><span data-stu-id="5ec04-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="5ec04-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5ec04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5ec04-105">Мастер профилей — это функция MAPI, которая позволяет пользователю создавать профиль самым простым способом.</span><span class="sxs-lookup"><span data-stu-id="5ec04-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="5ec04-106">Мастер профилей отображает ряд диалогов, которые побуждают пользователя выбирать службы сообщений и вводить значения для нескольких наиболее важных свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5ec04-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="5ec04-107">Для большинства других необходимых свойств мастер профилей использует предоставленные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5ec04-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="5ec04-108">Чтобы вызвать мастер профиля, позвоните **в LaunchWizard**, функцию, основанную на [прототипе LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="5ec04-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="5ec04-109">Пользователь может добавлять в новый профиль только те службы и поставщики сообщений, которые поддерживают мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="5ec04-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="5ec04-110">Поскольку для каждой службы сообщений может потребоваться больше свойств, чем может обрабатывать мастер профилей, следует помнить, что при использовании этого подхода может быть неполно настроена одна или несколько выбранных служб или поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5ec04-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

