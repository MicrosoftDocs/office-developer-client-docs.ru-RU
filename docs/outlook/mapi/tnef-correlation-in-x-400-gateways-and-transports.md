---
title: Корреляция TNEF в операциях транспорта и шлюзах X.400
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 0ffa0802-bfdd-4993-b4a3-142e5d15bfb4
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 297fff3482a4b7aea391c3e1869cd127cc49cad2
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22566819"
---
# <a name="tnef-correlation-in-x400-gateways-and-transports"></a><span data-ttu-id="03ac1-103">Корреляция TNEF в операциях транспорта и шлюзах X.400</span><span class="sxs-lookup"><span data-stu-id="03ac1-103">TNEF Correlation in X.400 Gateways and Transports</span></span>

  
  
<span data-ttu-id="03ac1-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="03ac1-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="03ac1-105">Шлюзы и транспортов, обеспечивающих возможности подключения для компьютеров на базе X.400, используйте значение атрибутов IM_THIS_IPM X.400 и **attMessageID** TNEF для реализации корреляции TNEF.</span><span class="sxs-lookup"><span data-stu-id="03ac1-105">Gateways and transports that connect to X.400-based systems, use the value of the IM_THIS_IPM X.400 attribute and the **attMessageID** TNEF attribute to implement TNEF correlation.</span></span> 
  
<span data-ttu-id="03ac1-106">Значение атрибута IM_THIS_IPM исходящие сообщения копируется **attMessageID** в потоке TNEF.</span><span class="sxs-lookup"><span data-stu-id="03ac1-106">The value of the IM_THIS_IPM attribute of the outbound message is copied to **attMessageID** in the TNEF stream.</span></span> <span data-ttu-id="03ac1-107">Атрибут IM_THIS_IPM X.400 обычно — это строка, а атрибут TNEF **attMessageID** — это строка шестнадцатеричных цифр, представляющих двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="03ac1-107">The IM_THIS_IPM X.400 attribute is typically a string, while the **attMessageID** TNEF attribute is a string of hexadecimal digits representing a binary value.</span></span> <span data-ttu-id="03ac1-108">Таким образом каждый символ в качестве атрибута IM_THIS_IPM X.400, включая символ null, должны быть преобразованы в 2-значный шестнадцатеричную строку, представляющее значение ASCII символа.</span><span class="sxs-lookup"><span data-stu-id="03ac1-108">Therefore, each character in the IM_THIS_IPM X.400 attribute, including the terminating null character, must be converted to a 2-character hexadecimal string representing the ASCII value of that character.</span></span> <span data-ttu-id="03ac1-109">Например если атрибут IM_THIS_IPM X.400 имеет следующую строку:</span><span class="sxs-lookup"><span data-stu-id="03ac1-109">For instance, if the IM_THIS_IPM X.400 attribute is the following string:</span></span> 
  
<span data-ttu-id="03ac1-110">3030322D3030312D305337533A3A3936303631312D313533373030</span><span class="sxs-lookup"><span data-stu-id="03ac1-110">3030322D3030312D305337533A3A3936303631312D313533373030</span></span>
  
<span data-ttu-id="03ac1-111">Выберите значение **attMessageID** должно быть следующую последовательность шестнадцатеричных цифр:</span><span class="sxs-lookup"><span data-stu-id="03ac1-111">then the value of **attMessageID** would be the following sequence of hexadecimal digits:</span></span> 
  
<span data-ttu-id="03ac1-112">33 30 33 30 33 32 32 44</span><span class="sxs-lookup"><span data-stu-id="03ac1-112">33 30 33 30 33 32 32 44</span></span>
  
<span data-ttu-id="03ac1-113">33 30 33 30 33 31 32 44</span><span class="sxs-lookup"><span data-stu-id="03ac1-113">33 30 33 30 33 31 32 44</span></span>
  
<span data-ttu-id="03ac1-114">33 30 35 33 33 37 35 33</span><span class="sxs-lookup"><span data-stu-id="03ac1-114">33 30 35 33 33 37 35 33</span></span>
  
<span data-ttu-id="03ac1-115">33 41 33 41 33 39 33 36</span><span class="sxs-lookup"><span data-stu-id="03ac1-115">33 41 33 41 33 39 33 36</span></span>
  
<span data-ttu-id="03ac1-116">33 30 33 36 33 33 31 31</span><span class="sxs-lookup"><span data-stu-id="03ac1-116">33 30 33 36 33 31 33 31</span></span>
  
<span data-ttu-id="03ac1-117">32 44 33 31 33 35 33 33</span><span class="sxs-lookup"><span data-stu-id="03ac1-117">32 44 33 31 33 35 33 33</span></span>
  
<span data-ttu-id="03ac1-118">33 37 33 30 33 30 00</span><span class="sxs-lookup"><span data-stu-id="03ac1-118">33 37 33 30 33 30 00</span></span>
  
<span data-ttu-id="03ac1-119">Этот метод используется соединитель X.400 Microsoft Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="03ac1-119">This technique is used by the Microsoft Exchange Server X.400 Connector.</span></span> <span data-ttu-id="03ac1-120">Этот метод можно использовать с любой X.400 шлюзов и транспортов, подключение к Microsoft Exchange Server для обеспечения максимальной взаимодействия.</span><span class="sxs-lookup"><span data-stu-id="03ac1-120">This technique should be used by any X.400 gateways and transports that connect to Microsoft Exchange Server in order to maximize interoperability.</span></span>
  
<span data-ttu-id="03ac1-121">Для полной совместимости с будущими, а также присутствует программного обеспечения корпорации Майкрософт атрибут IM_THIS_IPM X.400 необходимо копировать в свойство **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="03ac1-121">For greatest compatibility with future as well as present Microsoft software, the IM_THIS_IPM X.400 attribute should also be copied to the **PR_TNEF_CORRELATION_KEY** ([PidTagTnefCorrelationKey](pidtagtnefcorrelationkey-canonical-property.md)) property.</span></span> <span data-ttu-id="03ac1-122">Тем не менее так как **PR_TNEF_CORRELATION_KEY** двоичного свойства, не переводом шестнадцатеричную строку не требуется.</span><span class="sxs-lookup"><span data-stu-id="03ac1-122">However, since **PR_TNEF_CORRELATION_KEY** is a binary property, no translation into a hexadecimal string is necessary.</span></span> 
  

