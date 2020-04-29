---
title: Каноническое свойство PidTagWizardNoPstPage
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- MAPI.PidTagWizardNoPstPage
api_type:
- COM
ms.assetid: 1ac09578-892b-4c72-92f6-c2419ac2efe8
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: e816af2ce60b4c06ae14f720cf7c36d58468d09d
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422889"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="52c48-103">Каноническое свойство PidTagWizardNoPstPage</span><span class="sxs-lookup"><span data-stu-id="52c48-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="52c48-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="52c48-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="52c48-105">Это свойство содержит значение TRUE, если мастер профилей запрещает отдавление со страницы PST-хранилища личных сообщений.</span><span class="sxs-lookup"><span data-stu-id="52c48-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="52c48-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="52c48-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="52c48-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="52c48-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="52c48-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="52c48-108">Identifier:</span></span>  <br/> |<span data-ttu-id="52c48-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="52c48-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="52c48-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="52c48-110">Data type:</span></span>  <br/> |<span data-ttu-id="52c48-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="52c48-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="52c48-112">Область:</span><span class="sxs-lookup"><span data-stu-id="52c48-112">Area:</span></span>  <br/> |<span data-ttu-id="52c48-113">Административная служба Exchange</span><span class="sxs-lookup"><span data-stu-id="52c48-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="52c48-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="52c48-114">Remarks</span></span>

<span data-ttu-id="52c48-115">Поставщики услуг могут задать это свойство при вызове функции на основе прототипа функции [лаунчвизардентри](launchwizardentry.md) .</span><span class="sxs-lookup"><span data-stu-id="52c48-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="52c48-116">Это свойство сообщает мастеру профилей, что поставщик не хочет, чтобы страница PST отображалась в диалоговом окне пользователя.</span><span class="sxs-lookup"><span data-stu-id="52c48-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="52c48-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="52c48-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="52c48-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="52c48-118">Header files</span></span>

<span data-ttu-id="52c48-119">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="52c48-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="52c48-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="52c48-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="52c48-121">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="52c48-121">Mapitags.h</span></span>
  
> <span data-ttu-id="52c48-122">Содержит определения свойств, перечисленных как связанные свойства.</span><span class="sxs-lookup"><span data-stu-id="52c48-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="52c48-123">См. также</span><span class="sxs-lookup"><span data-stu-id="52c48-123">See also</span></span>



[<span data-ttu-id="52c48-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="52c48-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="52c48-125">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="52c48-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="52c48-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="52c48-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="52c48-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="52c48-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

