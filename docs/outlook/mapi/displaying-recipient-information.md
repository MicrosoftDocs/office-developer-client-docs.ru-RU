---
title: Отображение сведения о получателях
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 7ffec274-ee90-44c7-ab2e-7dfb502517a6
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 7071c05f6f59740163f97f840c7fa48d83bea815
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808329"
---
# <a name="displaying-recipient-information"></a><span data-ttu-id="45780-103">Отображение сведения о получателях</span><span class="sxs-lookup"><span data-stu-id="45780-103">Displaying recipient information</span></span>

<span data-ttu-id="45780-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="45780-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="45780-105">MAPI стандартным диалоговым окном служит для отображения сведения о получателе.</span><span class="sxs-lookup"><span data-stu-id="45780-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="45780-106">Диалоговое окно "Подробности" будет создан из таблицы отображения и реализацию **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="45780-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="45780-107">В таблице Отображаемое описание внешний вид отображения сведений и реализации **IMAPIProp** управляет данные для получателя.</span><span class="sxs-lookup"><span data-stu-id="45780-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="45780-108">Поставщик отвечает за предоставление в таблице отображения и реализации **IMAPIProp** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="45780-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="45780-109">Это самый простой способ создания таблицы отображения является определение структуры [DTPAGE](dtpage.md) и вызов [BuildDisplayTable](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="45780-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="45780-110">Тем не менее некоторые поставщики, а именно только для чтения поставщиков, которые разрешить создание одноразовых получателей используйте **IPropData**.</span><span class="sxs-lookup"><span data-stu-id="45780-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="45780-111">Реализация **IMAPIProp** может иметь любой тип свойства объекта.</span><span class="sxs-lookup"><span data-stu-id="45780-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="45780-112">Существует два метода для вызова этого диалогового окна: [IAddrBook::Details](iaddrbook-details.md) и [IMAPISupport::Details](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="45780-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="45780-113">Когда ваш поставщик вызывает один из следующих методов для запроса сведений для получателя, MAPI сначала открывает получателя путем вызова метода [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) его контейнера.</span><span class="sxs-lookup"><span data-stu-id="45780-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="45780-114">Затем вызывается метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) получателя для запроса свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="45780-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="45780-115">**PR_DETAILS_TABLE** — это свойство, представляющее таблица отображения сведений о получателя.</span><span class="sxs-lookup"><span data-stu-id="45780-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="45780-116">[IPropData: IMAPIProp](ipropdataimapiprop.md) интерфейс можно использовать для отслеживания изменений для отображения элементов управления в таблице, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="45780-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="45780-117">Отслеживание изменений для элемента управления</span><span class="sxs-lookup"><span data-stu-id="45780-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="45780-118">Прежде чем пользователь получает доступ к элементу управления, вызовите [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) , чтобы задать разрешения доступа IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="45780-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="45780-119">Предоставление пользователю возможности работы с диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="45780-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="45780-120">После завершения работы пользователя, вызовите [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) для получения текущего уровня доступа элемента управления.</span><span class="sxs-lookup"><span data-stu-id="45780-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="45780-121">Если уровень доступа IPROP_DIRTY, элемент управления был изменен пользователем.</span><span class="sxs-lookup"><span data-stu-id="45780-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="45780-122">Ваш поставщик выполнить следующие действия:</span><span class="sxs-lookup"><span data-stu-id="45780-122">Your provider should:</span></span>
    
   - <span data-ttu-id="45780-123">Вызовите [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) , чтобы задать доступ уровня вернуться к IPROP_CLEAN.</span><span class="sxs-lookup"><span data-stu-id="45780-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="45780-124">Вызов метода [IMAPIProp::GetProps](imapiprop-getprops.md) объект данных свойств для извлечения измененное свойство и обновления путем вызова [IMAPIProp::SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="45780-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="45780-125">Если уровень доступа по-прежнему IPROP_CLEAN, элемент управления не был изменен.</span><span class="sxs-lookup"><span data-stu-id="45780-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="45780-126">Дополнительные сведения о создании таблиц отображения видеть [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="45780-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

