---
title: Реализация одноразовой таблицы поставщика
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
# <a name="implementing-a-provider-one-off-table"></a><span data-ttu-id="ca149-103">Реализация одноразовой таблицы поставщика</span><span class="sxs-lookup"><span data-stu-id="ca149-103">Implementing a Provider One-Off Table</span></span>

  
  
<span data-ttu-id="ca149-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="ca149-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="ca149-105">MAPI вызывает метод [иаблогон:: жетонеоффтабле](iablogon-getoneofftable.md) поставщика, когда пользователь клиентского приложения добавляет получателя в исходящее сообщение.</span><span class="sxs-lookup"><span data-stu-id="ca149-105">MAPI calls your provider's [IABLogon::GetOneOffTable](iablogon-getoneofftable.md) method when the user of a client application adds a recipient to an outgoing message.</span></span> <span data-ttu-id="ca149-106">Как правило, запрошенные типы адресов уникальны для системы обмена сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ca149-106">Typically, the types of addresses requested are unique to your messaging system.</span></span> <span data-ttu-id="ca149-107">Если поставщик поддерживает создание получателей, он должен предоставить одноразовую таблицу, предоставляющую шаблоны для каждого типа поддерживаемого адреса получателя.</span><span class="sxs-lookup"><span data-stu-id="ca149-107">If your provider supports recipient creation, it must supply a one-off table that exposes templates for every type of supported recipient address.</span></span> <span data-ttu-id="ca149-108">Если поставщик не поддерживает создание получателей, возвращайте МАПИ_Е_НО_СУППОРТ из вызова **жетонеоффтабле** .</span><span class="sxs-lookup"><span data-stu-id="ca149-108">If your provider does not support recipient creation, return MAPI_E_NO_SUPPORT from the **GetOneOffTable** call.</span></span> 
  
<span data-ttu-id="ca149-109">Как правило, Служба MAPI будет хранить одноразовую таблицу поставщика в течение всего времени существования сеанса, освобождая ее, только когда клиент вызывает метод [имапистатус:: валидатестате](imapistatus-validatestate.md) подсистемы или адресной книги.</span><span class="sxs-lookup"><span data-stu-id="ca149-109">MAPI will typically keep your provider's one-off table open for the lifetime of the session, releasing it only when a client calls either the subsystem's or address book's [IMAPIStatus::ValidateState](imapistatus-validatestate.md) method.</span></span> <span data-ttu-id="ca149-110">Регистры MAPI для уведомлений в этой таблице, чтобы при добавлении или удалении шаблонов эти изменения могли быть отражены для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ca149-110">MAPI registers for notifications on this table so that if templates are added or deleted, these changes can be reflected to the user.</span></span> 
  
 <span data-ttu-id="ca149-111">**Реализация Иаблогон:: Жетонеоффтабле**</span><span class="sxs-lookup"><span data-stu-id="ca149-111">**To implement IABLogon::GetOneOffTable**</span></span>
  
1. <span data-ttu-id="ca149-112">Проверьте значение параметра flags, _ulFlags_.</span><span class="sxs-lookup"><span data-stu-id="ca149-112">Check the value of the flags parameter,  _ulFlags_.</span></span> <span data-ttu-id="ca149-113">Если установлен флаг МАПИ_УНИКОДЕ, а поставщик не поддерживает Юникод, ошибки и возвращать МАПИ_Е_БАД_ЧАРВИДС.</span><span class="sxs-lookup"><span data-stu-id="ca149-113">If the MAPI_UNICODE flag is set and your provider does not support Unicode, fail and return MAPI_E_BAD_CHARWIDTH.</span></span> 
    
2. <span data-ttu-id="ca149-114">Проверьте, была ли уже создана одноразовая таблица поставщика.</span><span class="sxs-lookup"><span data-stu-id="ca149-114">Check if your provider's one-off table has already been created.</span></span> <span data-ttu-id="ca149-115">Так как одноразовые таблицы обычно статичны, поставщику никогда не придется выполнять процесс создания несколько раз.</span><span class="sxs-lookup"><span data-stu-id="ca149-115">Because one-off tables are typically static, your provider never has to go through the creation process more than once.</span></span> <span data-ttu-id="ca149-116">Если таблица уже существует, возвращается указатель на нее.</span><span class="sxs-lookup"><span data-stu-id="ca149-116">If a table already exists, return a pointer to it.</span></span> 
    
