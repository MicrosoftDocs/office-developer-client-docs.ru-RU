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
ms.openlocfilehash: d92e9dbbf594dffc3dbf5bbf271fc80a0abed68e
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812095"
---
# <a name="recipient-properties-for-all-messages"></a><span data-ttu-id="90228-103">Свойства получателей для всех сообщений</span><span class="sxs-lookup"><span data-stu-id="90228-103">Recipient Properties for All Messages</span></span>

  
  
<span data-ttu-id="90228-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="90228-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="90228-105">Следующие свойства обычно присутствуют для всех получателей сообщений.</span><span class="sxs-lookup"><span data-stu-id="90228-105">The following properties are typically present for all message recipients.</span></span> <span data-ttu-id="90228-106">**PR_EMAIL_ADDRESS** и **PR_SEARCH_KEY** являются необязательными. все другие свойства являются обязательными.</span><span class="sxs-lookup"><span data-stu-id="90228-106">**PR_EMAIL_ADDRESS** and **PR_SEARCH_KEY** are optional; all of the other properties are required.</span></span> 
  
<span data-ttu-id="90228-107">**Заголовок таблицы**</span><span class="sxs-lookup"><span data-stu-id="90228-107">**Table Title**</span></span>

|<span data-ttu-id="90228-108">**Свойство**</span><span class="sxs-lookup"><span data-stu-id="90228-108">**Property**</span></span>|<span data-ttu-id="90228-109">**Описание**</span><span class="sxs-lookup"><span data-stu-id="90228-109">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="90228-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-110">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-111">Содержит тип адреса электронной почты, обмена мгновенными сообщениями пользователя, например SMTP.</span><span class="sxs-lookup"><span data-stu-id="90228-111">Contains the messaging user's email address type, such as SMTP.</span></span>  <br/> |
|<span data-ttu-id="90228-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-112">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-113">Содержит отображаемое имя для данного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="90228-113">Contains the display name for a given MAPI object.</span></span>  <br/> |
|<span data-ttu-id="90228-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-114">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-115">Содержит значение, используемое для сопоставления значка с конкретной строки таблицы.</span><span class="sxs-lookup"><span data-stu-id="90228-115">Contains a value used to associate an icon with a particular row of a table.</span></span>  <br/> |
|<span data-ttu-id="90228-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-116">**PR_EMAIL_ADDRESS** ([PidTagEmailAddress](pidtagemailaddress-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-117">Содержит адрес электронной почты пользователя обмена мгновенными сообщениями.</span><span class="sxs-lookup"><span data-stu-id="90228-117">Contains the messaging user's email address.</span></span>  <br/> |
|<span data-ttu-id="90228-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-118">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-119">Содержит идентификатор запись MAPI, используемый для открытия и изменения свойств конкретного объекта MAPI.</span><span class="sxs-lookup"><span data-stu-id="90228-119">Contains a MAPI entry identifier used to open and edit properties of a particular MAPI object.</span></span>  <br/> |
|<span data-ttu-id="90228-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-120">**PR_OBJECT_TYPE** ([PidTagObjectType](pidtagobjecttype-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-121">Содержит тип объекта.</span><span class="sxs-lookup"><span data-stu-id="90228-121">Contains the type of an object.</span></span>  <br/> |
|<span data-ttu-id="90228-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span><span class="sxs-lookup"><span data-stu-id="90228-122">**PR_SEARCH_KEY** ([PidTagSearchKey](pidtagsearchkey-canonical-property.md))</span></span>  <br/> |<span data-ttu-id="90228-123">Содержит двоичный сравнимые ключ, который определяет соответствующих объектов для поиска.</span><span class="sxs-lookup"><span data-stu-id="90228-123">Contains a binary-comparable key that identifies correlated objects for a search.</span></span>  <br/> |
   

