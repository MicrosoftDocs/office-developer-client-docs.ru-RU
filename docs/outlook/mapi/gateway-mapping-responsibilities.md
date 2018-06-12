---
title: Обязанности сопоставления шлюза
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ac67bb83-e4f3-4c82-995b-c11a2a195e90
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: ad5f4e896b748dc0d7495c428af093af57bc7cdd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808522"
---
# <a name="gateway-mapping-responsibilities"></a><span data-ttu-id="ca452-103">Обязанности сопоставления шлюза</span><span class="sxs-lookup"><span data-stu-id="ca452-103">Gateway mapping responsibilities</span></span>

<span data-ttu-id="ca452-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ca452-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ca452-105">Получив принять во внимание MAPI шлюза сообщений с именованных свойств в одном специальные свойства наборов данных, предназначенный для хранения шлюза сопоставляемые свойства, шлюз следует сопоставить все свойства протокола назначения, системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ca452-105">When a MAPI-aware gateway receives a message containing named properties in one of the special property sets designated to contain gateway-mappable properties, the gateway should map all of the properties to the protocol of the destination messaging system.</span></span> <span data-ttu-id="ca452-106">Несмотря на то, что MAPI рекомендует, шлюзы обрабатывать все именованные свойства в наборы специальных свойств, шлюзы должны обрабатывать только два: адрес электронной почты и тип адреса.</span><span class="sxs-lookup"><span data-stu-id="ca452-106">Although MAPI recommends that gateways handle all named properties in the special property sets, gateways are expected to handle only two: email address and address type.</span></span> <span data-ttu-id="ca452-107">Так как свойства типа адреса и адрес электронной почты непосредственно влияют на передачи сообщений, очень важно, что шлюзы поддерживают сопоставления эти два свойства.</span><span class="sxs-lookup"><span data-stu-id="ca452-107">Because the email address and address type properties directly affect message transmission, it is critical that gateways support the mapping of these two properties.</span></span> <span data-ttu-id="ca452-108">Так как ключи поиска состоят из тип адреса и адрес пользователя, они также преобразования, если это возможно.</span><span class="sxs-lookup"><span data-stu-id="ca452-108">Because search keys consist of a user's address type and address, they should also be translated if at all possible.</span></span>
  
<span data-ttu-id="ca452-109">Идентификаторы записей, не должны обрабатываться часто.</span><span class="sxs-lookup"><span data-stu-id="ca452-109">Entry identifiers are not expected to be handled frequently.</span></span> <span data-ttu-id="ca452-110">Для включения сопоставления идентификатора запись, которая исходит в одной системе обмена сообщениями для записи идентификатор, который можно использовать с другой системой обмена сообщениями, шлюз должен иметь возможность использовать формат обеими системами.</span><span class="sxs-lookup"><span data-stu-id="ca452-110">To enable mapping of an entry identifier that originates in one messaging system to an entry identifier that is usable by another messaging system, the gateway must be able to use the format of both systems.</span></span> <span data-ttu-id="ca452-111">Поскольку большинство шлюзы не поддерживают запись идентификатор форматы, перевода идентификаторы записей очень редко.</span><span class="sxs-lookup"><span data-stu-id="ca452-111">Because most gateways are not aware of entry identifier formats, the translation of entry identifiers is rare.</span></span>
  
<span data-ttu-id="ca452-112">Другой сопоставляемые свойства, которые не должны быть переведены часто — отображаемое имя.</span><span class="sxs-lookup"><span data-stu-id="ca452-112">Another mappable property that is not expected to be translated frequently is the display name.</span></span> <span data-ttu-id="ca452-113">Шлюзы следует хранить отображаемые имена и передавать их, но переводчик не обязательно.</span><span class="sxs-lookup"><span data-stu-id="ca452-113">Gateways should store display names and transmit them, but not necessarily translate them.</span></span> 
  

