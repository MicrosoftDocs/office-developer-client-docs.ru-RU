---
title: Обязанности по сопоставлению со шлюзами
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 214d24bb0b0af525d5e2588c556c37cf720364a0
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422756"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="6fdad-103">Обязанности по сопоставлению со шлюзами</span><span class="sxs-lookup"><span data-stu-id="6fdad-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="6fdad-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6fdad-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6fdad-105">Когда шлюз, поддерживающий MAPI, получает сообщение, содержащее именованные свойства, в одном из специальных наборов свойств, которые содержат свойства Gateway — сопоставляемые со, шлюз должен сопоставить все свойства с протоколом целевой системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="6fdad-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="6fdad-106">Хотя MAPI рекомендует шлюзам обрабатывать все именованные свойства в специальных наборах свойств, шлюзы должны обрабатывать только два: адрес электронной почты и тип адреса.</span><span class="sxs-lookup"><span data-stu-id="6fdad-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="6fdad-107">Так как адрес электронной почты и свойства типа адреса непосредственно влияют на передачу сообщений, очень важно, чтобы шлюзы поддерживали сопоставление этих двух свойств.</span><span class="sxs-lookup"><span data-stu-id="6fdad-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="6fdad-108">Так как ключи поиска состоят из типа адреса и адреса пользователя, они также должны быть переведены, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="6fdad-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="6fdad-109">Идентификаторы записей не должны обрабатываться часто.</span><span class="sxs-lookup"><span data-stu-id="6fdad-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="6fdad-110">Чтобы включить сопоставление идентификатора записи, созданного в одной системе обмена сообщениями, с идентификатором записи, используемым другой системой обмена сообщениями, шлюз должен иметь возможность использовать формат обеих систем.</span><span class="sxs-lookup"><span data-stu-id="6fdad-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="6fdad-111">Так как большинство шлюзов не знают о форматах идентификаторов записей, преобразование идентификаторов записей очень редко.</span><span class="sxs-lookup"><span data-stu-id="6fdad-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="6fdad-112">Еще одно свойство сопоставляемые со, которое не требуется переводить часто, это отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="6fdad-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="6fdad-113">Шлюзы должны хранить отображаемые имена и передавать их, но не обязательно преобразовывать их.</span><span class="sxs-lookup"><span data-stu-id="6fdad-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

