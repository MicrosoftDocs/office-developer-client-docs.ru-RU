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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408343"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="b6d3d-103">Общие сведения о программировании MAPI</span><span class="sxs-lookup"><span data-stu-id="b6d3d-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="b6d3d-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b6d3d-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b6d3d-105">Эта справка по API сообщений Microsoft Outlook (MAPI) написана для разработчиков C и C++ с различными потребностями и опытом работы с сообщениями.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="b6d3d-106">Для тех разработчиков, которые хотят использовать MAPI для расширения своих приложений с функциями обмена сообщениями, никаких специальных знаний не требуется.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="b6d3d-107">Для использования MAPI для создания полномасштабных приложений рабочих групп или драйверов для специализированных систем обмена сообщениями необходим фон обмена сообщениями и модель COM.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="b6d3d-108">Перед началом разработки следует учесть следующие сведения об использовании MAPI, процессе запуска и настройке профилей и служб сообщений.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="b6d3d-109">MapI — это обширный набор функций, которые разработчики могут использовать для создания приложений с включенной поддержкой почты.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="b6d3d-110">Полная библиотека функций называется MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="b6d3d-111">MAPI обеспечивает полный контроль над системой обмена сообщениями на клиентском компьютере, создание сообщений и управление ими, управление почтовым ящиком клиента, поставщиками услуг и так далее.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="b6d3d-112">Расширенный MAPI такой же, как MAPI, и просто называется MAPI в документации MAPI.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="b6d3d-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="b6d3d-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="b6d3d-114">Simple MAPI предоставляет набор функций, позволяющих добавить базовый уровень функций обмена сообщениями в приложения на основе Microsoft Windows.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="b6d3d-115">Простая функция MAPI MAPISendMail поддерживается в Microsoft Outlook 2013 и Microsoft Outlook 2010, русская версия.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="b6d3d-116">Другие простые функции MAPI были неподготовлены в Windows.</span><span class="sxs-lookup"><span data-stu-id="b6d3d-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

