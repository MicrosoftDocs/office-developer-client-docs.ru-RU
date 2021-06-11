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
ms.openlocfilehash: cdf1eae945cddf9eb76a2b7a2532d5dc6568beac
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33422707"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="ad478-103">Диапазоны идентификаторов свойств</span><span class="sxs-lookup"><span data-stu-id="ad478-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="ad478-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ad478-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ad478-105">В следующей таблице описываются различные диапазоны идентификаторов свойств, описывающие владельца свойств в каждом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="ad478-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="ad478-106">**Диапазон идентификаторов**</span><span class="sxs-lookup"><span data-stu-id="ad478-106">**Identifier range**</span></span>|<span data-ttu-id="ad478-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ad478-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad478-108">0000</span><span class="sxs-lookup"><span data-stu-id="ad478-108">0000</span></span>  <br/> |<span data-ttu-id="ad478-109">Зарезервировано MAPI для специального **значения PR_NULL**.</span><span class="sxs-lookup"><span data-stu-id="ad478-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="ad478-110">0001 - 0BFF</span><span class="sxs-lookup"><span data-stu-id="ad478-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="ad478-111">Свойства конверта сообщений, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad478-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ad478-112">0C00 - 0DFF</span><span class="sxs-lookup"><span data-stu-id="ad478-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="ad478-113">Свойства получателей, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad478-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ad478-114">0E00 - 0FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="ad478-115">Свойства непередаваемого сообщения, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad478-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ad478-116">1000 - 2FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="ad478-117">Свойства контента сообщений, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad478-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ad478-118">3000 — 3FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="ad478-119">Свойства для объектов, помимо сообщений и получателей, определенных MAPI.</span><span class="sxs-lookup"><span data-stu-id="ad478-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="ad478-120">4000 - 57FF</span><span class="sxs-lookup"><span data-stu-id="ad478-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="ad478-121">Свойства конверта сообщений, определенные поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="ad478-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="ad478-122">5800 - 5FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="ad478-123">Свойства получателей, определенные поставщиками транспортных и адресных книг.</span><span class="sxs-lookup"><span data-stu-id="ad478-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="ad478-124">6000 - 65FF</span><span class="sxs-lookup"><span data-stu-id="ad478-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="ad478-125">Свойства непередаваемого сообщения, определенные клиентами.</span><span class="sxs-lookup"><span data-stu-id="ad478-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="ad478-126">6600 - 67FF</span><span class="sxs-lookup"><span data-stu-id="ad478-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="ad478-127">Свойства, которые не передаются, определенные поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="ad478-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="ad478-128">Эти свойства могут быть видимыми или невидимыми для пользователей.</span><span class="sxs-lookup"><span data-stu-id="ad478-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="ad478-129">6800 - 7BFF</span><span class="sxs-lookup"><span data-stu-id="ad478-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="ad478-130">Свойства контента сообщений для пользовательских классов сообщений, определенных создателями этих классов.</span><span class="sxs-lookup"><span data-stu-id="ad478-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="ad478-131">7C00 - 7FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="ad478-132">Непередаваемые свойства для настраиваемых классов сообщений, определенных создателями этих классов.</span><span class="sxs-lookup"><span data-stu-id="ad478-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="ad478-133">8000 - FFFE</span><span class="sxs-lookup"><span data-stu-id="ad478-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="ad478-134">Свойства, определенные клиентами и иногда поставщиками услуг, которые определяются по имени с помощью [методов IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) и [IMAPIProp::GetIDsFromNames.](imapiprop-getidsfromnames.md)</span><span class="sxs-lookup"><span data-stu-id="ad478-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="ad478-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="ad478-135">FFFF</span></span>  <br/> |<span data-ttu-id="ad478-136">Зарезервировано MAPI для специального значения ошибки PROP_ID_INVALID.</span><span class="sxs-lookup"><span data-stu-id="ad478-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="ad478-137">Диапазон между 3000 и 3FFF зарезервирован для свойств, не связанных ни с сообщениями, ни с получателями.</span><span class="sxs-lookup"><span data-stu-id="ad478-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="ad478-138">MAPI делит этот диапазон на подстанцию по типам объектов; В следующей таблице показана следующая разбивка.</span><span class="sxs-lookup"><span data-stu-id="ad478-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="ad478-139">**Диапазон идентификаторов**</span><span class="sxs-lookup"><span data-stu-id="ad478-139">**Identifier range**</span></span>|<span data-ttu-id="ad478-140">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="ad478-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ad478-141">3000 - 33FF</span><span class="sxs-lookup"><span data-stu-id="ad478-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="ad478-142">Общие свойства, которые отображаются на нескольких объектах, таких как **PR_DISPLAY_NAME** и **PR_ENTRYID.**</span><span class="sxs-lookup"><span data-stu-id="ad478-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="ad478-143">3400 - 35FF</span><span class="sxs-lookup"><span data-stu-id="ad478-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="ad478-144">Свойства магазина сообщений</span><span class="sxs-lookup"><span data-stu-id="ad478-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="ad478-145">3600 - 36FF</span><span class="sxs-lookup"><span data-stu-id="ad478-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="ad478-146">Свойства контейнера папки и адресной книги</span><span class="sxs-lookup"><span data-stu-id="ad478-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="ad478-147">3700 - 38FF</span><span class="sxs-lookup"><span data-stu-id="ad478-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="ad478-148">Свойства вложения</span><span class="sxs-lookup"><span data-stu-id="ad478-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="ad478-149">3900 - 39FF</span><span class="sxs-lookup"><span data-stu-id="ad478-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="ad478-150">Свойства адресной книги</span><span class="sxs-lookup"><span data-stu-id="ad478-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="ad478-151">3A00 - 3BFF</span><span class="sxs-lookup"><span data-stu-id="ad478-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="ad478-152">Свойства пользователей обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="ad478-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="ad478-153">3C00 - 3CFF</span><span class="sxs-lookup"><span data-stu-id="ad478-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="ad478-154">Свойства списка рассылки</span><span class="sxs-lookup"><span data-stu-id="ad478-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="ad478-155">3D00 - 3DFF</span><span class="sxs-lookup"><span data-stu-id="ad478-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="ad478-156">Свойства профиля</span><span class="sxs-lookup"><span data-stu-id="ad478-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="ad478-157">3E00 - 3FFF</span><span class="sxs-lookup"><span data-stu-id="ad478-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="ad478-158">Свойства объекта status</span><span class="sxs-lookup"><span data-stu-id="ad478-158">Status object properties</span></span>  <br/> |
   

