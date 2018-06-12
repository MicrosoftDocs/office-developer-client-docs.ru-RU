---
title: Развертывание списков рассылки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 44231a95-dafc-44f7-bfa9-9f73ea8cb8b7
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 47a37683ac54bef72ebd50aaaa11a36bdfd28659
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808402"
---
# <a name="expanding-distribution-lists"></a><span data-ttu-id="6cd56-103">Развертывание списков рассылки</span><span class="sxs-lookup"><span data-stu-id="6cd56-103">Expanding Distribution Lists</span></span>

  
  
<span data-ttu-id="6cd56-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="6cd56-104">**Applies to**: Outlook</span></span> 
  
 <span data-ttu-id="6cd56-105">**Чтобы запрашивать MAPI разверните список рассылки**</span><span class="sxs-lookup"><span data-stu-id="6cd56-105">**To prompt MAPI to expand a distribution list**</span></span>
  
- <span data-ttu-id="6cd56-106">Присвойте свойству **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) MAPIPDL.</span><span class="sxs-lookup"><span data-stu-id="6cd56-106">Set its **PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) property to MAPIPDL.</span></span>
    
    <span data-ttu-id="6cd56-107">MAPI расширяет адреса с этим типом перед отправкой сообщения поставщика транспорта.</span><span class="sxs-lookup"><span data-stu-id="6cd56-107">MAPI expands addresses with this type before sending the message to the transport provider.</span></span>
    

