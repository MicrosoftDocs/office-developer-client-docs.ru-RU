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
ms.openlocfilehash: 0cb40c3c644618bdf65a2c90a91580a5be8fc88c
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808096"
---
# <a name="attowner"></a><span data-ttu-id="5e820-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="5e820-103">attOwner</span></span>

  
  
<span data-ttu-id="5e820-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="5e820-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="5e820-105">Атрибут **attOwner** кодируются инвентаризации строк нужным начала до конца.</span><span class="sxs-lookup"><span data-stu-id="5e820-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="5e820-106">Формат для **attOwner** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="5e820-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="5e820-107">**attOwner**:</span><span class="sxs-lookup"><span data-stu-id="5e820-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="5e820-108">Длина имени отображения отображаемое имя — длина адреса _адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="5e820-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="5e820-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="5e820-109">_email-address_</span></span>
  
> <span data-ttu-id="5e820-110">Тип **:** адрес</span><span class="sxs-lookup"><span data-stu-id="5e820-110">type **:** address</span></span> 
    
<span data-ttu-id="5e820-111">В отличие от других длины значения, отображаемое имя длину и длину адреса имеют неподписанных значения 16-разрядный вместо длинных целых.</span><span class="sxs-lookup"><span data-stu-id="5e820-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="5e820-112">Они по-прежнему включают завершение символы null, однако.</span><span class="sxs-lookup"><span data-stu-id="5e820-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="5e820-113">Тип и адрес строк в запись _адреса электронной почты_ , разделенных как двоеточие (:) литерал, например «smtp:joe@nowhere.com».</span><span class="sxs-lookup"><span data-stu-id="5e820-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="5e820-114">Только строка адреса объединенный тип **:** символом null.</span><span class="sxs-lookup"><span data-stu-id="5e820-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="5e820-115">Сопоставление свойств MAPI для атрибута **attOwner** , зависит от класса сообщений для кодирования сообщения.</span><span class="sxs-lookup"><span data-stu-id="5e820-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