3. <span data-ttu-id="ca149-117">Если одна из таблиц еще не существует, вызовите **креатетабле** , чтобы создать ее.</span><span class="sxs-lookup"><span data-stu-id="ca149-117">If a one-off table does not yet exist, call **CreateTable** to create one.</span></span> 
    
4. <span data-ttu-id="ca149-118">Задайте следующие свойства для столбцов в строках таблицы:</span><span class="sxs-lookup"><span data-stu-id="ca149-118">Set the following properties for the columns in your table rows:</span></span>
    
  - <span data-ttu-id="ca149-119">**Пр_дисплай_наме** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) имя типа получателя, который может создать шаблон.</span><span class="sxs-lookup"><span data-stu-id="ca149-119">**PR_DISPLAY_NAME** ([PidTagDisplayName](pidtagdisplayname-canonical-property.md)) to the name of the type of recipient that the template can create.</span></span> 
    
  - <span data-ttu-id="ca149-120">**Пр_ентрид** ([PidTagEntryId](pidtagentryid-canonical-property.md)) на идентификатор записи для одноразового шаблона.</span><span class="sxs-lookup"><span data-stu-id="ca149-120">**PR_ENTRYID** ([PidTagEntryId](pidtagentryid-canonical-property.md)) to the entry identifier for the one-off template.</span></span>
    
  - <span data-ttu-id="ca149-121">**Пр_депс** ([PidTagDepth](pidtagdepth-canonical-property.md)), чтобы обозначить уровень иерархии в отображении односторонней таблицы.</span><span class="sxs-lookup"><span data-stu-id="ca149-121">**PR_DEPTH** ([PidTagDepth](pidtagdepth-canonical-property.md)) to indicate the hierarchy level in the one-off table display.</span></span>
    
  - <span data-ttu-id="ca149-122">**Пр_селектабле** ([PidTagSelectable](pidtagselectable-canonical-property.md)) в значение true, чтобы указать, представляет ли строка шаблон, и false в противном случае.</span><span class="sxs-lookup"><span data-stu-id="ca149-122">**PR_SELECTABLE** ([PidTagSelectable](pidtagselectable-canonical-property.md)) to TRUE to indicate if the row represents a template and FALSE otherwise.</span></span>
    
  - <span data-ttu-id="ca149-123">**Пр_аддртипе** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) на тип адреса, созданного шаблоном.</span><span class="sxs-lookup"><span data-stu-id="ca149-123">**PR_ADDRTYPE** ([PidTagAddressType](pidtagaddresstype-canonical-property.md)) to the type of address created by the template.</span></span>
    
  - <span data-ttu-id="ca149-124">**Пр_дисплай_типе** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) в дт_маилусер или другое значение, указывающее тип отображения для шаблона.</span><span class="sxs-lookup"><span data-stu-id="ca149-124">**PR_DISPLAY_TYPE** ([PidTagDisplayType](pidtagdisplaytype-canonical-property.md)) to DT_MAILUSER or another value that indicates the type of display for the template.</span></span>
    
  - <span data-ttu-id="ca149-125">**Пр_инстанце_кэй** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) на уникальное двоичное значение.</span><span class="sxs-lookup"><span data-stu-id="ca149-125">**PR_INSTANCE_KEY** ([PidTagInstanceKey](pidtaginstancekey-canonical-property.md)) to a unique binary value.</span></span> 
    
5. <span data-ttu-id="ca149-126">Call [итабледата:: хрмодифиров](itabledata-hrmodifyrow.md) для непосредственного изменения таблицы.</span><span class="sxs-lookup"><span data-stu-id="ca149-126">Call [ITableData::HrModifyRow](itabledata-hrmodifyrow.md) to modify the table directly.</span></span> 
    
6. <span data-ttu-id="ca149-127">Call [итабледата:: хржетвиев](itabledata-hrgetview.md) , чтобы создать реализацию интерфейса **IMAPITable** , чтобы вернуться к вызывающему абоненту.</span><span class="sxs-lookup"><span data-stu-id="ca149-127">Call [ITableData::HrGetView](itabledata-hrgetview.md) to create an **IMAPITable** interface implementation to return to the caller.</span></span> 
    

