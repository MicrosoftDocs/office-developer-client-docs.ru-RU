---
title: Свойства получателей для всех сообщений
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 18c96796-f38d-4058-9c51-9c5a14990846
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: 3c5764d74039249ccac47d449f0ebd4042893434
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33439718"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="449e8-103">Свойства получателей для всех сообщений</span><span class="sxs-lookup"><span data-stu-id="449e8-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="449e8-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="449e8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="449e8-105">Следующие свойства обычно присутствуют для всех получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="449e8-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="449e8-106">**PR_EMAIL_ADDRESS** **и PR_SEARCH_KEY** являются необязательными; все остальные свойства необходимы.</span><span class="sxs-lookup"><span data-stu-id="449e8-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="449e8-107">**Название таблицы**</span><span class="sxs-lookup"><span data-stu-id="449e8-107">**Table Title**</span></span>

|<span data-ttu-id="449e8-108">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="449e8-108">**Property**</span></span>|<span data-ttu-id="449e8-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="449e8-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="449e8-110">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-111">Содержит тип адреса электронной почты пользователя обмена сообщениями, например SMTP.</span><span class="sxs-lookup"><span data-stu-id="449e8-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="449e8-112">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-113">Содержит имя отображения для данного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="449e8-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="449e8-114">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-115">Содержит значение, используемого для связи значка с определенной строкой таблицы.</span><span class="sxs-lookup"><span data-stu-id="449e8-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="449e8-116">**PR_EMAIL_ADDRESS** [(PidTagEmailAddress)](pidtagemailaddress-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-117">Содержит адрес электронной почты пользователя обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="449e8-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="449e8-118">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-119">Содержит идентификатор записи MAPI, используемый для открытия и редактирования свойств определенного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="449e8-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="449e8-120">**PR_OBJECT_TYPE** [(PidTagObjectType)](pidtagobjecttype-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-121">Содержит тип объекта.</span><span class="sxs-lookup"><span data-stu-id="449e8-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="449e8-122">**PR_SEARCH_KEY** [(PidTagSearchKey)](pidtagsearchkey-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="449e8-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="449e8-123">Содержит двухсопоставимый ключ, который определяет связанные объекты для поиска.</span><span class="sxs-lookup"><span data-stu-id="449e8-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

