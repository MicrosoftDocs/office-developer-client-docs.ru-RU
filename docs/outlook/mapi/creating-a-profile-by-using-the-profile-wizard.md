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
ms.openlocfilehash: f30dca8323f74bc2817bab375b58fcc1bc15c18b
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574260"
---
# <a name="creating-a-profile-by-using-the-profile-wizard"></a><span data-ttu-id="bfd31-103">Создание профиля с помощью мастера профилей</span><span class="sxs-lookup"><span data-stu-id="bfd31-103">Creating a Profile by Using the Profile Wizard</span></span>

  
  
<span data-ttu-id="bfd31-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="bfd31-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="bfd31-105">Мастер профиля является компонентом MAPI, который позволяет пользователю создать профиль в простой из способов.</span><span class="sxs-lookup"><span data-stu-id="bfd31-105">The Profile Wizard is a MAPI feature that enables a user to create a profile in the easiest possible way.</span></span> <span data-ttu-id="bfd31-106">Мастер профиля отображается ряд диалоговых окон, которые запрос пользователю для выбора службы сообщений и введите значения для некоторые важные свойства конфигурации.</span><span class="sxs-lookup"><span data-stu-id="bfd31-106">The Profile Wizard displays a series of dialog boxes which prompt the user to select message services and enter values for a few of the most essential configuration properties.</span></span> <span data-ttu-id="bfd31-107">Для большинства необходимые свойства профилей мастер использует значения по умолчанию, предоставляемые.</span><span class="sxs-lookup"><span data-stu-id="bfd31-107">For most of the other required properties, the Profile Wizard uses default values provided.</span></span> <span data-ttu-id="bfd31-108">Чтобы вызвать мастер профилей, метод **LaunchWizard**, функции, основанной на прототипе [LAUNCHWIZARDENTRY](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="bfd31-108">To invoke the Profile Wizard, call **LaunchWizard**, a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) prototype.</span></span> 
  
<span data-ttu-id="bfd31-109">Пользователя можно добавить в новый профиль, который поддерживает мастер профиля службы сообщений и поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="bfd31-109">The user can add only those message services and service providers to the new profile that support the Profile Wizard.</span></span> <span data-ttu-id="bfd31-110">Так как каждая служба сообщений может потребоваться несколько свойств должно быть задано, чем может обработать мастер профилей, обратите внимание, что если используется этот подход может для одной или нескольких выбранных служб и поставщиков на не полностью настроить.</span><span class="sxs-lookup"><span data-stu-id="bfd31-110">Because each message service might require more properties to be set than the Profile Wizard can handle, be aware that if you use this approach, it is possible for one or more of the selected services or providers to be incompletely configured.</span></span>
  

