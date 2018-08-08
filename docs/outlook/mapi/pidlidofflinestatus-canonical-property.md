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
ms.openlocfilehash: 34f50766c2c45d85bbb0bd9e12d32c5dd87e3cac
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810438"
---
# <a name="pidlidofflinestatus-canonical-property"></a><span data-ttu-id="a235d-103">Каноническое свойство PidLidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="a235d-103">PidLidOfflineStatus Canonical Property</span></span>

  
  
<span data-ttu-id="a235d-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="a235d-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="a235d-105">Определяет состояние файла на сервере, который реализует [MS-LISTSWS].</span><span class="sxs-lookup"><span data-stu-id="a235d-105">Determines the state of a document file on a server that implements [MS-LISTSWS].</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="a235d-106">Связанными свойствами</span><span class="sxs-lookup"><span data-stu-id="a235d-106">Associated properties</span></span>  <br/> |<span data-ttu-id="a235d-107">dispidOfflineStatus</span><span class="sxs-lookup"><span data-stu-id="a235d-107">dispidOfflineStatus</span></span>  <br/> |
|<span data-ttu-id="a235d-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="a235d-108">Property set:</span></span>  <br/> |<span data-ttu-id="a235d-109">PSETID_Common</span><span class="sxs-lookup"><span data-stu-id="a235d-109">PSETID_Common</span></span>  <br/> |
|<span data-ttu-id="a235d-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="a235d-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="a235d-111">0x000085B9</span><span class="sxs-lookup"><span data-stu-id="a235d-111">0x000085B9</span></span>  <br/> |
|<span data-ttu-id="a235d-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="a235d-112">Data type:</span></span>  <br/> |<span data-ttu-id="a235d-113">PT_LONG</span><span class="sxs-lookup"><span data-stu-id="a235d-113">PT_LONG</span></span>  <br/> |
|<span data-ttu-id="a235d-114">Область:</span><span class="sxs-lookup"><span data-stu-id="a235d-114">Area:</span></span>  <br/> |<span data-ttu-id="a235d-115">Общие системы обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="a235d-115">General messaging</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="a235d-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="a235d-116">Remarks</span></span>

<span data-ttu-id="a235d-117">В следующей таблице показаны возможные значения этого свойства.</span><span class="sxs-lookup"><span data-stu-id="a235d-117">The following table shows the possible values of this property.</span></span>
  
|<span data-ttu-id="a235d-118">**Значение**</span><span class="sxs-lookup"><span data-stu-id="a235d-118">**Value**</span></span>|<span data-ttu-id="a235d-119">**Описание**</span><span class="sxs-lookup"><span data-stu-id="a235d-119">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="a235d-120">0</span><span class="sxs-lookup"><span data-stu-id="a235d-120">0</span></span>  <br/> |<span data-ttu-id="a235d-121">Документ не извлечен.</span><span class="sxs-lookup"><span data-stu-id="a235d-121">Document is not checked out.</span></span>  <br/> |
|<span data-ttu-id="a235d-122">1</span><span class="sxs-lookup"><span data-stu-id="a235d-122">1</span></span>  <br/> |<span data-ttu-id="a235d-123">Документ извлечен текущим пользователем.</span><span class="sxs-lookup"><span data-stu-id="a235d-123">Document is checked out to the current user.</span></span>  <br/> |
|<span data-ttu-id="a235d-124">2</span><span class="sxs-lookup"><span data-stu-id="a235d-124">2</span></span>  <br/> |<span data-ttu-id="a235d-125">Документ не извлечен, но текущего пользователя имеется копия файл, сохраненный для редактирования на данном компьютере.</span><span class="sxs-lookup"><span data-stu-id="a235d-125">Document is not checked out, but the current user has a copy of the file saved for editing on the current computer.</span></span>  <br/> |
   
<span data-ttu-id="a235d-126">Это свойство рассчитывается локально и не отправляются на сервер в любое время, пока пользователь перетаскивает элемент в другую учетную запись.</span><span class="sxs-lookup"><span data-stu-id="a235d-126">This property is calculated locally and is not sent to a server at any time unless a user drags the item to another account.</span></span> <span data-ttu-id="a235d-127">В этом случае он обрабатывается как пользовательские настраиваемого свойства.</span><span class="sxs-lookup"><span data-stu-id="a235d-127">In that case, it is treated as a user-defined custom property.</span></span>
  
## <a name="related-resources"></a><span data-ttu-id="a235d-128">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="a235d-128">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="a235d-129">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="a235d-129">Protocol specifications</span></span>

<span data-ttu-id="a235d-130">[[MS-OXPROPS]]</span><span class="sxs-lookup"><span data-stu-id="a235d-130">[[MS-OXPROPS]]</span></span> 
  
> <span data-ttu-id="a235d-131">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="a235d-131">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="a235d-132">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="a235d-132">Header files</span></span>

<span data-ttu-id="a235d-133">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="a235d-133">Mapidefs.h</span></span>
  
> <span data-ttu-id="a235d-134">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="a235d-134">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="a235d-135">См. также</span><span class="sxs-lookup"><span data-stu-id="a235d-135">See also</span></span>



[<span data-ttu-id="a235d-136">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a235d-136">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="a235d-137">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="a235d-137">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="a235d-138">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="a235d-138">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="a235d-139">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="a235d-139">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

