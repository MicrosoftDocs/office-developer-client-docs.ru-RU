---
title: Отправка отчетов о доСтавке сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32332839"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="8a534-103">Отправка отчетов о доСтавке сообщений</span><span class="sxs-lookup"><span data-stu-id="8a534-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="8a534-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="8a534-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="8a534-105">Некоторые базовые системы обмена сообщениями поддерживают отчеты о доставке, а другие — нет.</span><span class="sxs-lookup"><span data-stu-id="8a534-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="8a534-106">Сведения о том, как поставщик транспорта определяет, можно ли отправлять отчеты о доставке или недоставке в клиентские приложения, сведения о реализации относятся к отдельным поставщикам транспорта.</span><span class="sxs-lookup"><span data-stu-id="8a534-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="8a534-107">Если отчеты о доставке можно отправлять в клиентские приложения, поставщики транспорта используют метод [имаписуппорт:: статусреЦипс](imapisupport-statusrecips.md) , чтобы уведомить MAPI о успешной или неудачной доставке для одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="8a534-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="8a534-108">Затем MAPI создает отчеты о доставке или недоставке, соответствующие указанным получателям.</span><span class="sxs-lookup"><span data-stu-id="8a534-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="8a534-109">Поставщики транспорта также могут транслировать отчеты о входящей доставке и о недоставке, которые являются собственными для системы обмена сообщениями, в отчеты о доставке и недоставке MAPI с помощью **статусреЦипс**.</span><span class="sxs-lookup"><span data-stu-id="8a534-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

