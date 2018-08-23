---
title: attSentFor
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: aa8c8d64-d2a0-4cdf-a8aa-21c8d0a0a3fc
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: b292e65ddabcbe052832687a3dcf01658de5e379
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22567477"
---
# <a name="attsentfor"></a><span data-ttu-id="90ffb-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="90ffb-103">attSentFor</span></span>

  
  
<span data-ttu-id="90ffb-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="90ffb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="90ffb-105">Атрибут **attSentFor** кодируются инвентаризации строк нужным начала до конца.</span><span class="sxs-lookup"><span data-stu-id="90ffb-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="90ffb-106">Формат для **attSentFor** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="90ffb-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="90ffb-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="90ffb-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="90ffb-108">Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="90ffb-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="90ffb-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="90ffb-109">_email-address_</span></span>
  
> <span data-ttu-id="90ffb-110">Тип **:** адрес</span><span class="sxs-lookup"><span data-stu-id="90ffb-110">type **:** address</span></span> 
    
<span data-ttu-id="90ffb-111">В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых.</span><span class="sxs-lookup"><span data-stu-id="90ffb-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="90ffb-112">Они по-прежнему включают завершение символы null, однако.</span><span class="sxs-lookup"><span data-stu-id="90ffb-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="90ffb-113">Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="90ffb-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="90ffb-114">Только строка адреса объединенный тип **:** символом null.</span><span class="sxs-lookup"><span data-stu-id="90ffb-114">Only the combined type **:** address string is null-terminated.</span></span>
  

