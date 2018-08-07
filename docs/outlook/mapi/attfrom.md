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
ms.openlocfilehash: c7c0d1df32a0ad6359fad20128a6a1e3dd225143
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808102"
---
# <a name="attfrom"></a><span data-ttu-id="ad8e1-103">attFrom</span><span class="sxs-lookup"><span data-stu-id="ad8e1-103">attFrom</span></span>

<span data-ttu-id="ad8e1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ad8e1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ad8e1-105">Атрибут **attFrom** закодирован **BIOS** структуру, которая кодирует отображаемое имя и адрес электронной почты адрес отправителя, следуют отображаемое имя и адрес отправителя, следуют любые необходимые внутренние поля.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-105">The **attFrom** attribute is encoded as a **TRP** structure which encodes the display name and email address of the sender, followed by the display name and address of the sender, followed by any necessary padding.</span></span> <span data-ttu-id="ad8e1-106">Формат для **attFrom** выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ad8e1-106">The format for **attFrom** is as follows:</span></span> 
  
<span data-ttu-id="ad8e1-107">**attFrom**: заполнение _ адрес отправителя отправителя отображаемое имя _ _Структура BIOS._</span><span class="sxs-lookup"><span data-stu-id="ad8e1-107">**attFrom**: _TRP-structure_ sender-display-name  _ sender-address _ padding</span></span> 
    
<span data-ttu-id="ad8e1-108">Отправитель отображаемое имя — строка символом null, заполняется дополнительные символ null, если это необходимо для связи с 2-байтовое границы.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-108">The sender-display-name is a null-terminated string that is padded with an additional null character, if necessary, to reach a 2-byte boundary.</span></span> <span data-ttu-id="ad8e1-109">Внутренние поля в конце кодирования **attFrom** состоит из числа символов null, чтобы сделать доступными **sizeof(TRP)** границы.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-109">The padding at the end of the **attFrom** encoding consists of as many null characters as needed to reach a **sizeof(TRP)** boundary.</span></span> 
  
<span data-ttu-id="ad8e1-110">_BIOS структура:_ Сертификация cch cbgrtrp **trpidOneOff**</span><span class="sxs-lookup"><span data-stu-id="ad8e1-110">_TRP-structure:_ **trpidOneOff** cbgrtrp cch cb</span></span> 
    
<span data-ttu-id="ad8e1-111">Для элемента **attFrom** **BIOS.**-Структура — это всегда одноразовых кодирования, поэтому trpid off **BIOS.**-поле структуры всегда является **trpidOneOff**.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-111">For the **attFrom** item, the **TRP**-structure is always a one-off encoding, so the trpid off the **TRP**-structure field is always **trpidOneOff**.</span></span> <span data-ttu-id="ad8e1-112">Cbgrtrp, cch и сертификация элементов соответствуют остальные поля структуры **BIOS.** .</span><span class="sxs-lookup"><span data-stu-id="ad8e1-112">The cbgrtrp, cch, and cb items correspond to the remaining fields of the **TRP** structure.</span></span> 
  
<span data-ttu-id="ad8e1-113">В поле cbgrtrp рассчитывается как сумма **(sizeof(TRP) \*2)**, длина символом null-display имя отправителя его заполнения и длина символом null адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-113">The cbgrtrp field is calculated as the sum of **(sizeof(TRP) \*2)**, the length of the null-terminated sender-display-name with its padding, and the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="ad8e1-114">В поле cch рассчитывается как длина символом null названия его заполнения.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-114">The cch field is calculated as the length of the null-terminated display-name with its padding.</span></span>
  
<span data-ttu-id="ad8e1-115">В поле сертификация рассчитывается как длина символом null адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-115">The cb field is calculated as the length of the null-terminated sender-address.</span></span>
  
<span data-ttu-id="ad8e1-116">_адрес отправителя:_ **:** адрес типа адреса **«\0»**</span><span class="sxs-lookup"><span data-stu-id="ad8e1-116">_sender-address:_ address-type **:** address **'\0'**</span></span>
    
<span data-ttu-id="ad8e1-117">Адрес отправителя — это строка, которая состоит из четырех частей, тип адреса, литерал двоеточие (:), сам по себе адрес и конечный символ null.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-117">The sender-address is a string that is composed of four parts, the address-type, a literal colon (:), the address itself, and a terminating null character.</span></span> <span data-ttu-id="ad8e1-118">Например, строка `fax:1-909-555-1234\0` может иметь значение юридический адрес отправителя.</span><span class="sxs-lookup"><span data-stu-id="ad8e1-118">For example, the string `fax:1-909-555-1234\0` would be a legal sender-address value.</span></span>
  

