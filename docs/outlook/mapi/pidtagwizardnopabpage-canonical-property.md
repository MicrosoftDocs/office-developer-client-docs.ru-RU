---
title: Каноническое свойство PidTagWizardNoPabPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPabPage
api_type:
- COM
ms.assetid: 9cec22cd-798d-41f6-9ebd-c7354f2162c2
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: fc971be76dbaa83176f207411f9f125ffee386cf
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33424464"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a><span data-ttu-id="e9366-103">Каноническое свойство PidTagWizardNoPabPage</span><span class="sxs-lookup"><span data-stu-id="e9366-103">PidTagWizardNoPabPage Canonical Property</span></span>

  
  
<span data-ttu-id="e9366-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e9366-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e9366-105">Это свойство содержит TRUE, если мастер профиля должен подавить страницу личной адресной книги (PAB).</span><span class="sxs-lookup"><span data-stu-id="e9366-105">This property contains TRUE if the profile wizard is to suppress the personal address book (PAB) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="e9366-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="e9366-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="e9366-107">PR_WIZARD_NO_PAB_PAGE</span><span class="sxs-lookup"><span data-stu-id="e9366-107">PR_WIZARD_NO_PAB_PAGE</span></span>  <br/> |
|<span data-ttu-id="e9366-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="e9366-108">Identifier:</span></span>  <br/> |<span data-ttu-id="e9366-109">0x6701</span><span class="sxs-lookup"><span data-stu-id="e9366-109">0x6701</span></span>  <br/> |
|<span data-ttu-id="e9366-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="e9366-110">Data type:</span></span>  <br/> |<span data-ttu-id="e9366-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="e9366-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="e9366-112">Область:</span><span class="sxs-lookup"><span data-stu-id="e9366-112">Area:</span></span>  <br/> |<span data-ttu-id="e9366-113">Exchange Администрирование</span><span class="sxs-lookup"><span data-stu-id="e9366-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="e9366-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="e9366-114">Remarks</span></span>

<span data-ttu-id="e9366-115">Поставщики услуг могут установить это свойство при вызове функции на основе прототипа функции [LAUNCHWIZARDENTRY.](launchwizardentry.md)</span><span class="sxs-lookup"><span data-stu-id="e9366-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="e9366-116">Это свойство сообщает мастеру профиля, что поставщик не хочет, чтобы страница PAB отображалась во время диалогов пользователя.</span><span class="sxs-lookup"><span data-stu-id="e9366-116">This property tells the profile wizard that the provider does not want the PAB page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="e9366-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="e9366-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="e9366-118">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="e9366-118">Header files</span></span>

<span data-ttu-id="e9366-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="e9366-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="e9366-120">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="e9366-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="e9366-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="e9366-121">Mapitags.h</span></span>
  
> <span data-ttu-id="e9366-122">Содержит определения свойств, перечисленных в качестве связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="e9366-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="e9366-123">См. также</span><span class="sxs-lookup"><span data-stu-id="e9366-123">See also</span></span>



[<span data-ttu-id="e9366-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9366-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="e9366-125">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="e9366-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="e9366-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="e9366-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="e9366-127">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="e9366-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

