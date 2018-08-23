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
ms.openlocfilehash: ceda6b1d551af973df08f8069d1eaf543085a375
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22574220"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="3cc09-103">Свойства получателей для всех сообщений</span><span class="sxs-lookup"><span data-stu-id="3cc09-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="3cc09-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="3cc09-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="3cc09-105">Следующие свойства обычно присутствуют для всех получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="3cc09-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="3cc09-106">**PR_EMAIL_ADDRESS** и **PR_SEARCH_KEY** являются необязательными. все другие свойства являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="3cc09-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="3cc09-107">**Заголовок таблицы**</span><span class="sxs-lookup"><span data-stu-id="3cc09-107">**Table Title**</span></span>

|<span data-ttu-id="3cc09-108">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="3cc09-108">**Property**</span></span>|<span data-ttu-id="3cc09-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="3cc09-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="3cc09-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-111">Содержит тип адреса электронной почты, обмена мгновенными сообщениями пользователя, например SMTP.</span><span class="sxs-lookup"><span data-stu-id="3cc09-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="3cc09-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-113">Содержит отображаемое имя для данного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="3cc09-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="3cc09-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-115">Содержит значение, используемое для сопоставления значка с конкретной строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="3cc09-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="3cc09-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-117">Содержит адрес электронной почты пользователя обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="3cc09-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="3cc09-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-119">Содержит идентификатор запись MAPI, используемый для открытия и изменения свойств конкретного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="3cc09-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="3cc09-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-121">Содержит тип объекта.</span><span class="sxs-lookup"><span data-stu-id="3cc09-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="3cc09-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="3cc09-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="3cc09-123">Содержит двоичный сравнимые ключ, который определяет соответствующих объектов для поиска.</span><span class="sxs-lookup"><span data-stu-id="3cc09-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

