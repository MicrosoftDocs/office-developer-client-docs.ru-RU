---
title: Функции и архитектура MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 34bae703-a979-437c-9d86-8b91e9822a54
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 8156cb53fc81f4861e4a66da4960df0458ec6c91
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418283"
---
# <a name="mapi-features-and-architecture"></a><span data-ttu-id="2ff9e-103">Функции и архитектура MAPI</span><span class="sxs-lookup"><span data-stu-id="2ff9e-103">MAPI Features and Architecture</span></span>

  
  
<span data-ttu-id="2ff9e-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2ff9e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2ff9e-105">API обмена сообщениями (MAPI) состоит из набора распространенных программных интерфейсов приложений и компонента библиотеки динамической компоновки (DLL).</span><span class="sxs-lookup"><span data-stu-id="2ff9e-105">Messaging API (MAPI) is composed of a set of common application programming interfaces and a dynamic-link library (DLL) component.</span></span> <span data-ttu-id="2ff9e-106">Интерфейсы используются для создания и доступа к различным приложениям обмена сообщениями и системам обмена сообщениями, предоставляя единую среду для разработки и использования и предоставляя для обоих типов фактическую независимость.</span><span class="sxs-lookup"><span data-stu-id="2ff9e-106">The interfaces are used to create and access diverse messaging applications and messaging systems, offering a uniform environment for development and use, and providing true independence for both.</span></span> <span data-ttu-id="2ff9e-107">Библиотека DLL содержит подсистему MAPI, которая управляет взаимодействием между интерфейсными приложениями обмена сообщениями и внутренними системами обмена сообщениями и предоставляет общий пользовательский интерфейс для часто выполняемых задач.</span><span class="sxs-lookup"><span data-stu-id="2ff9e-107">The DLL contains the MAPI subsystem, which manages the interaction between front-end messaging applications and back-end messaging systems and provides a common user interface for frequent tasks.</span></span> <span data-ttu-id="2ff9e-108">Подсистема MAPI выступает в качестве центральной расчетной палаты для объединения различных систем обмена сообщениями и клиентов экранирования из их отличий.</span><span class="sxs-lookup"><span data-stu-id="2ff9e-108">The MAPI subsystem acts as a central clearinghouse to unify the various messaging systems and shield clients from their differences.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="2ff9e-109">См. также</span><span class="sxs-lookup"><span data-stu-id="2ff9e-109">See also</span></span>



[<span data-ttu-id="2ff9e-110">Понятия MAPI</span><span class="sxs-lookup"><span data-stu-id="2ff9e-110">MAPI Concepts</span></span>](mapi-concepts.md)

