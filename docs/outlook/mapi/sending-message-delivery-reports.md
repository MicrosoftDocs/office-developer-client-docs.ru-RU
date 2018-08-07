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
ms.openlocfilehash: d94785df9becf46bbfad66465facea35202c6079
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812245"
---
# <a name="sending-message-delivery-reports"></a><span data-ttu-id="4332f-103">Отправка отчетов о доставке сообщений</span><span class="sxs-lookup"><span data-stu-id="4332f-103">Sending Message Delivery Reports</span></span>

  
  
<span data-ttu-id="4332f-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="4332f-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="4332f-105">Некоторые базовой системы обмена сообщениями поддерживают отчеты о доставке и некоторых — отключена.</span><span class="sxs-lookup"><span data-stu-id="4332f-105">Some underlying messaging systems support delivery reports and some do not.</span></span> <span data-ttu-id="4332f-106">Как поставщика транспорта определяет, будет ли отчеты о доставке или недоставке сообщения могут быть отправлены на клиентские приложения — это специально для отдельных транспорта поставщиков сведения о реализации.</span><span class="sxs-lookup"><span data-stu-id="4332f-106">How the transport provider determines whether message delivery or nondelivery reports can be sent to client applications is an implementation detail specific to individual transport providers.</span></span> <span data-ttu-id="4332f-107">Если отчеты о доставке могут быть отправлены на клиентские приложения, поставщиками транспорта используйте метод [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) для уведомления MAPI успешного или неудачного доставки для одного или нескольких получателей.</span><span class="sxs-lookup"><span data-stu-id="4332f-107">If delivery reports can be sent to client applications, transport providers use the [IMAPISupport::StatusRecips](imapisupport-statusrecips.md) method to notify MAPI of successful or unsuccessful delivery for one or more recipients.</span></span> <span data-ttu-id="4332f-108">MAPI создает отчеты о доставке или недоставке, соответствующий тем пользователям.</span><span class="sxs-lookup"><span data-stu-id="4332f-108">MAPI then generates delivery or nondelivery reports corresponding to those recipients.</span></span> <span data-ttu-id="4332f-109">Поставщиками транспорта также можно перевести входящих доставке и недоставке отчетов, присущих системы обмена сообщениями в доставке MAPI и отчет о недоставке с помощью **StatusRecips**.</span><span class="sxs-lookup"><span data-stu-id="4332f-109">Transport providers can also translate incoming delivery and nondelivery reports that are native to the messaging system into MAPI delivery and nondelivery reports by means of **StatusRecips**.</span></span>
  

