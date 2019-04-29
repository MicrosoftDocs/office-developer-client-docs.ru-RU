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
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="5be05-103">Создание профиля с помощью мастера профилей</span><span class="sxs-lookup"><span data-stu-id="5be05-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="5be05-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5be05-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5be05-105">Мастер профилей — это компонент MAPI, который позволяет пользователю создать профиль простым способом.</span><span class="sxs-lookup"><span data-stu-id="5be05-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="5be05-106">Мастер профилей отображает ряд диалоговых окон, предлагающих пользователю выбрать службы сообщений и ввести значения для нескольких наиболее важных свойств конфигурации.</span><span class="sxs-lookup"><span data-stu-id="5be05-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="5be05-107">Для большинства других обязательных свойств мастер профилей использует предоставленные значения по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="5be05-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="5be05-108">Чтобы вызвать мастер профилей, вызовите **лаунчвизард**, функцию на основе прототипа [лаунчвизардентри](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="5be05-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="5be05-109">Пользователь может добавить в новый профиль только тех служб и поставщиков служб сообщений, которые поддерживают мастер профилей.</span><span class="sxs-lookup"><span data-stu-id="5be05-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="5be05-110">Так как для каждой службы сообщений может потребоваться задать больше свойств, чем мастер профилей может обработать, следует помнить, что при использовании этого способа невозможно настроить одну или несколько выбранных служб или поставщиков.</span><span class="sxs-lookup"><span data-stu-id="5be05-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

