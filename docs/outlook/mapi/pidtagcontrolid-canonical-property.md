---
title: Каноническое свойство PidTagControlId
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidTagControlId
api_type:
- HeaderDef
ms.assetid: 281bc3e0-7c69-461b-bf09-4281abbb5e1b
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: b27f59e0bfdcac8eca1751af2f07139f12e2b3a7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33416022"
---
# <a name="pidtagcontrolid-canonical-property"></a><span data-ttu-id="de566-103">Каноническое свойство PidTagControlId</span><span class="sxs-lookup"><span data-stu-id="de566-103">PidTagControlId Canonical Property</span></span>

  
  
<span data-ttu-id="de566-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="de566-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="de566-105">Содержит уникальный идентификатор элемента управления, используемого в диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="de566-105">Contains a unique identifier for a control used in a dialog box.</span></span> 
  
|||
|:-----|:-----|
|<span data-ttu-id="de566-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="de566-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="de566-107">PR_CONTROL_ID</span><span class="sxs-lookup"><span data-stu-id="de566-107">PR_CONTROL_ID</span></span>  <br/> |
|<span data-ttu-id="de566-108">Идентификатор:</span><span class="sxs-lookup"><span data-stu-id="de566-108">Identifier:</span></span>  <br/> |<span data-ttu-id="de566-109">0x3F07</span><span class="sxs-lookup"><span data-stu-id="de566-109">0x3F07</span></span>  <br/> |
|<span data-ttu-id="de566-110">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="de566-110">Data type:</span></span>  <br/> |<span data-ttu-id="de566-111">PT_BINARY</span><span class="sxs-lookup"><span data-stu-id="de566-111">PT_BINARY</span></span>  <br/> |
|<span data-ttu-id="de566-112">Область:</span><span class="sxs-lookup"><span data-stu-id="de566-112">Area:</span></span>  <br/> |<span data-ttu-id="de566-113">Таблица отображения MAPI</span><span class="sxs-lookup"><span data-stu-id="de566-113">MAPI display table</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="de566-114">Примечания</span><span class="sxs-lookup"><span data-stu-id="de566-114">Remarks</span></span>

<span data-ttu-id="de566-115">Это свойство содержит уникальный идентификатор для элемента управления.</span><span class="sxs-lookup"><span data-stu-id="de566-115">This property contains a unique identifier for the control.</span></span> <span data-ttu-id="de566-116">Этот идентификатор должен содержать структуру [GUID](guid.md) и двоичное значение типа **Long**.</span><span class="sxs-lookup"><span data-stu-id="de566-116">This identifier should contain a [GUID](guid.md) structure and a binary value of type **LONG**.</span></span> <span data-ttu-id="de566-117">Все элементы управления в диалоговом окне должны использовать один **GUID** для идентификации поставщика услуг, а каждый элемент управления должен использовать уникальное **длинное** значение, чтобы избежать конфликта элементов управления.</span><span class="sxs-lookup"><span data-stu-id="de566-117">All controls in the dialog box should use the same **GUID** to identify the service provider, and each control should use a unique **LONG** value to ensure that the controls do not collide.</span></span> 
  
<span data-ttu-id="de566-118">Это свойство используется в уведомлениях.</span><span class="sxs-lookup"><span data-stu-id="de566-118">This property is used in notifications.</span></span> <span data-ttu-id="de566-119">Например, уведомления, отправляемые в таблице отображения, должны задавать это свойство, чтобы уникальным образом определить обновляемый элемент управления.</span><span class="sxs-lookup"><span data-stu-id="de566-119">For example, notifications sent on the display table must set this property to uniquely identify the control to update.</span></span> 
  
## <a name="related-resources"></a><span data-ttu-id="de566-120">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="de566-120">Related resources</span></span>

### <a name="header-files"></a><span data-ttu-id="de566-121">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="de566-121">Header files</span></span>

<span data-ttu-id="de566-122">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="de566-122">Mapidefs.h</span></span>
  
> <span data-ttu-id="de566-123">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="de566-123">Provides data type definitions.</span></span>
    
<span data-ttu-id="de566-124">Мапитагс. h</span><span class="sxs-lookup"><span data-stu-id="de566-124">Mapitags.h</span></span>
  
> <span data-ttu-id="de566-125">Содержит определения свойств, перечисленных как альтернативные имена.</span><span class="sxs-lookup"><span data-stu-id="de566-125">Contains definitions of properties listed as alternate names.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="de566-126">См. также</span><span class="sxs-lookup"><span data-stu-id="de566-126">See also</span></span>



[<span data-ttu-id="de566-127">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="de566-127">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="de566-128">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="de566-128">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="de566-129">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="de566-129">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="de566-130">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="de566-130">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

