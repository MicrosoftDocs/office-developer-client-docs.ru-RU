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
# <a name="attowner"></a><span data-ttu-id="eb541-103">attOwner</span><span class="sxs-lookup"><span data-stu-id="eb541-103">attOwner</span></span>

  
  
<span data-ttu-id="eb541-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="eb541-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="eb541-105">Атрибут **аттовнер** кодируется в виде строк, подсчитанных до конца.</span><span class="sxs-lookup"><span data-stu-id="eb541-105">The **attOwner** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="eb541-106">Формат для **аттовнер** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="eb541-106">The format for **attOwner** is as follows:</span></span> 
  
 <span data-ttu-id="eb541-107">**аттовнер**:</span><span class="sxs-lookup"><span data-stu-id="eb541-107">**attOwner**:</span></span> 
  
> <span data-ttu-id="eb541-108">Display — имя — длина отображаемого имени, адрес _электронной почты_ , длина адреса</span><span class="sxs-lookup"><span data-stu-id="eb541-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="eb541-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="eb541-109">_email-address_</span></span>
  
> <span data-ttu-id="eb541-110">Тип **:** Address</span><span class="sxs-lookup"><span data-stu-id="eb541-110">type **:** address</span></span> 
    
<span data-ttu-id="eb541-111">В отличие от других значений длины, отображаемое имя и длина адреса — это 16 – битовые значения без знака, а не длинные целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="eb541-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="eb541-112">Тем не менее, они по-прежнему содержат завершающие символы NULL.</span><span class="sxs-lookup"><span data-stu-id="eb541-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="eb541-113">Строки Type и Address в записи _адреса электронной почты_ разделяются с помощью литерального двоеточия (:) символ, например "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="eb541-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="eb541-114">Только объединенный тип **:** строка адреса завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="eb541-114">Only the combined type **:** address string is null-terminated.</span></span>
  
<span data-ttu-id="eb541-115">Сопоставление свойств MAPI с атрибутом **аттовнер** зависит от класса Message закодированного сообщения.</span><span class="sxs-lookup"><span data-stu-id="eb541-115">The mapping of MAPI properties to the **attOwner** attribute is dependent on the message class of the message being encoded.</span></span> 
  

