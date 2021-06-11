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
ms.openlocfilehash: 17e900ac28481388379133a95b4b206ca4bc1805
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33427656"
---
# <a name="attowner"></a><span data-ttu-id="2a293-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="2a293-103">attOwner</span></span>

  
  
<span data-ttu-id="2a293-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="2a293-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="2a293-105">Атрибут **attOwner** закодирован как подсчитываемая строка, заложенная в конец.</span><span class="sxs-lookup"><span data-stu-id="2a293-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="2a293-106">Формат **attOwner:**</span><span class="sxs-lookup"><span data-stu-id="2a293-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="2a293-107">**attOwner:**</span><span class="sxs-lookup"><span data-stu-id="2a293-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="2a293-108">адрес электронной почты с отображаемой  _именем-именем_</span><span class="sxs-lookup"><span data-stu-id="2a293-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="2a293-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="2a293-109">_email-address_</span></span>
  
> <span data-ttu-id="2a293-110">**тип:** адрес</span><span class="sxs-lookup"><span data-stu-id="2a293-110">type **:** address</span></span> 
    
<span data-ttu-id="2a293-111">В отличие от других значений длины, отображаемая длина и длина адреса являются неподписаными 16-битными значениями вместо неподписаных длинных многословий.</span><span class="sxs-lookup"><span data-stu-id="2a293-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="2a293-112">Они по-прежнему включают прекращение null символов, однако.</span><span class="sxs-lookup"><span data-stu-id="2a293-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="2a293-113">Строки типа и адреса в  _записи электронного_ адреса разделены буквальной двоеточием (:) символ, например "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="2a293-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="2a293-114">Только комбинированный **тип:** строка адресов не прекращается.</span><span class="sxs-lookup"><span data-stu-id="2a293-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="2a293-115">Сопоставление свойств MAPI с атрибутом **attOwner** зависит от класса сообщений кодируемых сообщений.</span><span class="sxs-lookup"><span data-stu-id="2a293-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

