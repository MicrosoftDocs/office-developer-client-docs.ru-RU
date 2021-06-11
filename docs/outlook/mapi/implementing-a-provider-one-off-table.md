---
title: Реализация таблицы One-Off поставщика
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 023686702b76b5b29acf4304fcfdb3377e8cfcff
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33436295"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="968aa-103">Реализация таблицы One-Off поставщика</span><span class="sxs-lookup"><span data-stu-id="968aa-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="968aa-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="968aa-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="968aa-105">MAPI вызывает метод [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) поставщика, когда пользователь клиентского приложения добавляет получателя в исходяние сообщение.</span><span class="sxs-lookup"><span data-stu-id="968aa-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="968aa-106">Как правило, типы запрашиваемого адреса уникальны для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="968aa-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="968aa-107">Если поставщик поддерживает создание получателей, он должен предоставить разовую таблицу, которая предоставляет шаблоны для каждого типа поддерживаемого адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="968aa-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="968aa-108">Если поставщик не поддерживает создание получателей, MAPI_E_NO_SUPPORT из **вызова GetOneOffTable.**</span><span class="sxs-lookup"><span data-stu-id="968aa-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="968aa-109">MapI обычно будет держать разовую таблицу поставщика открытой на весь срок действия сеанса, выпуская ее только тогда, когда клиент вызывает метод [IMAPIStatus::ValidateState](imapistatus-validatestate.md) подсистемы или адресной книги.</span><span class="sxs-lookup"><span data-stu-id="968aa-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="968aa-110">MAPI регистрирует уведомления на этой таблице, чтобы при добавлении или удалении шаблонов эти изменения могли быть отражены пользователю.</span><span class="sxs-lookup"><span data-stu-id="968aa-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="968aa-111">**Реализация IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="968aa-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="968aa-112">Проверьте значение параметра флаги  _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="968aa-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="968aa-113">Если флаг MAPI_UNICODE установлен и поставщик не поддерживает Unicode, сбой и возвращение MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="968aa-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="968aa-114">Проверьте, создана ли разовая таблица поставщика.</span><span class="sxs-lookup"><span data-stu-id="968aa-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="968aa-115">Поскольку разовые таблицы обычно являются статичными, поставщику никогда не нужно проходить процесс создания более одного раза.</span><span class="sxs-lookup"><span data-stu-id="968aa-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="968aa-116">Если таблица уже существует, верни указатель в нее.</span><span class="sxs-lookup"><span data-stu-id="968aa-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="968aa-117">Если разовая таблица еще не существует, позвоните **в CreateTable,** чтобы создать ее.</span><span class="sxs-lookup"><span data-stu-id="968aa-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="968aa-118">Установите следующие свойства для столбцов в строках таблицы:</span><span class="sxs-lookup"><span data-stu-id="968aa-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="968aa-119">**PR_DISPLAY_NAME** [(PidTagDisplayName)](pidtagdisplayname-canonical-property.md)имени типа получателя, который может создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="968aa-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="968aa-120">**PR_ENTRYID** [(PidTagEntryId)](pidtagentryid-canonical-property.md)к идентификатору записи для разового шаблона.</span><span class="sxs-lookup"><span data-stu-id="968aa-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="968aa-121">**PR_DEPTH** [(PidTagDepth),](pidtagdepth-canonical-property.md)чтобы указать уровень иерархии в разовом дисплее таблицы.</span><span class="sxs-lookup"><span data-stu-id="968aa-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="968aa-122">**PR_SELECTABLE** [(PidTagSelectable)](pidtagselectable-canonical-property.md)для TRUE, чтобы указать, представляет ли строка шаблон, а false — иначе.</span><span class="sxs-lookup"><span data-stu-id="968aa-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="968aa-123">**PR_ADDRTYPE** [(PidTagAddressType)](pidtagaddresstype-canonical-property.md)для типа адреса, созданного шаблоном.</span><span class="sxs-lookup"><span data-stu-id="968aa-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="968aa-124">**PR_DISPLAY_TYPE** [(PidTagDisplayType)](pidtagdisplaytype-canonical-property.md)для DT_MAILUSER или другого значения, которое указывает тип отображения шаблона.</span><span class="sxs-lookup"><span data-stu-id="968aa-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="968aa-125">**PR_INSTANCE_KEY** [(PidTagInstanceKey)](pidtaginstancekey-canonical-property.md)к уникальному двоичному значению.</span><span class="sxs-lookup"><span data-stu-id="968aa-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="968aa-126">Вызов [ITableData::HrModifyRow,](itabledata-hrmodifyrow.md) чтобы изменить таблицу напрямую.</span><span class="sxs-lookup"><span data-stu-id="968aa-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="968aa-127">Вызов [ITableData::HrGetView](itabledata-hrgetview.md) для создания **реализации интерфейса IMAPITable,** чтобы вернуться к вызываемой.</span><span class="sxs-lookup"><span data-stu-id="968aa-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

