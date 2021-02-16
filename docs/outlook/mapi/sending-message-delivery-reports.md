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
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="9dc5c-103">Отправка отчетов о доставке сообщений</span><span class="sxs-lookup"><span data-stu-id="9dc5c-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="9dc5c-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9dc5c-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9dc5c-105">Некоторые из них поддерживают отчеты о доставке, а другие нет.</span><span class="sxs-lookup"><span data-stu-id="9dc5c-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="9dc5c-106">То, как поставщик транспорта определяет, можно ли отправлять отчеты о доставке или ненастройке сообщений в клиентские приложения, является подробной реализацией, характерной для отдельных поставщиков транспорта.</span><span class="sxs-lookup"><span data-stu-id="9dc5c-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="9dc5c-107">Если отчеты о доставке можно отправить в клиентские приложения, поставщики транспорта используют метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для уведомления MAPI об успешной или неудачной доставке для одного или более получателей.</span><span class="sxs-lookup"><span data-stu-id="9dc5c-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="9dc5c-108">MapI затем создает отчеты о доставке или ненастройстве, соответствующие этим получателям.</span><span class="sxs-lookup"><span data-stu-id="9dc5c-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="9dc5c-109">Поставщики транспорта также могут преобразовывать входящие отчеты о доставке и ненастройстве, относящуюся к системе обмена сообщениями, в отчеты о доставке и нестандартных сообщениях MAPI с помощью **StatusRecips.**</span><span class="sxs-lookup"><span data-stu-id="9dc5c-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

