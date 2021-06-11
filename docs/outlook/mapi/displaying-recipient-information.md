---
title: Отображение сведений о получателях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: e1c31e5edf702dd8f172f67e7055a96ae4cfff1c
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33412957"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="689b0-103">Отображение сведений о получателях</span><span class="sxs-lookup"><span data-stu-id="689b0-103">Displaying recipient information</span></span>

<span data-ttu-id="689b0-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="689b0-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="689b0-105">MAPI предоставляет общий диалоговое окно для демонстрации сведений о получателе.</span><span class="sxs-lookup"><span data-stu-id="689b0-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="689b0-106">Диалоговое окно с подробными сведениями создается из таблицы отображения и **реализации IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="689b0-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="689b0-107">В таблице отображения описывается внешний вид отображения сведений, а реализация **IMAPIProp** управляет данными для получателя.</span><span class="sxs-lookup"><span data-stu-id="689b0-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="689b0-108">Поставщик отвечает за поставку таблицы отображения и **реализацию IMAPIProp** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="689b0-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="689b0-109">Самый простой способ создания таблицы отображения — определить структуру [DTPAGE](dtpage.md) и вызвать [BuildDisplayTable.](builddisplaytable.md)</span><span class="sxs-lookup"><span data-stu-id="689b0-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="689b0-110">Однако некоторые поставщики, в частности поставщики только для чтения, которые позволяют создавать разных получателей, используют **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="689b0-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="689b0-111">Реализация **IMAPIProp может** быть любым типом объекта свойства.</span><span class="sxs-lookup"><span data-stu-id="689b0-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="689b0-112">Для этого диалоговое окно можно использовать два метода: [IAddrBook::D etails](iaddrbook-details.md) и [IMAPISupport::D etails](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="689b0-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="689b0-113">Когда поставщик вызывает один из этих методов для запроса сведений для получателя, MAPI сначала открывает получателя, вызывая его метод [IMAPIContainer::OpenEntry.](imapicontainer-openentry.md)</span><span class="sxs-lookup"><span data-stu-id="689b0-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="689b0-114">Далее он вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) для запроса **свойства PR_DETAILS_TABLE** [(PidTagDetailsTable).](pidtagdetailstable-canonical-property.md)</span><span class="sxs-lookup"><span data-stu-id="689b0-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="689b0-115">**PR_DETAILS_TABLE** является свойством, которое представляет таблицу отображения сведений получателя.</span><span class="sxs-lookup"><span data-stu-id="689b0-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="689b0-116">Интерфейс [IPropData : IMAPIProp](ipropdataimapiprop.md) можно использовать для мониторинга изменений в элементе управления таблицой отображения, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="689b0-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="689b0-117">Отслеживание изменений в области управления</span><span class="sxs-lookup"><span data-stu-id="689b0-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="689b0-118">Прежде чем пользователь получит доступ к нему, позвоните [в IPropData::HrSetObjAccess,](ipropdata-hrsetobjaccess.md) чтобы установить доступ к IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="689b0-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="689b0-119">Разрешить пользователю работать с диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="689b0-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="689b0-120">Когда пользователь закончит работу, позвоните [в IPropData::HrGetPropAccess,](ipropdata-hrgetpropaccess.md) чтобы получить текущий уровень доступа к данным управления.</span><span class="sxs-lookup"><span data-stu-id="689b0-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="689b0-121">Если уровень доступа IPROP_DIRTY, пользователь изменил управление.</span><span class="sxs-lookup"><span data-stu-id="689b0-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="689b0-122">Поставщик должен:</span><span class="sxs-lookup"><span data-stu-id="689b0-122">Your provider should:</span></span>
    
   - <span data-ttu-id="689b0-123">Вызов [IPropData::HrSetPropAccess,](ipropdata-hrsetpropaccess.md) чтобы установить уровень доступа к IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="689b0-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="689b0-124">Чтобы получить измененное свойство и обновить его, позвоните по методу [IMAPIProp::GetProps](imapiprop-getprops.md) объекта [IMAPIProp::SetProps.](imapiprop-setprops.md)</span><span class="sxs-lookup"><span data-stu-id="689b0-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="689b0-125">Если уровень доступа по-прежнему IPROP_CLEAN, управление не было изменено.</span><span class="sxs-lookup"><span data-stu-id="689b0-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="689b0-126">Дополнительные сведения о создании таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="689b0-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

