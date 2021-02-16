---
title: Корреляция TNEF в шлюзах и транспортах X.400
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
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="cf7c7-103">Корреляция TNEF в шлюзах и транспортах X.400</span><span class="sxs-lookup"><span data-stu-id="cf7c7-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="cf7c7-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="cf7c7-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="cf7c7-105">Шлюзы и транспортные средства, которые подключаются к системам на основе X.400, используют значение атрибута IM_THIS_IPM X.400 и **атрибута attMessageID** TNEF для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="cf7c7-106">Значение атрибута IM_THIS_IPM исходящие сообщения копируется в **attMessageID** в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="cf7c7-107">Атрибут IM_THIS_IPM X.400 обычно представляет собой строку, а атрибут **attMessageID** TNEF — это строка из hexadecimal digits, представляющая двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="cf7c7-108">Поэтому каждый символ в атрибуте IM_THIS_IPM X.400, включая завершающий символ null, необходимо преобразовать в 2-символьную строку, представляющую значение ASCII этого символа.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="cf7c7-109">Например, если атрибут IM_THIS_IPM X.400 является следующей строкой:</span><span class="sxs-lookup"><span data-stu-id="cf7c7-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="cf7c7-110">3030322D3030312D305337533A3936303631312D31353337303030</span><span class="sxs-lookup"><span data-stu-id="cf7c7-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="cf7c7-111">затем **значением attMessageID** будет следующая последовательность шестью цифрами:</span><span class="sxs-lookup"><span data-stu-id="cf7c7-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="cf7c7-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="cf7c7-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="cf7c7-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="cf7c7-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="cf7c7-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="cf7c7-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="cf7c7-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="cf7c7-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="cf7c7-116">33 30 33 36 33 31 33 31</span><span class="sxs-lookup"><span data-stu-id="cf7c7-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="cf7c7-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="cf7c7-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="cf7c7-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="cf7c7-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="cf7c7-119">Этот метод используется соединитетелем Microsoft Exchange Server X.400.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="cf7c7-120">Этот метод должен использоваться любыми шлюзами и транспортными средствами X.400, которые подключаются к Microsoft Exchange Server для максимального обеспечения максимальной производительности.</span><span class="sxs-lookup"><span data-stu-id="cf7c7-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="cf7c7-121">Для обеспечения максимальной совместимости с будущим и представленным программным обеспечением Майкрософт атрибут IM_THIS_IPM X.400 также следует скопировать в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey).](pidtagtnefcorrelationkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="cf7c7-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="cf7c7-122">Однако поскольку **PR_TNEF_CORRELATION_KEY** является двоичным свойством, нет необходимости в переводе в строку-</span><span class="sxs-lookup"><span data-stu-id="cf7c7-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

