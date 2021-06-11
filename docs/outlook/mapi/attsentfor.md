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
ms.openlocfilehash: f961348e7be474202273aa97a2922566ef40c3a5
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33408840"
---
# <a name="attsentfor"></a><span data-ttu-id="19718-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="19718-103">attSentFor</span></span>

  
  
<span data-ttu-id="19718-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="19718-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="19718-105">Атрибут **attSentFor** закодирован как подсчитываемая строка, заложенная в конец.</span><span class="sxs-lookup"><span data-stu-id="19718-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="19718-106">Формат **attSentFor** следующим образом:</span><span class="sxs-lookup"><span data-stu-id="19718-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="19718-107">**attSentFor:**</span><span class="sxs-lookup"><span data-stu-id="19718-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="19718-108">адрес электронной почты с отображаемой  _именем-именем_</span><span class="sxs-lookup"><span data-stu-id="19718-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="19718-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="19718-109">_email-address_</span></span>
  
> <span data-ttu-id="19718-110">**тип:** адрес</span><span class="sxs-lookup"><span data-stu-id="19718-110">type **:** address</span></span> 
    
<span data-ttu-id="19718-111">В отличие от других значений длины, отображаемая длина и длина адреса являются неподписаными 16-битными значениями вместо неподписаных длинных многословий.</span><span class="sxs-lookup"><span data-stu-id="19718-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="19718-112">Они по-прежнему включают прекращение null символов, однако.</span><span class="sxs-lookup"><span data-stu-id="19718-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="19718-113">Строки типа и адреса в  _записи электронного_ адреса разделены буквальной двоеточием (:) символ, например "smtp:joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="19718-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="19718-114">Только комбинированный **тип:** строка адресов не прекращается.</span><span class="sxs-lookup"><span data-stu-id="19718-114">Only the combined type **:** address string is null-terminated.</span></span>
  

