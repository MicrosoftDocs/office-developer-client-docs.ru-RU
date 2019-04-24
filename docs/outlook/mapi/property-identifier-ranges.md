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
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32328534"
---
# <a name="property-identifier-ranges"></a><span data-ttu-id="0227e-103">Диапазоны идентификаторов свойств</span><span class="sxs-lookup"><span data-stu-id="0227e-103">Property Identifier Ranges</span></span>

  
  
<span data-ttu-id="0227e-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="0227e-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="0227e-105">В следующей таблице приведены различные диапазоны для идентификаторов свойств, описывающих владельца свойств в каждом диапазоне.</span><span class="sxs-lookup"><span data-stu-id="0227e-105">The following table summarizes the different ranges for property identifiers, describing the owner for the properties in each range.</span></span>
  
|<span data-ttu-id="0227e-106">**Диапазон идентификаторов**</span><span class="sxs-lookup"><span data-stu-id="0227e-106">**Identifier range**</span></span>|<span data-ttu-id="0227e-107">**Описание**</span><span class="sxs-lookup"><span data-stu-id="0227e-107">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0227e-108">0000</span><span class="sxs-lookup"><span data-stu-id="0227e-108">0000</span></span>  <br/> |<span data-ttu-id="0227e-109">ЗаРезервировано MAPI для специального значения **пр_нулл**.</span><span class="sxs-lookup"><span data-stu-id="0227e-109">Reserved by MAPI for the special value **PR_NULL**.</span></span>  <br/> |
|<span data-ttu-id="0227e-110">0001 — 0BFF</span><span class="sxs-lookup"><span data-stu-id="0227e-110">0001 - 0BFF</span></span>  <br/> |<span data-ttu-id="0227e-111">Свойства конверта сообщения, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="0227e-111">Message envelope properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="0227e-112">0C00 — 0DFF</span><span class="sxs-lookup"><span data-stu-id="0227e-112">0C00 - 0DFF</span></span>  <br/> |<span data-ttu-id="0227e-113">Свойства получателей, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="0227e-113">Recipient properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="0227e-114">0E00 — 0FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-114">0E00 - 0FFF</span></span>  <br/> |<span data-ttu-id="0227e-115">Свойства сообщений, не поддерживающие передачу, заданные MAPI.</span><span class="sxs-lookup"><span data-stu-id="0227e-115">Non-transmittable message properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="0227e-116">1000 — 2FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-116">1000 - 2FFF</span></span>  <br/> |<span data-ttu-id="0227e-117">Свойства содержимого сообщения, определенные MAPI.</span><span class="sxs-lookup"><span data-stu-id="0227e-117">Message content properties defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="0227e-118">3000 — 3FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-118">3000 - 3FFF</span></span>  <br/> |<span data-ttu-id="0227e-119">Свойства для объектов, отличных от сообщений и получателей, определенных MAPI.</span><span class="sxs-lookup"><span data-stu-id="0227e-119">Properties for objects other than messages and recipients defined by MAPI.</span></span>  <br/> |
|<span data-ttu-id="0227e-120">4000 — 57FF</span><span class="sxs-lookup"><span data-stu-id="0227e-120">4000 - 57FF</span></span>  <br/> |<span data-ttu-id="0227e-121">Свойства конверта сообщения, определенные поставщиками транспорта.</span><span class="sxs-lookup"><span data-stu-id="0227e-121">Message envelope properties defined by transport providers.</span></span>  <br/> |
|<span data-ttu-id="0227e-122">5800 — 5FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-122">5800 - 5FFF</span></span>  <br/> |<span data-ttu-id="0227e-123">Свойства получателей, определенные в поставщиках транспорта и адресных книг.</span><span class="sxs-lookup"><span data-stu-id="0227e-123">Recipient properties defined by transport and address book providers.</span></span>  <br/> |
|<span data-ttu-id="0227e-124">6000 — 65FF</span><span class="sxs-lookup"><span data-stu-id="0227e-124">6000 - 65FF</span></span>  <br/> |<span data-ttu-id="0227e-125">Свойства сообщений, не поддерживающие передачу, заданные клиентами.</span><span class="sxs-lookup"><span data-stu-id="0227e-125">Non-transmittable message properties defined by clients.</span></span>  <br/> |
|<span data-ttu-id="0227e-126">6600 — 67FF</span><span class="sxs-lookup"><span data-stu-id="0227e-126">6600 - 67FF</span></span>  <br/> |<span data-ttu-id="0227e-127">Неподдерживаемые свойства, определенные поставщиком услуг.</span><span class="sxs-lookup"><span data-stu-id="0227e-127">Non-transmittable properties defined by a service provider.</span></span> <span data-ttu-id="0227e-128">Эти свойства могут быть видимыми или невидимыми для пользователей.</span><span class="sxs-lookup"><span data-stu-id="0227e-128">These properties can be visible or invisible to users.</span></span>  <br/> |
|<span data-ttu-id="0227e-129">6800 — 7BFF</span><span class="sxs-lookup"><span data-stu-id="0227e-129">6800 - 7BFF</span></span>  <br/> |<span data-ttu-id="0227e-130">Свойства содержимого сообщений для настраиваемых классов сообщений, определенных авторами этих классов.</span><span class="sxs-lookup"><span data-stu-id="0227e-130">Message content properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="0227e-131">7C00 — 7FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-131">7C00 - 7FFF</span></span>  <br/> |<span data-ttu-id="0227e-132">Неподдерживаемые свойства для настраиваемых классов сообщений, определенных авторами этих классов.</span><span class="sxs-lookup"><span data-stu-id="0227e-132">Non-transmittable properties for custom message classes defined by creators of those classes.</span></span>  <br/> |
|<span data-ttu-id="0227e-133">8000 — ФФФЕ</span><span class="sxs-lookup"><span data-stu-id="0227e-133">8000 - FFFE</span></span>  <br/> |<span data-ttu-id="0227e-134">Свойства, определяемые клиентами и порой поставщики услуг, идентифицируемые по имени с помощью методов [IMAPIProp:: жетнамесфромидс](imapiprop-getnamesfromids.md) и [IMAPIProp:: жетидсфромнамес](imapiprop-getidsfromnames.md) .</span><span class="sxs-lookup"><span data-stu-id="0227e-134">Properties defined by clients and occasionally service providers that are identified by name through the [IMAPIProp::GetNamesFromIDs](imapiprop-getnamesfromids.md) and [IMAPIProp::GetIDsFromNames](imapiprop-getidsfromnames.md) methods.</span></span>  <br/> |
|<span data-ttu-id="0227e-135">FFFF</span><span class="sxs-lookup"><span data-stu-id="0227e-135">FFFF</span></span>  <br/> |<span data-ttu-id="0227e-136">ЗаРезервировано MAPI для специального значения ошибки ПРОП_ИД_ИНВАЛИД.</span><span class="sxs-lookup"><span data-stu-id="0227e-136">Reserved by MAPI for the special error value PROP_ID_INVALID.</span></span>  <br/> |
   
