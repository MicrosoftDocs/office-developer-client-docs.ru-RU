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
description: '���� ���������� ���������: 9 ����� 2015 �.'
ms.openlocfilehash: b94e1f2d66f89d680cc738968342de0fbcee5cda
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/15/2018
ms.locfileid: "19812047"
---
# <a name="pidtagwizardnopstpage-canonical-property"></a><span data-ttu-id="0d02c-103">Каноническое свойство PidTagWizardNoPstPage</span><span class="sxs-lookup"><span data-stu-id="0d02c-103">PidTagWizardNoPstPage Canonical Property</span></span>

  
  
<span data-ttu-id="0d02c-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="0d02c-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="0d02c-105">Это свойство содержит значение TRUE, если мастер профиля для отмены вывода страницы личное сообщение store (PST).</span><span class="sxs-lookup"><span data-stu-id="0d02c-105">This property contains TRUE if the profile wizard is to suppress the personal message store (PST) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="0d02c-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="0d02c-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="0d02c-107">PR_WIZARD_NO_PST_PAGE</span><span class="sxs-lookup"><span data-stu-id="0d02c-107">PR_WIZARD_NO_PST_PAGE</span></span>  <br/> |
|<span data-ttu-id="0d02c-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="0d02c-108">Identifier:</span></span>  <br/> |<span data-ttu-id="0d02c-109">0x6700</span><span class="sxs-lookup"><span data-stu-id="0d02c-109">0x6700</span></span>  <br/> |
|<span data-ttu-id="0d02c-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="0d02c-110">Data type:</span></span>  <br/> |<span data-ttu-id="0d02c-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="0d02c-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="0d02c-112">Области:</span><span class="sxs-lookup"><span data-stu-id="0d02c-112">Area:</span></span>  <br/> |<span data-ttu-id="0d02c-113">Администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="0d02c-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="0d02c-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="0d02c-114">Remarks</span></span>

<span data-ttu-id="0d02c-115">При вызове функции, основанной на прототип функции [LAUNCHWIZARDENTRY](launchwizardentry.md) этому свойству можно задать поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="0d02c-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="0d02c-116">Это свойство сообщает мастер профилей, что поставщик не нужно странице PST-файлов будет отображаться во время диалоговое окно user.</span><span class="sxs-lookup"><span data-stu-id="0d02c-116">This property tells the profile wizard that the provider does not want the PST page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="0d02c-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="0d02c-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="0d02c-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="0d02c-118">Header files</span></span>

<span data-ttu-id="0d02c-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="0d02c-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="0d02c-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="0d02c-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="0d02c-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="0d02c-121">Mapitags.h</span></span>
  
> <span data-ttu-id="0d02c-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="0d02c-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="0d02c-123">См. также</span><span class="sxs-lookup"><span data-stu-id="0d02c-123">See also</span></span>



[<span data-ttu-id="0d02c-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d02c-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="0d02c-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="0d02c-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="0d02c-126">Каноническое свойство имена сопоставляемых именам MAPI</span><span class="sxs-lookup"><span data-stu-id="0d02c-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="0d02c-127">Сопоставление имен MAPI имена каноническое свойств</span><span class="sxs-lookup"><span data-stu-id="0d02c-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

