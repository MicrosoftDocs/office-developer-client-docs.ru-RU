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
# <a name="pidlidcontactitemdata-canonical-property"></a><span data-ttu-id="56296-103">Каноническое свойство PidLidContactItemData</span><span class="sxs-lookup"><span data-stu-id="56296-103">PidLidContactItemData Canonical Property</span></span>

  
  
<span data-ttu-id="56296-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="56296-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="56296-105">Используется для отображения контактной информации.</span><span class="sxs-lookup"><span data-stu-id="56296-105">Used to display the contact information.</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="56296-106">Связанные свойства:</span><span class="sxs-lookup"><span data-stu-id="56296-106">Associated properties:</span></span>  <br/> |<span data-ttu-id="56296-107">диспидконтактитемдата</span><span class="sxs-lookup"><span data-stu-id="56296-107">dispidContactItemData</span></span>  <br/> |
|<span data-ttu-id="56296-108">Набор свойств:</span><span class="sxs-lookup"><span data-stu-id="56296-108">Property set:</span></span>  <br/> |<span data-ttu-id="56296-109">PSETID_Address</span><span class="sxs-lookup"><span data-stu-id="56296-109">PSETID_Address</span></span>  <br/> |
|<span data-ttu-id="56296-110">Длинный идентификатор (крышка):</span><span class="sxs-lookup"><span data-stu-id="56296-110">Long ID (LID):</span></span>  <br/> |<span data-ttu-id="56296-111">0x00008007</span><span class="sxs-lookup"><span data-stu-id="56296-111">0x00008007</span></span>  <br/> |
|<span data-ttu-id="56296-112">Тип данных:</span><span class="sxs-lookup"><span data-stu-id="56296-112">Data type:</span></span>  <br/> |<span data-ttu-id="56296-113">PT_MV_LONG</span><span class="sxs-lookup"><span data-stu-id="56296-113">PT_MV_LONG</span></span>  <br/> |
|<span data-ttu-id="56296-114">Область:</span><span class="sxs-lookup"><span data-stu-id="56296-114">Area:</span></span>  <br/> |<span data-ttu-id="56296-115">Контакт</span><span class="sxs-lookup"><span data-stu-id="56296-115">Contact</span></span>  <br/> |
   
## <a name="remarks"></a><span data-ttu-id="56296-116">Примечания</span><span class="sxs-lookup"><span data-stu-id="56296-116">Remarks</span></span>

<span data-ttu-id="56296-117">Если задано, свойство должно иметь шесть записей, каждое из которых соответствует видимому полю в пользовательском интерфейсе приложения.</span><span class="sxs-lookup"><span data-stu-id="56296-117">If present, the property must have six entries, each corresponding to a visible field in the application's user interface.</span></span>
  
