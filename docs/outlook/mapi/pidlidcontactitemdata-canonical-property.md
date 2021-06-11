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
ms.openlocfilehash: 031e5483539ce17c8b9b994690985c2349573e27
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32319512"
---
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="df321-103">Каноническое свойство PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="df321-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="df321-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="df321-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="df321-105">Используется для отображения контактных данных.</span><span class="sxs-lookup"><span data-stu-id="df321-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="df321-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="df321-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="df321-107">dispidContactItemData</span><span class="sxs-lookup"><span data-stu-id="df321-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="df321-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="df321-108">Property set:</span></span>  <br/> |<span data-ttu-id="df321-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="df321-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="df321-110">Long ID (LID):</span><span class="sxs-lookup"><span data-stu-id="df321-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="df321-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="df321-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="df321-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="df321-112">Data type:</span></span>  <br/> |<span data-ttu-id="df321-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="df321-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="df321-114">Область:</span><span class="sxs-lookup"><span data-stu-id="df321-114">Area:</span></span>  <br/> |<span data-ttu-id="df321-115">Contact</span><span class="sxs-lookup"><span data-stu-id="df321-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="df321-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="df321-116">Remarks</span></span>

<span data-ttu-id="df321-117">При этом свойство должно иметь шесть записей, каждая из которых соответствует видимому полю в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="df321-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="df321-118">**One-based index into the multi-valued property**</span><span class="sxs-lookup"><span data-stu-id="df321-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="df321-119">**Значение должно быть одним из следующих**</span><span class="sxs-lookup"><span data-stu-id="df321-119">**The value must be one of the following**</span></span>|<span data-ttu-id="df321-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="df321-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="df321-121">1</span><span class="sxs-lookup"><span data-stu-id="df321-121">1</span></span>  <br/> |<span data-ttu-id="df321-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="df321-122">0x00000001</span></span>  <br/> |<span data-ttu-id="df321-123">Приложение должно отображать домашний адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="df321-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="df321-124">1</span><span class="sxs-lookup"><span data-stu-id="df321-124">1</span></span>  <br/> |<span data-ttu-id="df321-125">0x00000002 или 0x00000000</span><span class="sxs-lookup"><span data-stu-id="df321-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="df321-126">Приложение должно отображать работу контакта.</span><span class="sxs-lookup"><span data-stu-id="df321-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="df321-127">1</span><span class="sxs-lookup"><span data-stu-id="df321-127">1</span></span>  <br/> |<span data-ttu-id="df321-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="df321-128">0x00000003</span></span>  <br/> |<span data-ttu-id="df321-129">Приложение должно отображать другой адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="df321-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="df321-130">2</span><span class="sxs-lookup"><span data-stu-id="df321-130">2</span></span>  <br/> |<span data-ttu-id="df321-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="df321-131">0x00008080</span></span>  <br/> |<span data-ttu-id="df321-132">Приложение должно отображать email1.</span><span class="sxs-lookup"><span data-stu-id="df321-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="df321-133">2</span><span class="sxs-lookup"><span data-stu-id="df321-133">2</span></span>  <br/> |<span data-ttu-id="df321-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="df321-134">0x00008090</span></span>  <br/> |<span data-ttu-id="df321-135">Приложение должно отображать email2.</span><span class="sxs-lookup"><span data-stu-id="df321-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="df321-136">2</span><span class="sxs-lookup"><span data-stu-id="df321-136">2</span></span>  <br/> |<span data-ttu-id="df321-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="df321-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="df321-138">Приложение должно отображать email3.</span><span class="sxs-lookup"><span data-stu-id="df321-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="df321-139">3,4,5,6</span><span class="sxs-lookup"><span data-stu-id="df321-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="df321-140">PropertyID любого из свойств телефона или любых номеров факсов, указанных [в [MS-OXOCNTC].](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df321-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="df321-141">Приложение должно отображать соответствующее свойство.</span><span class="sxs-lookup"><span data-stu-id="df321-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="df321-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="df321-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="df321-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="df321-143">Protocol specifications</span></span>

<span data-ttu-id="df321-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df321-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df321-145">Предоставляет определения набора свойств и ссылки на связанные Exchange Server протоколы.</span><span class="sxs-lookup"><span data-stu-id="df321-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="df321-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="df321-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="df321-147">Указывает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="df321-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="df321-148">Файлы заголовки</span><span class="sxs-lookup"><span data-stu-id="df321-148">Header files</span></span>

<span data-ttu-id="df321-149">Mapidefs.h</span><span class="sxs-lookup"><span data-stu-id="df321-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="df321-150">Предоставляет определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="df321-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="df321-151">См. также</span><span class="sxs-lookup"><span data-stu-id="df321-151">See also</span></span>



[<span data-ttu-id="df321-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="df321-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="df321-153">Канонические свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="df321-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="df321-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="df321-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="df321-155">Сопоставление имен MAPI с каноническими именами свойств</span><span class="sxs-lookup"><span data-stu-id="df321-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

