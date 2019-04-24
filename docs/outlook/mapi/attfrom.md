---
title: attFrom
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 2d405268-bb33-4863-be38-2d17e8fc956e
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 496bd5439b9f004d3b13d2d73b31b5cac3f9eec9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32318160"
---
# <a name="attfrom"></a><span data-ttu-id="d46c4-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="d46c4-103">attFrom</span></span>

<span data-ttu-id="d46c4-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="d46c4-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="d46c4-105">Атрибут **аттфром** кодируется как структура **ТРП** , которая кодирует отображаемое имя и адрес электронной почты отправителя, а также отображаемое имя и адрес отправителя, за которым следуют все необходимые поля.</span><span class="sxs-lookup"><span data-stu-id="d46c4-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="d46c4-106">Формат для **аттфром** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="d46c4-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="d46c4-107">**аттфром**: _ТРП — структура_ отправителя — отображаемое имя _ sender/Address _ Padding</span><span class="sxs-lookup"><span data-stu-id="d46c4-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="d46c4-108">Sender-Display-Name — это строка с завершающим нулем, дополненная дополнительным нулевым символом (при необходимости) для достижения границы 2 байта.</span><span class="sxs-lookup"><span data-stu-id="d46c4-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="d46c4-109">Заполнение в конце кодировки **аттфром** состоит из количества символов NULL, необходимых для достижения границы **sizeof (ТРП)** .</span><span class="sxs-lookup"><span data-stu-id="d46c4-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="d46c4-110">_ТРП — структура:_ **трпидонеофф** кбгртрп Кч CB</span><span class="sxs-lookup"><span data-stu-id="d46c4-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="d46c4-111">Для элемента **Аттфром** **ТРП**-Structure всегда является одноразовым кодированием, поэтому трпид в поле **ТРП**структуры всегда является **трпидонеофф**.</span><span class="sxs-lookup"><span data-stu-id="d46c4-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="d46c4-112">Элементы кбгртрп, Кч и CB соответствуют оставшимся полям структуры **ТРП** .</span><span class="sxs-lookup"><span data-stu-id="d46c4-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="d46c4-113">Поле кбгртрп вычисляется как сумма **(sizeof (ТРП \*) 2)**, длина отправителя, заканчивающаяся нулем, с заполнением и длиной отправителя, заканчивающейся нулем.</span><span class="sxs-lookup"><span data-stu-id="d46c4-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="d46c4-114">Поле Кч рассчитывается как длина отображаемого имени, заканчивающегося нулем, с заполнением.</span><span class="sxs-lookup"><span data-stu-id="d46c4-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="d46c4-115">Поле CB рассчитывается как длина адреса отправителя, заканчивающегося нулем.</span><span class="sxs-lookup"><span data-stu-id="d46c4-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="d46c4-116">_адрес отправителя:_ адрес — тип **:** адрес **"\ 0"**</span><span class="sxs-lookup"><span data-stu-id="d46c4-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="d46c4-117">Адрес отправителя — это строка, состоящая из четырех частей, типа Address, литерала двоеточия (:), самого адреса и завершающего null-символа.</span><span class="sxs-lookup"><span data-stu-id="d46c4-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="d46c4-118">Например, строка `fax:1-909-555-1234\0` будет иметь допустимый адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="d46c4-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

