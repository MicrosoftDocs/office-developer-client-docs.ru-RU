---
title: attOwner
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 3c6a4050-fd97-42ce-abb1-118254b367bd
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 865d929f3348710b7786f4182670f3304a3a9244
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22578040"
---
# <a name="attowner"></a><span data-ttu-id="57812-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="57812-103">attOwner</span></span>

  
  
<span data-ttu-id="57812-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="57812-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="57812-105">Атрибут **attOwner** кодируются инвентаризации строк нужным начала до конца.</span><span class="sxs-lookup"><span data-stu-id="57812-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="57812-106">Формат для **attOwner** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="57812-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="57812-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="57812-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="57812-108">Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="57812-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="57812-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="57812-109">_email-address_</span></span>
  
> <span data-ttu-id="57812-110">Тип **:** адрес</span><span class="sxs-lookup"><span data-stu-id="57812-110">type **:** address</span></span> 
    
<span data-ttu-id="57812-111">В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых.</span><span class="sxs-lookup"><span data-stu-id="57812-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="57812-112">Они по-прежнему включают завершение символы null, однако.</span><span class="sxs-lookup"><span data-stu-id="57812-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="57812-113">Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="57812-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="57812-114">Только строка адреса объединенный тип **:** символом null.</span><span class="sxs-lookup"><span data-stu-id="57812-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="57812-115">Сопоставление свойств MAPI для атрибута **attOwner** , зависит от класса сообщений для кодирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="57812-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

