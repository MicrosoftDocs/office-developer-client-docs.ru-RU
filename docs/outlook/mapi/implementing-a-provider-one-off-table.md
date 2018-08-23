---
title: Реализация одноразовой таблицы поставщиков
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 8b0dcbfe-6bed-4fb8-a906-009f1d009055
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: f484174bd0a83c9bb874bec4896fe3dd925405c7
ms.sourcegitcommit: 0cf39e5382b8c6f236c8a63c6036849ed3527ded
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 08/23/2018
ms.locfileid: "22568240"
---
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="e02f5-103">Реализация одноразовой таблицы поставщиков</span><span class="sxs-lookup"><span data-stu-id="e02f5-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="e02f5-104">**Применимо к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="e02f5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="e02f5-105">MAPI вызывает метод [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) ваш поставщик, когда пользователь клиентское приложение добавляет получателя для исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="e02f5-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="e02f5-106">Как правило типы адресов запрошено являются уникальными для обмена сообщениями в системе.</span><span class="sxs-lookup"><span data-stu-id="e02f5-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="e02f5-107">Если ваш поставщик поддерживает создание получателей, оно должно поддерживать одноразовых таблица, в которой предоставляет шаблоны для каждого типа поддерживаемых адрес получателя.</span><span class="sxs-lookup"><span data-stu-id="e02f5-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="e02f5-108">Если ваш поставщик не поддерживает создание получателей, возвратите MAPI_E_NO_SUPPORT из **GetOneOffTable** вызова.</span><span class="sxs-lookup"><span data-stu-id="e02f5-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="e02f5-109">MAPI обычно будет закрывайте ваш поставщик одноразовых таблицы для сеанса, освобождая его только в том случае, если клиент вызывает либо подсистемы или адресной книги [IMAPIStatus::ValidateState](imapistatus-validatestate.md) метод.</span><span class="sxs-lookup"><span data-stu-id="e02f5-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="e02f5-110">MAPI регистрирует уведомлений на этой таблице, чтобы при добавлении или удалении шаблонов, эти изменения могут быть отражены для пользователя.</span><span class="sxs-lookup"><span data-stu-id="e02f5-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="e02f5-111">**Для реализации IABLogon::GetOneOffTable**</span><span class="sxs-lookup"><span data-stu-id="e02f5-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="e02f5-112">Проверьте значение параметра флаги, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="e02f5-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="e02f5-113">Если задан флаг MAPI_UNICODE и ваш поставщик не поддерживает Юникод, с ошибкой и возвращают MAPI_E_BAD_CHARWIDTH.</span><span class="sxs-lookup"><span data-stu-id="e02f5-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="e02f5-114">Установите флажок, если ваш поставщик одноразовых таблица еще создана.</span><span class="sxs-lookup"><span data-stu-id="e02f5-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="e02f5-115">Поскольку одноразовых таблиц, обычно static, ваш поставщик не может пройти через процесс создания более одного раза.</span><span class="sxs-lookup"><span data-stu-id="e02f5-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="e02f5-116">Если таблица уже существует, возвращает указатель на него.</span><span class="sxs-lookup"><span data-stu-id="e02f5-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="e02f5-117">Если одноразовых таблица еще не существует, вызовите **CreateTable** для его создания.</span><span class="sxs-lookup"><span data-stu-id="e02f5-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="e02f5-118">Задайте следующие свойства для столбцов в строк таблицы:</span><span class="sxs-lookup"><span data-stu-id="e02f5-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="e02f5-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) к имени типа получателя, который можно создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="e02f5-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="e02f5-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) с идентификатором записи для одноразовых шаблона.</span><span class="sxs-lookup"><span data-stu-id="e02f5-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="e02f5-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) для определения уровня иерархии в отображении одноразовых таблицы.</span><span class="sxs-lookup"><span data-stu-id="e02f5-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="e02f5-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) значение TRUE, чтобы указать, если строка представляет шаблон и значение FALSE в противном случае.</span><span class="sxs-lookup"><span data-stu-id="e02f5-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="e02f5-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) тип адреса, создаваемых в шаблоне.</span><span class="sxs-lookup"><span data-stu-id="e02f5-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="e02f5-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) DT_MAILUSER или другое значение, указывающее тип отображения для шаблона.</span><span class="sxs-lookup"><span data-stu-id="e02f5-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="e02f5-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) уникальный двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="e02f5-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="e02f5-126">Вызов [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) для изменения непосредственно в таблице.</span><span class="sxs-lookup"><span data-stu-id="e02f5-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="e02f5-127">Вызов [ITableData::HrGetView](itabledata-hrgetview.md) для создания реализация интерфейса **IMAPITable** , чтобы вернуться к вызывающему.</span><span class="sxs-lookup"><span data-stu-id="e02f5-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

