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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318118"
---
# <a name="attsentfor"></a><span data-ttu-id="daacd-103">attSentFor</span><span class="sxs-lookup"><span data-stu-id="daacd-103">attSentFor</span></span>

  
  
<span data-ttu-id="daacd-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="daacd-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="daacd-105">Атрибут **аттсентфор** кодируется в виде строк, подсчитанных до конца.</span><span class="sxs-lookup"><span data-stu-id="daacd-105">The **attSentFor** attribute is encoded as counted strings laid end-to-end.</span></span> <span data-ttu-id="daacd-106">Формат для **аттсентфор** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="daacd-106">The format for **attSentFor** is as follows:</span></span> 
  
 <span data-ttu-id="daacd-107">**аттсентфор**:</span><span class="sxs-lookup"><span data-stu-id="daacd-107">**attSentFor**:</span></span> 
  
> <span data-ttu-id="daacd-108">Display — имя — длина отображаемого имени, адрес _электронной почты_ , длина адреса</span><span class="sxs-lookup"><span data-stu-id="daacd-108">display-name-length display-name address-length  _email-address_</span></span>
    
 <span data-ttu-id="daacd-109">_адрес электронной почты_</span><span class="sxs-lookup"><span data-stu-id="daacd-109">_email-address_</span></span>
  
> <span data-ttu-id="daacd-110">Тип **:** Address</span><span class="sxs-lookup"><span data-stu-id="daacd-110">type **:** address</span></span> 
    
<span data-ttu-id="daacd-111">В отличие от других значений длины, отображаемое имя и длина адреса — это 16 – битовые значения без знака, а не длинные целые числа без знака.</span><span class="sxs-lookup"><span data-stu-id="daacd-111">Unlike other length values, the display-name-length and address-length are unsigned 16-bit values instead of unsigned long integers.</span></span> <span data-ttu-id="daacd-112">Тем не менее, они по-прежнему содержат завершающие символы NULL.</span><span class="sxs-lookup"><span data-stu-id="daacd-112">They still include terminating null characters, however.</span></span> <span data-ttu-id="daacd-113">Строки Type и Address в записи _адреса электронной почты_ разделяются с помощью литерального двоеточия (:) символ, например "SMTP:Joe@nowhere.com".</span><span class="sxs-lookup"><span data-stu-id="daacd-113">The type and address strings in the  _email-address_ entry are separated by a literal colon (:) character, such as "smtp:joe@nowhere.com".</span></span> <span data-ttu-id="daacd-114">Только объединенный тип **:** строка адреса завершается нулем.</span><span class="sxs-lookup"><span data-stu-id="daacd-114">Only the combined type **:** address string is null-terminated.</span></span>
  

