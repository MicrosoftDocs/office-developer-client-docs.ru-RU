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
ms.openlocfilehash: fd7f79ad7a36fd174bf9817ff463b00e6a334104
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808116"
---
# <a name="attsentfor"></a><span data-ttu-id="3038d-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="3038d-103">attSentFor</span></span>

  
  
<span data-ttu-id="3038d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="3038d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="3038d-105">Атрибут **attSentFor** кодируются инвентаризации строк нужным начала до конца.</span><span class="sxs-lookup"><span data-stu-id="3038d-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="3038d-106">Формат для **attSentFor** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="3038d-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="3038d-107">**attSentFor**:</span><span class="sxs-lookup"><span data-stu-id="3038d-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="3038d-108">Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="3038d-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="3038d-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="3038d-109">_email-address_</span></span>
  
> <span data-ttu-id="3038d-110">Тип **:** адрес</span><span class="sxs-lookup"><span data-stu-id="3038d-110">type **:** address</span></span> 
    
<span data-ttu-id="3038d-111">В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых.</span><span class="sxs-lookup"><span data-stu-id="3038d-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="3038d-112">Они по-прежнему включают завершение символы null, однако.</span><span class="sxs-lookup"><span data-stu-id="3038d-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="3038d-113">Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="3038d-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="3038d-114">Только строка адреса объединенный тип **:** символом null.</span><span class="sxs-lookup"><span data-stu-id="3038d-114">Only the combined type **:** address string is null-terminated.</span></span>
  

