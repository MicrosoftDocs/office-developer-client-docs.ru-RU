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
ms.openlocfilehash: 79ef85955f15e0ca829ac6f206dddc17031b0562
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33420642"
---
# <a name="pidtagrecipientnumberforadvice-canonical-property"></a><span data-ttu-id="6d356-103">Каноническое свойство PidTagRecipientNumberForAdvice</span><span class="sxs-lookup"><span data-stu-id="6d356-103">PidTagRecipientNumberForAdvice Canonical Property</span></span>

  
  
<span data-ttu-id="6d356-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="6d356-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="6d356-105">Это свойство содержит телефонный номер получателя сообщения для вызова, чтобы сообщить о физической доставке сообщения.</span><span class="sxs-lookup"><span data-stu-id="6d356-105">This property contains a message recipient's telephone number to call to advise of the physical delivery of a message.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="6d356-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="6d356-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="6d356-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span><span class="sxs-lookup"><span data-stu-id="6d356-107">PR_RECIPIENT_NUMBER_FOR_ADVICE, PR_RECIPIENT_NUMBER_FOR_ADVICE_A, PR_RECIPIENT_NUMBER_FOR_ADVICE_W</span></span>  <br/> |
|<span data-ttu-id="6d356-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="6d356-108">Identifier:</span></span>  <br/> |<span data-ttu-id="6d356-109">0x0C14</span><span class="sxs-lookup"><span data-stu-id="6d356-109">0x0C14</span></span>  <br/> |
|<span data-ttu-id="6d356-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="6d356-110">Data type:</span></span>  <br/> |<span data-ttu-id="6d356-111">PT_STRING8, PT_UNICODE</span><span class="sxs-lookup"><span data-stu-id="6d356-111">PT_STRING8, PT_UNICODE</span></span>  <br/> |
|<span data-ttu-id="6d356-112">Область:</span><span class="sxs-lookup"><span data-stu-id="6d356-112">Area:</span></span>  <br/> |<span data-ttu-id="6d356-113">Получатель MAPI</span><span class="sxs-lookup"><span data-stu-id="6d356-113">MAPI Recipient</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="6d356-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="6d356-114">Remarks</span></span>

<span data-ttu-id="6d356-115">Эти свойства предназначены для использования в сочетании с доставкой в физическое место назначения, а не в электронный почтовый ящик, если получатель не должен присутствовать при доставке.</span><span class="sxs-lookup"><span data-stu-id="6d356-115">These properties are meant to be used in conjunction with delivery to a physical destination, rather than an electronic mailbox, when the human recipient is not expected to be present at delivery.</span></span> <span data-ttu-id="6d356-116">В качестве примера можно привести номер телефона на листе факс-связи.</span><span class="sxs-lookup"><span data-stu-id="6d356-116">An example is the telephone number on a fax cover sheet.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="6d356-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="6d356-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="6d356-118">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="6d356-118">Header files</span></span>

<span data-ttu-id="6d356-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="6d356-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="6d356-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="6d356-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="6d356-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="6d356-121">Mapitags.h</span></span>
  
> <span data-ttu-id="6d356-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="6d356-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="6d356-123">См. также</span><span class="sxs-lookup"><span data-stu-id="6d356-123">See also</span></span>



[<span data-ttu-id="6d356-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d356-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="6d356-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="6d356-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="6d356-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="6d356-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="6d356-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="6d356-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

