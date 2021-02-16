---
title: Каноническое свойство PidLidOfflineStatus
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidOfflineStatus
api_type:
- COM
ms.assetid: ee69f0c4-b552-4cfd-8a39-a822d414549e
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 537b45420390903d67722c074a1edcc04a0aede8
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418836"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="c51d9-103">Каноническое свойство PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="c51d9-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="c51d9-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c51d9-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c51d9-105">Определяет состояние файла документа на сервере, который реализует [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="c51d9-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="c51d9-106">Связанные свойства</span><span class="sxs-lookup"><span data-stu-id="c51d9-106">Associated properties</span></span>  <br/> |<span data-ttu-id="c51d9-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="c51d9-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="c51d9-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="c51d9-108">Property set:</span></span>  <br/> |<span data-ttu-id="c51d9-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="c51d9-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="c51d9-110">Длинный ИД (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="c51d9-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="c51d9-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="c51d9-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="c51d9-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="c51d9-112">Data type:</span></span>  <br/> |<span data-ttu-id="c51d9-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="c51d9-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="c51d9-114">Область:</span><span class="sxs-lookup"><span data-stu-id="c51d9-114">Area:</span></span>  <br/> |<span data-ttu-id="c51d9-115">Общие сообщения</span><span class="sxs-lookup"><span data-stu-id="c51d9-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="c51d9-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="c51d9-116">Remarks</span></span>

<span data-ttu-id="c51d9-117">В следующей таблице показаны возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="c51d9-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="c51d9-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="c51d9-118">**Value**</span></span>|<span data-ttu-id="c51d9-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="c51d9-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="c51d9-120">0</span><span class="sxs-lookup"><span data-stu-id="c51d9-120">0</span></span>  <br/> |<span data-ttu-id="c51d9-121">Документ не был выверяем.</span><span class="sxs-lookup"><span data-stu-id="c51d9-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="c51d9-122">1 </span><span class="sxs-lookup"><span data-stu-id="c51d9-122">1</span></span>  <br/> |<span data-ttu-id="c51d9-123">Документ получается у текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="c51d9-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="c51d9-124">2 </span><span class="sxs-lookup"><span data-stu-id="c51d9-124">2</span></span>  <br/> |<span data-ttu-id="c51d9-125">Документ не получается, но у текущего пользователя есть копия файла, сохраненная для редактирования на текущем компьютере.</span><span class="sxs-lookup"><span data-stu-id="c51d9-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="c51d9-126">Это свойство вычисляется локально и не отправляется на сервер в любое время, если пользователь не перетащите элемент в другую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="c51d9-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="c51d9-127">В этом случае он рассматривается как пользовательское настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="c51d9-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="c51d9-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="c51d9-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="c51d9-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="c51d9-129">Protocol specifications</span></span>

<span data-ttu-id="c51d9-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="c51d9-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="c51d9-131">Предоставляет определения набора свойств и ссылки на связанные Exchange Server спецификации протокола.</span><span class="sxs-lookup"><span data-stu-id="c51d9-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="c51d9-132">Файлы заголовок</span><span class="sxs-lookup"><span data-stu-id="c51d9-132">Header files</span></span>

<span data-ttu-id="c51d9-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="c51d9-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="c51d9-134">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="c51d9-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="c51d9-135">См. также</span><span class="sxs-lookup"><span data-stu-id="c51d9-135">See also</span></span>



[<span data-ttu-id="c51d9-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c51d9-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="c51d9-137">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="c51d9-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="c51d9-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="c51d9-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="c51d9-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="c51d9-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

