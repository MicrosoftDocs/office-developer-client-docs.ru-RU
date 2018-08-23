---
title: Диапазоны идентификаторов свойств
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: c01e95bb-be25-490d-880b-60674f890258
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 479e5abda9137ddaedcabb8d914bc038ddf200f3
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22581106"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="9d610-103">Диапазоны идентификаторов свойств</span><span class="sxs-lookup"><span data-stu-id="9d610-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="9d610-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="9d610-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="9d610-105">В следующей таблице приведены различные диапазонов для идентификаторов свойств, описывающее владельца для свойств в каждом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="9d610-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="9d610-106">**Идентификатор диапазона**</span><span class="sxs-lookup"><span data-stu-id="9d610-106">**Identifier range**</span></span>|<span data-ttu-id="9d610-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="9d610-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d610-108">0000</span><span class="sxs-lookup"><span data-stu-id="9d610-108">0000</span></span>  <br/> |<span data-ttu-id="9d610-109">Зарезервировано для MAPI для особое значение **PR_NULL**.</span><span class="sxs-lookup"><span data-stu-id="9d610-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="9d610-110">0001 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="9d610-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="9d610-111">Свойства конверт сообщения, определенные в MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d610-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="9d610-112">0C 00 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="9d610-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="9d610-113">Получателей свойств, определенных в MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d610-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="9d610-114">0E00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="9d610-115">Свойства не передаваемого сообщения, определенные в MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d610-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="9d610-116">1000 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="9d610-117">Сообщение контента свойств, определенных в MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d610-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="9d610-118">3000 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="9d610-119">Свойства для объектов, отличные от сообщений и получателей, определенных для MAPI.</span><span class="sxs-lookup"><span data-stu-id="9d610-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="9d610-120">4000 - 57FF</span><span class="sxs-lookup"><span data-stu-id="9d610-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="9d610-121">Свойства конверт сообщения, определенные поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="9d610-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="9d610-122">5800 - 5FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="9d610-123">Получателей свойств, определенных в транспортный сервер и адресной книги поставщиков.</span><span class="sxs-lookup"><span data-stu-id="9d610-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="9d610-124">6000 - 65FF</span><span class="sxs-lookup"><span data-stu-id="9d610-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="9d610-125">Свойства не передаваемого сообщения, определенные клиентами.</span><span class="sxs-lookup"><span data-stu-id="9d610-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="9d610-126">6600 - 67FF</span><span class="sxs-lookup"><span data-stu-id="9d610-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="9d610-127">Не передаваемого свойств, определенных поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="9d610-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="9d610-128">Эти свойства могут быть видимой или невидимой для пользователей.</span><span class="sxs-lookup"><span data-stu-id="9d610-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="9d610-129">6800 - 7BFF</span><span class="sxs-lookup"><span data-stu-id="9d610-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="9d610-130">Свойства содержимого сообщения для пользовательских классов сообщений определенные создателями классов.</span><span class="sxs-lookup"><span data-stu-id="9d610-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="9d610-131">7C 00 - 7FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="9d610-132">Не передаваемого свойства для пользовательских классов сообщений определенные создателями классов.</span><span class="sxs-lookup"><span data-stu-id="9d610-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="9d610-133">8000 - FFFE</span><span class="sxs-lookup"><span data-stu-id="9d610-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="9d610-134">Свойства иногда службы поставщиков, которые определяются по имени с помощью методов [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) и определенных клиентами.</span><span class="sxs-lookup"><span data-stu-id="9d610-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="9d610-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="9d610-135">FFFF</span></span>  <br/> |<span data-ttu-id="9d610-136">Зарезервировано для MAPI для PROP_ID_INVALID значение специальные ошибки.</span><span class="sxs-lookup"><span data-stu-id="9d610-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="9d610-137">Диапазон между 3000 и 3FFF зарезервирован для свойств, которые не связаны с сообщения или получателей.</span><span class="sxs-lookup"><span data-stu-id="9d610-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="9d610-138">MAPI делит этот диапазон в подменю диапазонов на тип объектов; в следующей таблице показаны в этом тщательного анализа.</span><span class="sxs-lookup"><span data-stu-id="9d610-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="9d610-139">**Идентификатор диапазона**</span><span class="sxs-lookup"><span data-stu-id="9d610-139">**Identifier range**</span></span>|<span data-ttu-id="9d610-140">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="9d610-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="9d610-141">3000 - 33FF</span><span class="sxs-lookup"><span data-stu-id="9d610-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="9d610-142">Общие свойства, отображаемые на несколько объектов, таких как **PR_DISPLAY_NAME** и **PR_ENTRYID**.</span><span class="sxs-lookup"><span data-stu-id="9d610-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="9d610-143">3400 - 35FF</span><span class="sxs-lookup"><span data-stu-id="9d610-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="9d610-144">Свойства хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="9d610-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="9d610-145">3600 - 36FF</span><span class="sxs-lookup"><span data-stu-id="9d610-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="9d610-146">Папка и адресной книги контейнер свойств</span><span class="sxs-lookup"><span data-stu-id="9d610-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="9d610-147">3700 - 38FF</span><span class="sxs-lookup"><span data-stu-id="9d610-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="9d610-148">Свойства вложения</span><span class="sxs-lookup"><span data-stu-id="9d610-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="9d610-149">3900 - 39FF</span><span class="sxs-lookup"><span data-stu-id="9d610-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="9d610-150">Свойств адресной книги</span><span class="sxs-lookup"><span data-stu-id="9d610-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="9d610-151">3A00 - 3BFF</span><span class="sxs-lookup"><span data-stu-id="9d610-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="9d610-152">Система обмена сообщениями свойств пользователя</span><span class="sxs-lookup"><span data-stu-id="9d610-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="9d610-153">3C 00 - 3CFF</span><span class="sxs-lookup"><span data-stu-id="9d610-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="9d610-154">Свойства списка рассылки</span><span class="sxs-lookup"><span data-stu-id="9d610-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="9d610-155">3D 00 - 3DFF</span><span class="sxs-lookup"><span data-stu-id="9d610-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="9d610-156">Свойства профиля</span><span class="sxs-lookup"><span data-stu-id="9d610-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="9d610-157">3E00 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="9d610-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="9d610-158">Свойства объекта состояния</span><span class="sxs-lookup"><span data-stu-id="9d610-158">Status object properties</span></span>  <br/> |
   