|<span data-ttu-id="56296-118">**Индекс, отсчитываемый от единицы, в свойстве с несколькими значениями**</span><span class="sxs-lookup"><span data-stu-id="56296-118">**One-based index into the multi-valued property**</span></span>|<span data-ttu-id="56296-119">**Значение должно быть одним из следующих**</span><span class="sxs-lookup"><span data-stu-id="56296-119">**The value must be one of the following**</span></span>|<span data-ttu-id="56296-120">**Описание**</span><span class="sxs-lookup"><span data-stu-id="56296-120">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="56296-121">1,1</span><span class="sxs-lookup"><span data-stu-id="56296-121">1</span></span>  <br/> |<span data-ttu-id="56296-122">0x00000001</span><span class="sxs-lookup"><span data-stu-id="56296-122">0x00000001</span></span>  <br/> |<span data-ttu-id="56296-123">Приложение должно отображать домашний адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="56296-123">The application should display the contact's home address.</span></span>  <br/> |
|<span data-ttu-id="56296-124">1,1</span><span class="sxs-lookup"><span data-stu-id="56296-124">1</span></span>  <br/> |<span data-ttu-id="56296-125">0x00000002 или 0x00000000</span><span class="sxs-lookup"><span data-stu-id="56296-125">0x00000002 or 0x00000000</span></span>  <br/> |<span data-ttu-id="56296-126">Приложение должно отображать работу контакта.</span><span class="sxs-lookup"><span data-stu-id="56296-126">The application should display the contact's work.</span></span>  <br/> |
|<span data-ttu-id="56296-127">1,1</span><span class="sxs-lookup"><span data-stu-id="56296-127">1</span></span>  <br/> |<span data-ttu-id="56296-128">0x00000003</span><span class="sxs-lookup"><span data-stu-id="56296-128">0x00000003</span></span>  <br/> |<span data-ttu-id="56296-129">Приложение должно отображать другой адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="56296-129">The application should display the contact's other address.</span></span>  <br/> |
|<span data-ttu-id="56296-130">2</span><span class="sxs-lookup"><span data-stu-id="56296-130">2</span></span>  <br/> |<span data-ttu-id="56296-131">0x00008080</span><span class="sxs-lookup"><span data-stu-id="56296-131">0x00008080</span></span>  <br/> |<span data-ttu-id="56296-132">Приложение должно отображать Email1.</span><span class="sxs-lookup"><span data-stu-id="56296-132">The application should display Email1.</span></span>  <br/> |
|<span data-ttu-id="56296-133">2</span><span class="sxs-lookup"><span data-stu-id="56296-133">2</span></span>  <br/> |<span data-ttu-id="56296-134">0x00008090</span><span class="sxs-lookup"><span data-stu-id="56296-134">0x00008090</span></span>  <br/> |<span data-ttu-id="56296-135">Приложение должно отображать Email2.</span><span class="sxs-lookup"><span data-stu-id="56296-135">The application should display Email2.</span></span>  <br/> |
|<span data-ttu-id="56296-136">2</span><span class="sxs-lookup"><span data-stu-id="56296-136">2</span></span>  <br/> |<span data-ttu-id="56296-137">0x000080A0</span><span class="sxs-lookup"><span data-stu-id="56296-137">0x000080A0</span></span>  <br/> |<span data-ttu-id="56296-138">Приложение должно отображать Email3.</span><span class="sxs-lookup"><span data-stu-id="56296-138">The application should display Email3.</span></span>  <br/> |
|<span data-ttu-id="56296-139">3, 4, 5, 6</span><span class="sxs-lookup"><span data-stu-id="56296-139">3,4,5,6</span></span>  <br/> |<span data-ttu-id="56296-140">Пропертид любого из свойств телефона или номеров факсов, указанных в [[MS-оксокнтк]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span><span class="sxs-lookup"><span data-stu-id="56296-140">PropertyID of any of the telephone properties or any of the fax numbers that are specified in [[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx).</span></span>  <br/> |<span data-ttu-id="56296-141">Приложение должно отображать соответствующее свойство.</span><span class="sxs-lookup"><span data-stu-id="56296-141">The application should display the corresponding property.</span></span>  <br/> |
   
## <a name="related-resources"></a><span data-ttu-id="56296-142">Связанные ресурсы</span><span class="sxs-lookup"><span data-stu-id="56296-142">Related resources</span></span>

### <a name="protocol-specifications"></a><span data-ttu-id="56296-143">Спецификации протокола</span><span class="sxs-lookup"><span data-stu-id="56296-143">Protocol specifications</span></span>

<span data-ttu-id="56296-144">[[MS — ОКСПРОПС]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56296-144">[[MS-OXPROPS]](https://msdn.microsoft.com/library/f6ab1613-aefe-447d-a49c-18217230b148%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56296-145">Содержит определения свойств и ссылки на связанные спецификации протокола Exchange Server.</span><span class="sxs-lookup"><span data-stu-id="56296-145">Provides property set definitions and references to related Exchange Server protocol specifications.</span></span>
    
<span data-ttu-id="56296-146">[[MS — ОКСОКНТК]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span><span class="sxs-lookup"><span data-stu-id="56296-146">[[MS-OXOCNTC]](https://msdn.microsoft.com/library/9b636532-9150-4836-9635-9c9b756c9ccf%28Office.15%29.aspx)</span></span>
  
> <span data-ttu-id="56296-147">Задает свойства и операции, допустимые для контактов и личных списков рассылки.</span><span class="sxs-lookup"><span data-stu-id="56296-147">Specifies the properties and operations that are permissible for contacts and personal distribution lists.</span></span>
    
### <a name="header-files"></a><span data-ttu-id="56296-148">Файлы заголовков</span><span class="sxs-lookup"><span data-stu-id="56296-148">Header files</span></span>

<span data-ttu-id="56296-149">MAPIDEFS. h</span><span class="sxs-lookup"><span data-stu-id="56296-149">Mapidefs.h</span></span>
  
> <span data-ttu-id="56296-150">Содержит определения типов данных.</span><span class="sxs-lookup"><span data-stu-id="56296-150">Provides data type definitions.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="56296-151">См. также</span><span class="sxs-lookup"><span data-stu-id="56296-151">See also</span></span>



[<span data-ttu-id="56296-152">Свойства MAPI</span><span class="sxs-lookup"><span data-stu-id="56296-152">MAPI Properties</span></span>](mapi-properties.md)
  
[<span data-ttu-id="56296-153">Каноническое свойство MAPI</span><span class="sxs-lookup"><span data-stu-id="56296-153">MAPI Canonical Properties</span></span>](mapi-canonical-properties.md)
  
[<span data-ttu-id="56296-154">Сопоставление имен канонических свойств с именами MAPI</span><span class="sxs-lookup"><span data-stu-id="56296-154">Mapping Canonical Property Names to MAPI Names</span></span>](mapping-canonical-property-names-to-mapi-names.md)
  
[<span data-ttu-id="56296-155">Сопоставление имен MAPI с именами канонических свойств</span><span class="sxs-lookup"><span data-stu-id="56296-155">Mapping MAPI Names to Canonical Property Names</span></span>](mapping-mapi-names-to-canonical-property-names.md)

