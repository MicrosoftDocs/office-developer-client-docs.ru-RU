---
title: Общие сведения о программировании MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: '���� ���������� ���������: 25 ���� 2012 �.'
ms.openlocfilehash: d69d15f0f635c81bea30401b3a6d6e3ccf620112
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328275"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="e0845-103">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="e0845-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="e0845-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e0845-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e0845-105">Эта Справка по ИНТЕРФЕЙСу API Microsoft Outlook (MAPI) предназначена для разработчиков C и C++ с различными потребностями и опытом.</span><span class="sxs-lookup"><span data-stu-id="e0845-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="e0845-106">Для тех разработчиков, которые хотят использовать MAPI для расширения своих приложений, у которых есть функции обмена сообщениями, не требуется никаких сведений о предварительных требованиях.</span><span class="sxs-lookup"><span data-stu-id="e0845-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="e0845-107">Вам нужен фоновый рисунок в обмене сообщениями и модель компонентных объектов (COM), чтобы использовать MAPI для создания крупномасштабных приложений рабочей группы или драйверов для специализированных служб системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="e0845-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="e0845-108">Перед началом разработки следует рассмотреть следующие сведения о том, как использовать MAPI, процесс входа в систему и как создаются и настраиваются профили и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="e0845-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="e0845-109">Интерфейс MAPI (MAPI) — это обширный набор функций, которые разработчики могут использовать для создания приложений с поддержкой почты.</span><span class="sxs-lookup"><span data-stu-id="e0845-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="e0845-110">Библиотека функций целиком называется MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0845-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="e0845-111">MAPI обеспечивает полный контроль над системой обмена сообщениями на клиентском компьютере, создание и управление сообщениями, управление почтовым ящиком клиента, поставщиками услуг и т. д.</span><span class="sxs-lookup"><span data-stu-id="e0845-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e0845-112">Расширенный MAPI такой же, как и MAPI, и просто называется MAPI в документации по MAPI.</span><span class="sxs-lookup"><span data-stu-id="e0845-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="e0845-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="e0845-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="e0845-114">Simple MAPI предоставляет набор функций, позволяющих добавлять основной уровень функции обмена сообщениями в приложения Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="e0845-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="e0845-115">Функция Simple MAPI MAPISendMail поддерживается в Microsoft Outlook 2013 и Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="e0845-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="e0845-116">Другие простые функции MAPI не поддерживаются в Windows.</span><span class="sxs-lookup"><span data-stu-id="e0845-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

