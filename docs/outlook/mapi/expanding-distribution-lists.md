---
title: Развертывание списков рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: c7c0043ed898a827b2ea8c65b20837c571f88883
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22582058"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="40f04-103">Развертывание списков рассылки</span><span class="sxs-lookup"><span data-stu-id="40f04-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="40f04-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="40f04-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
 <span data-ttu-id="40f04-105">**Чтобы запрашивать MAPI разверните список рассылки**</span><span class="sxs-lookup"><span data-stu-id="40f04-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="40f04-106">Присвойте свойству **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="40f04-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="40f04-107">MAPI расширяет адреса с этим типом перед отправкой сообщения поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="40f04-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

