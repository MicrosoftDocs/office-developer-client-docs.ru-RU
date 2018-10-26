---
title: ����� �������� � ���������������� MAPI
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 30ac637a-874f-4660-b5d0-d28d69486f64
description: 'Дата последнего изменения: 25 июня 2012 года'
ms.openlocfilehash: bd9cdd9119f94e1f7684be34e1b4ef6fb40ab2bf
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22576507"
---
# <a name="mapi-programming-overview"></a><span data-ttu-id="f4aa6-103">����� �������� � ���������������� MAPI</span><span class="sxs-lookup"><span data-stu-id="f4aa6-103">MAPI Programming Overview</span></span>

  
  
<span data-ttu-id="f4aa6-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="f4aa6-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="f4aa6-105">Этот справочник по API системы обмена сообщениями Microsoft Outlook (MAPI) для C, и разработчики C++ с различными должно и опыт работы с мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-105">This Microsoft Outlook Messaging API (MAPI) Reference is written for C and C++ developers with a variety of needs and experience with messaging.</span></span> <span data-ttu-id="f4aa6-106">Для разработчиков, которым необходимо использовать MAPI для расширения приложений, которые имеют функции обмена сообщениями не определенных необходимые знания является обязательным.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-106">For those developers who want to use MAPI to augment their applications that have messaging features, no specific prerequisite knowledge is required.</span></span> <span data-ttu-id="f4aa6-107">Требуется опыт в системе обмена сообщениями и модели компонентных объектов (COM) для использования протокола MAPI для создания приложений полномасштабное рабочей группы или драйверы для специализированных служб системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-107">You need a background in messaging and the Component Object Model (COM) to use MAPI to create full-scale workgroup applications or drivers for specialized messaging system services.</span></span>
  
<span data-ttu-id="f4aa6-108">Прежде чем начинать работу по разработке, необходимо учитывать следующие сведения об использовании MAPI, процесс входа в систему, а также способа создания и настройки профилей и службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-108">Before starting development work, you should consider the following information about how to use MAPI, the logon process, and how profiles and message services are created and configured.</span></span>
  
<span data-ttu-id="f4aa6-109">Программы интерфейса MAPI (Messaging Application) — это обширный набор функций, которые могут использоваться разработчиками для создания приложений с поддержкой почты.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-109">The Messaging Application Program Interface (MAPI) is an extensive set of functions that developers can use to create mail-enabled applications.</span></span> <span data-ttu-id="f4aa6-110">Библиотека полный функций называется MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-110">The full function library is known as MAPI.</span></span> <span data-ttu-id="f4aa6-111">MAPI позволяет контролировать системы обмена сообщениями на клиентском компьютере, создание и управление сообщений, управление почтовый ящик клиента, поставщиков услуг и т. д.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-111">MAPI enables complete control over the messaging system on the client computer, creation and management of messages, management of the client mailbox, service providers, and so on.</span></span>
  
> [!NOTE]
> <span data-ttu-id="f4aa6-112">Расширенного MAPI совпадает с MAPI, а просто называется MAPI в документации по MAPI.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-112">Extended MAPI is the same as MAPI, and is simply referred to as MAPI in the MAPI documentation.</span></span> 
  
 <span data-ttu-id="f4aa6-113">**Simple MAPI**</span><span class="sxs-lookup"><span data-stu-id="f4aa6-113">**Simple MAPI**</span></span>
  
<span data-ttu-id="f4aa6-114">Simple MAPI предоставляет набор функций, который позволяет добавить базовый уровень функциональные возможности Microsoft Windows приложения на основе системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-114">Simple MAPI provides a set of functions that enables you to add a basic level of messaging functionality to Microsoft Windows-based applications.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="f4aa6-115">Функция Simple MAPI MAPISendMail поддерживается в Microsoft Outlook 2013 и Microsoft Outlook 2010.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-115">The Simple MAPI function MAPISendMail is supported by Microsoft Outlook 2013 and Microsoft Outlook 2010.</span></span> <span data-ttu-id="f4aa6-116">Другие функции Simple MAPI являются устаревшими в Windows.</span><span class="sxs-lookup"><span data-stu-id="f4aa6-116">Other Simple MAPI functions have been deprecated in Windows.</span></span> 
  

