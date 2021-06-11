---
title: Отправка отчетов о доставке сообщений
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: abb12ec5-f0b7-488a-a75d-446f4be53e96
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 2a31e7d088d5c1f94b272cb4d307f3aff99f32ee
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33433082"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="5fae3-103">Отправка отчетов о доставке сообщений</span><span class="sxs-lookup"><span data-stu-id="5fae3-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="5fae3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="5fae3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="5fae3-105">Некоторые системы обмена сообщениями поддерживают отчеты о доставке, а некоторые нет.</span><span class="sxs-lookup"><span data-stu-id="5fae3-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="5fae3-106">То, как поставщик транспорта определяет, можно ли отправлять отчеты о доставке или неделивке в клиентские приложения, является подробной реализацией, конкретной для отдельных поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="5fae3-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="5fae3-107">Если отчеты о доставке можно отправить в клиентские приложения, поставщики транспорта используют метод [IMAPISupport::StatusRecips,](imapisupport-statusrecips.md) чтобы уведомить MAPI об успешной или неудачной доставке для одного или более получателей.</span><span class="sxs-lookup"><span data-stu-id="5fae3-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="5fae3-108">После этого MAPI создает отчеты о доставке или неделивстве, соответствующие этим получателям.</span><span class="sxs-lookup"><span data-stu-id="5fae3-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="5fae3-109">Поставщики транспорта также могут перевести входящие отчеты о доставке и неделивстве, которые являются родными для системы обмена сообщениями, в отчеты о доставке и неделиверии MAPI с помощью **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="5fae3-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

