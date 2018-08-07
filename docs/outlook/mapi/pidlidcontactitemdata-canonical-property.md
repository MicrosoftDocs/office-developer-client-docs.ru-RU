---
title: Каноническое свойство PidLidContactItemData
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
ms.prod: office-online-server
localization_priority: Normal
api_name:
- PidLidContactItemData
api_type:
- COM
ms.assetid: 411e8f81-c2b9-440a-9e9a-d6add5e4be63
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 510920af290fa1cfe13fc1a85ba72f902532c539
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19810236"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="ac298-103">Каноническое свойство PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="ac298-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="ac298-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="ac298-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="ac298-105">Используется для отображения контактных данных.</span><span class="sxs-lookup"><span data-stu-id="ac298-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="ac298-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="ac298-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="ac298-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="ac298-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="ac298-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="ac298-108">Property set:</span></span>  <br/> |<span data-ttu-id="ac298-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="ac298-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="ac298-110">Длинный идентификатор (КРЫШКА):</span><span class="sxs-lookup"><span data-stu-id="ac298-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="ac298-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="ac298-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="ac298-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="ac298-112">Data type:</span></span>  <br/> |<span data-ttu-id="ac298-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="ac298-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="ac298-114">Область:</span><span class="sxs-lookup"><span data-stu-id="ac298-114">Area:</span></span>  <br/> |<span data-ttu-id="ac298-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="ac298-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="ac298-116">Замечания</span><span class="sxs-lookup"><span data-stu-id="ac298-116">Remarks</span></span>

<span data-ttu-id="ac298-117">Если этот параметр указан, свойство должно иметь шесть записи, соответствующие каждой к полю видимой в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="ac298-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="ac298-118">**На основе одного индекса в многозначное свойство**</span><span class="sxs-lookup"><span data-stu-id="ac298-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="ac298-119">**Значение должно быть одно из следующих**</span><span class="sxs-lookup"><span data-stu-id="ac298-119">**The value must be one of the following**</span></span>|<span data-ttu-id="ac298-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ac298-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ac298-121">1</span><span class="sxs-lookup"><span data-stu-id="ac298-121">1</span></span>  <br/> |<span data-ttu-id="ac298-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="ac298-122">0x00000001</span></span>  <br/> |<span data-ttu-id="ac298-123">Приложения должны отображать домашний адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="ac298-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="ac298-124">1</span><span class="sxs-lookup"><span data-stu-id="ac298-124">1</span></span>  <br/> |<span data-ttu-id="ac298-125">0x00000002 или 0x00000000</span><span class="sxs-lookup"><span data-stu-id="ac298-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="ac298-126">Приложения должны отображать работы контакта.</span><span class="sxs-lookup"><span data-stu-id="ac298-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="ac298-127">1</span><span class="sxs-lookup"><span data-stu-id="ac298-127">1</span></span>  <br/> |<span data-ttu-id="ac298-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="ac298-128">0x00000003</span></span>  <br/> |<span data-ttu-id="ac298-129">Приложения должны отображать контакт в другой адрес.</span><span class="sxs-lookup"><span data-stu-id="ac298-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="ac298-130">2</span><span class="sxs-lookup"><span data-stu-id="ac298-130">2</span></span>  <br/> |<span data-ttu-id="ac298-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="ac298-131">0x00008080</span></span>  <br/> |<span data-ttu-id="ac298-132">Приложения должны отображать Email1.</span><span class="sxs-lookup"><span data-stu-id="ac298-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="ac298-133">2</span><span class="sxs-lookup"><span data-stu-id="ac298-133">2</span></span>  <br/> |<span data-ttu-id="ac298-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="ac298-134">0x00008090</span></span>  <br/> |<span data-ttu-id="ac298-135">Приложения должны отображать Почта2:.</span><span class="sxs-lookup"><span data-stu-id="ac298-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="ac298-136">2</span><span class="sxs-lookup"><span data-stu-id="ac298-136">2</span></span>  <br/> |<span data-ttu-id="ac298-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="ac298-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="ac298-138">Приложения должны отображать Почта3:.</span><span class="sxs-lookup"><span data-stu-id="ac298-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="ac298-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="ac298-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="ac298-140">PropertyID свойства телефона или любой из номеров факсов, который указан в [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="ac298-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="ac298-141">Приложения должны отображать соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="ac298-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="ac298-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="ac298-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="ac298-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="ac298-143">Protocol specifications</span></span>

<span data-ttu-id="ac298-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac298-144">[[MS-OXPROPS]](http://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac298-145">Содержит определения набора свойств и ссылки на связанные спецификаций протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="ac298-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="ac298-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="ac298-146">[[MS-OXOCNTC]](http://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="ac298-147">Задает свойства и операции, допустимые для контакты и списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="ac298-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="ac298-148">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="ac298-148">Header files</span></span>

<span data-ttu-id="ac298-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="ac298-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="ac298-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="ac298-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="ac298-151">См. также</span><span class="sxs-lookup"><span data-stu-id="ac298-151">See also</span></span>



[<span data-ttu-id="ac298-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac298-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="ac298-153">Каноническое свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="ac298-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="ac298-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="ac298-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="ac298-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="ac298-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

