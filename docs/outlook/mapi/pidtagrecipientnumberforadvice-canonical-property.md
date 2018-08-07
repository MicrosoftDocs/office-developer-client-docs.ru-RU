---
title: Каноническое свойство PidTagRecipientNumberForAdvice
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagRecipientNumberForAdvice
api_type:
- COM
ms.assetid: 636c1e75-3024-43ca-a7dd-1bb480dfbb5b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: ac4da2d4082cac632548594411528b7bf1d6dc64
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19811654"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="46ab6-103">Каноническое свойство PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="46ab6-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="46ab6-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="46ab6-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="46ab6-105">Это свойство содержит получателя сообщения телефонного номера для звонка информацией о физической доставки сообщения.</span><span class="sxs-lookup"><span data-stu-id="46ab6-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="46ab6-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="46ab6-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="46ab6-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="46ab6-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="46ab6-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="46ab6-108">Identifier:</span></span>  <br/> |<span data-ttu-id="46ab6-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="46ab6-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="46ab6-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="46ab6-110">Data type:</span></span>  <br/> |<span data-ttu-id="46ab6-111">PT_STRING8 PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="46ab6-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="46ab6-112">Область:</span><span class="sxs-lookup"><span data-stu-id="46ab6-112">Area:</span></span>  <br/> |<span data-ttu-id="46ab6-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="46ab6-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="46ab6-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="46ab6-114">Remarks</span></span>

<span data-ttu-id="46ab6-115">Эти свойства предназначены для использования в сочетании с доставки физических назначения, а не электронный почтовый ящик, когда человеческого получателя не должен быть указан в доставке.</span><span class="sxs-lookup"><span data-stu-id="46ab6-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="46ab6-116">Например, номер телефона на лист обложка факса.</span><span class="sxs-lookup"><span data-stu-id="46ab6-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="46ab6-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="46ab6-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="46ab6-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="46ab6-118">Header files</span></span>

<span data-ttu-id="46ab6-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="46ab6-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="46ab6-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="46ab6-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="46ab6-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="46ab6-121">Mapitags.h</span></span>
  
> <span data-ttu-id="46ab6-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="46ab6-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="46ab6-123">См. также</span><span class="sxs-lookup"><span data-stu-id="46ab6-123">See also</span></span>



[<span data-ttu-id="46ab6-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="46ab6-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="46ab6-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="46ab6-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="46ab6-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="46ab6-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="46ab6-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="46ab6-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