<span data-ttu-id="0227e-137">Диапазон между 3000 и 3FFF зарезервирован для свойств, которые не связаны ни с одним сообщением, ни с получателем.</span><span class="sxs-lookup"><span data-stu-id="0227e-137">The range between 3000 and 3FFF is reserved for properties that are not related to either messages or recipients.</span></span> <span data-ttu-id="0227e-138">MAPI разделяет этот диапазон на вложенные диапазоны по типам объекта; в следующей таблице приведена эта дальнейшая подразделение.</span><span class="sxs-lookup"><span data-stu-id="0227e-138">MAPI divides this range into sub-ranges by types of object; the following table shows this further breakdown.</span></span> 
  
|<span data-ttu-id="0227e-139">**Диапазон идентификаторов**</span><span class="sxs-lookup"><span data-stu-id="0227e-139">**Identifier range**</span></span>|<span data-ttu-id="0227e-140">**Тип свойства**</span><span class="sxs-lookup"><span data-stu-id="0227e-140">**Type of property**</span></span>|
|:-----|:-----|
|<span data-ttu-id="0227e-141">3000 — 33FF</span><span class="sxs-lookup"><span data-stu-id="0227e-141">3000 - 33FF</span></span>  <br/> |<span data-ttu-id="0227e-142">Общие свойства, которые отображаются в нескольких объектах, таких как **пр_дисплай_наме** и **пр_ентрид**.</span><span class="sxs-lookup"><span data-stu-id="0227e-142">Common properties that appear on multiple objects, such as **PR_DISPLAY_NAME** and **PR_ENTRYID**.</span></span>  <br/> |
|<span data-ttu-id="0227e-143">3400 — 35FF</span><span class="sxs-lookup"><span data-stu-id="0227e-143">3400 - 35FF</span></span>  <br/> |<span data-ttu-id="0227e-144">Свойства хранилища сообщений</span><span class="sxs-lookup"><span data-stu-id="0227e-144">Message store properties</span></span>  <br/> |
|<span data-ttu-id="0227e-145">3600 — 36FF</span><span class="sxs-lookup"><span data-stu-id="0227e-145">3600 - 36FF</span></span>  <br/> |<span data-ttu-id="0227e-146">Свойства контейнеров папок и адресных книг</span><span class="sxs-lookup"><span data-stu-id="0227e-146">Folder and address book container properties</span></span>  <br/> |
|<span data-ttu-id="0227e-147">3700 — 38FF</span><span class="sxs-lookup"><span data-stu-id="0227e-147">3700 - 38FF</span></span>  <br/> |<span data-ttu-id="0227e-148">Свойства вложений</span><span class="sxs-lookup"><span data-stu-id="0227e-148">Attachment properties</span></span>  <br/> |
|<span data-ttu-id="0227e-149">3900 — 39FF</span><span class="sxs-lookup"><span data-stu-id="0227e-149">3900 - 39FF</span></span>  <br/> |<span data-ttu-id="0227e-150">Свойства адресных книг</span><span class="sxs-lookup"><span data-stu-id="0227e-150">Address book properties</span></span>  <br/> |
|<span data-ttu-id="0227e-151">3A00 — 3BFF</span><span class="sxs-lookup"><span data-stu-id="0227e-151">3A00 - 3BFF</span></span>  <br/> |<span data-ttu-id="0227e-152">Свойства пользователя для обмена сообщениями</span><span class="sxs-lookup"><span data-stu-id="0227e-152">Messaging user properties</span></span>  <br/> |
|<span data-ttu-id="0227e-153">3C00 — 3CFF</span><span class="sxs-lookup"><span data-stu-id="0227e-153">3C00 - 3CFF</span></span>  <br/> |<span data-ttu-id="0227e-154">Свойства списка рассылки</span><span class="sxs-lookup"><span data-stu-id="0227e-154">Distribution list properties</span></span>  <br/> |
|<span data-ttu-id="0227e-155">3D00 — 3DFF</span><span class="sxs-lookup"><span data-stu-id="0227e-155">3D00 - 3DFF</span></span>  <br/> |<span data-ttu-id="0227e-156">Свойства профиля</span><span class="sxs-lookup"><span data-stu-id="0227e-156">Profile properties</span></span>  <br/> |
|<span data-ttu-id="0227e-157">3E00 — 3FFF</span><span class="sxs-lookup"><span data-stu-id="0227e-157">3E00 - 3FFF</span></span>  <br/> |<span data-ttu-id="0227e-158">Свойства объекта Status</span><span class="sxs-lookup"><span data-stu-id="0227e-158">Status object properties</span></span>  <br/> |
   

