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
ms.openlocfilehash: cdb7dde4853188eb0621dc3c2f45c2dc713441d3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22570242"
---
# <a name="pidtagwizardnopabpage-canonical-property"></a><span data-ttu-id="60339-103">Каноническое свойство PidTagWizardNoPabPage</span><span class="sxs-lookup"><span data-stu-id="60339-103">PidTagWizardNoPabPage Canonical Property</span></span>

  
  
<span data-ttu-id="60339-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="60339-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="60339-105">Это свойство содержит значение TRUE, если мастер профиля для отмены вывода страницы Личная адресная книга (адресной книги).</span><span class="sxs-lookup"><span data-stu-id="60339-105">This property contains TRUE if the profile wizard is to suppress the personal address book (PAB) page.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="60339-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="60339-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="60339-107">PR_WIZARD_NO_PAB_PAGE</span><span class="sxs-lookup"><span data-stu-id="60339-107">PR_WIZARD_NO_PAB_PAGE</span></span>  <br/> |
|<span data-ttu-id="60339-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="60339-108">Identifier:</span></span>  <br/> |<span data-ttu-id="60339-109">0x6701</span><span class="sxs-lookup"><span data-stu-id="60339-109">0x6701</span></span>  <br/> |
|<span data-ttu-id="60339-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="60339-110">Data type:</span></span>  <br/> |<span data-ttu-id="60339-111">PT_BOOLEAN</span><span class="sxs-lookup"><span data-stu-id="60339-111">PT_BOOLEAN</span></span>  <br/> |
|<span data-ttu-id="60339-112">Область:</span><span class="sxs-lookup"><span data-stu-id="60339-112">Area:</span></span>  <br/> |<span data-ttu-id="60339-113">Администрирования Exchange</span><span class="sxs-lookup"><span data-stu-id="60339-113">Exchange Administrative</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="60339-114">Замечания</span><span class="sxs-lookup"><span data-stu-id="60339-114">Remarks</span></span>

<span data-ttu-id="60339-115">При вызове функции, основанной на прототип функции [LAUNCHWIZARDENTRY](launchwizardentry.md) этому свойству можно задать поставщиков услуг.</span><span class="sxs-lookup"><span data-stu-id="60339-115">Service providers can set this property when calling a function based on the [LAUNCHWIZARDENTRY](launchwizardentry.md) function prototype.</span></span> <span data-ttu-id="60339-116">Это свойство сообщает мастер профилей, что поставщик не нужно странице адресной книги для отображения во время диалоговое окно user.</span><span class="sxs-lookup"><span data-stu-id="60339-116">This property tells the profile wizard that the provider does not want the PAB page to be displayed during the user dialog.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="60339-117">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="60339-117">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="60339-118">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="60339-118">Header files</span></span>

<span data-ttu-id="60339-119">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="60339-119">Mapidefs.h</span></span>
  
> <span data-ttu-id="60339-120">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="60339-120">Provides data type definitions.</span></span>
    
<span data-ttu-id="60339-121">Mapitags.h</span><span class="sxs-lookup"><span data-stu-id="60339-121">Mapitags.h</span></span>
  
> <span data-ttu-id="60339-122">Содержит определения свойств указано, что связанными свойствами.</span><span class="sxs-lookup"><span data-stu-id="60339-122">Contains definitions of properties listed as associated properties.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="60339-123">См. также</span><span class="sxs-lookup"><span data-stu-id="60339-123">See also</span></span>



[<span data-ttu-id="60339-124">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="60339-124">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="60339-125">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="60339-125">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="60339-126">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="60339-126">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="60339-127">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="60339-127">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

