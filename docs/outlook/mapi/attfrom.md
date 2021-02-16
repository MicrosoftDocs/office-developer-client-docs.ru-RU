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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33432417"
---
# <a name="attfrom"></a><span data-ttu-id="677ca-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="677ca-103">attFrom</span></span>

<span data-ttu-id="677ca-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="677ca-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="677ca-105">Атрибут **attFrom** закодирован как структура **TRP,** которая кодирует отображаемую и адрес электронной почты отправитель, а затем отображаемую и адрес отправитель, а затем все необходимые заполнения.</span><span class="sxs-lookup"><span data-stu-id="677ca-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="677ca-106">Формат **attFrom:**</span><span class="sxs-lookup"><span data-stu-id="677ca-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="677ca-107">**attFrom**: _sender-display-name_ _sender-address _padding в структуре TRP</span><span class="sxs-lookup"><span data-stu-id="677ca-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="677ca-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span><span class="sxs-lookup"><span data-stu-id="677ca-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="677ca-109">Заполнение в конце кодиру **attFrom** состоит из максимального объема символов null, необходимого для достижения границы **sizeof(TRP).**</span><span class="sxs-lookup"><span data-stu-id="677ca-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="677ca-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span><span class="sxs-lookup"><span data-stu-id="677ca-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="677ca-111">Для **элемента attFrom** структура **TRP** всегда является однофазной кодирой, поэтому в качестве trpid от поля структуры **TRP** всегда является **trpidOneOff.**</span><span class="sxs-lookup"><span data-stu-id="677ca-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="677ca-112">Элементы cbgrtrp, cch и cb соответствуют оставшимся полям структуры **TRP.**</span><span class="sxs-lookup"><span data-stu-id="677ca-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="677ca-113">Поле cbgrtrp вычисляется как сумма **(sizeof(TRP) \* 2),** длина нулевого имени sender-display-name с его заполнением и длина завершаемого null адреса отправитель.</span><span class="sxs-lookup"><span data-stu-id="677ca-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="677ca-114">Поле cch вычисляется как длина отображаемого имени, о завершаемого null, с его заполнением.</span><span class="sxs-lookup"><span data-stu-id="677ca-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="677ca-115">Поле cb вычисляется как длина завершаемого null-адреса отправитель.</span><span class="sxs-lookup"><span data-stu-id="677ca-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="677ca-116">_sender-address:_ address-type **:** address **'\0'**</span><span class="sxs-lookup"><span data-stu-id="677ca-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="677ca-117">Адрес отправитель — это строка, состоящая из четырех частей: типа адреса, литерального двоеточия (:), самого адреса и завершающих символов null.</span><span class="sxs-lookup"><span data-stu-id="677ca-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="677ca-118">Например, строка `fax:1-909-555-1234\0` будет иметь юридическое значение адреса отправитель.</span><span class="sxs-lookup"><span data-stu-id="677ca-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

