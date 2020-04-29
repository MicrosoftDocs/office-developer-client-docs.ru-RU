---
title: Корреляция TNEF в шлюзах и транспортах X. 400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e08f16ff60a282f1be3adf93d858471e38d19957
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33406376"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="b0e07-103">Корреляция TNEF в шлюзах и транспортах X. 400</span><span class="sxs-lookup"><span data-stu-id="b0e07-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="b0e07-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b0e07-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b0e07-105">Шлюзы и транспорты, которые подключаются к системам X. 400, используют значение атрибута IM_THIS_IPM X. 400 и атрибут TNEF **аттмессажеид** для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="b0e07-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="b0e07-106">Значение атрибута IM_THIS_IPM исходящих сообщений копируется в **аттмессажеид** в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="b0e07-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="b0e07-107">IM_THIS_IPM X. 400 — это, как правило, строка, а атрибут TNEF **аттмессажеид** — это строка шестнадцатеричных цифр, представляющих двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="b0e07-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="b0e07-108">Таким образом, каждый символ в атрибуте IM_THIS_IPM X. 400, включая завершающий символ null, должен быть преобразован в шестнадцатеричную строку из 2 символов, представляющую значение ASCII этого символа.</span><span class="sxs-lookup"><span data-stu-id="b0e07-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="b0e07-109">Например, если IM_THIS_IPM X. 400 атрибут имеет следующую строку:</span><span class="sxs-lookup"><span data-stu-id="b0e07-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="b0e07-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="b0e07-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="b0e07-111">тогда значение **аттмессажеид** будет равно следующей последовательности шестнадцатеричных цифр:</span><span class="sxs-lookup"><span data-stu-id="b0e07-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="b0e07-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="b0e07-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="b0e07-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="b0e07-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="b0e07-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="b0e07-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="b0e07-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="b0e07-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="b0e07-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="b0e07-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="b0e07-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="b0e07-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="b0e07-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="b0e07-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="b0e07-119">Этот метод используется соединителем Microsoft Exchange Server X. 400.</span><span class="sxs-lookup"><span data-stu-id="b0e07-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="b0e07-120">Этот способ должен использоваться любыми шлюзами и транспортами X. 400, которые подключаются к серверу Microsoft Exchange Server для обеспечения максимальной совместимости.</span><span class="sxs-lookup"><span data-stu-id="b0e07-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="b0e07-121">Для обеспечения лучшей совместимости с будущими и будущими версиями программного обеспечения Майкрософт атрибут IM_THIS_IPM X. 400 также должен быть скопирован в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="b0e07-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="b0e07-122">Однако, так как **PR_TNEF_CORRELATION_KEY** является двоичным свойством, не требуется перевод в шестнадцатеричную строку.</span><span class="sxs-lookup"><span data-stu-id="b0e07-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

