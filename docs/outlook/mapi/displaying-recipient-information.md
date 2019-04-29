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
# <a name="displaying-recipient-information"></a><span data-ttu-id="350f8-103">Отображение сведений о получателях</span><span class="sxs-lookup"><span data-stu-id="350f8-103">Displaying recipient information</span></span>

<span data-ttu-id="350f8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="350f8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="350f8-105">MAPI предоставляет общее диалоговое окно для отображения сведений о получателях.</span><span class="sxs-lookup"><span data-stu-id="350f8-105">MAPI provides a common dialog box for showing recipient details.</span></span> <span data-ttu-id="350f8-106">Диалоговое окно "сведения" создается из таблицы отображения и реализации **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="350f8-106">The details dialog box is created from a display table and an **IMAPIProp** implementation.</span></span> <span data-ttu-id="350f8-107">В таблице отображения описывается внешний вид отображения сведений и реализация **IMAPIProp** управляет данными для получателя.</span><span class="sxs-lookup"><span data-stu-id="350f8-107">The display table describes the appearance of the details display and the **IMAPIProp** implementation controls the data for the recipient.</span></span> <span data-ttu-id="350f8-108">Поставщик несет ответственность за предоставление таблицы отображения и реализации **IMAPIProp** для каждого получателя.</span><span class="sxs-lookup"><span data-stu-id="350f8-108">Your provider is responsible for supplying the display table and the **IMAPIProp** implementation for each recipient.</span></span> 
  
<span data-ttu-id="350f8-109">Простейший способ создания таблицы отображения заключается в определении структуры [дтпаже](dtpage.md) и вызове [буилддисплайтабле](builddisplaytable.md).</span><span class="sxs-lookup"><span data-stu-id="350f8-109">The easiest way to create the display table is to define a [DTPAGE](dtpage.md) structure and call [BuildDisplayTable](builddisplaytable.md).</span></span> <span data-ttu-id="350f8-110">Однако некоторые поставщики, а именно поставщики, предназначенные только для чтения, которые позволяют создавать одноразовых получателей, используют **ипропдата**.</span><span class="sxs-lookup"><span data-stu-id="350f8-110">However, some providers, specifically read-only providers that allow the creation of one-off recipients, use **IPropData**.</span></span> <span data-ttu-id="350f8-111">Реализация **IMAPIProp** может быть любым типом объекта Property.</span><span class="sxs-lookup"><span data-stu-id="350f8-111">The **IMAPIProp** implementation can be any type of property object.</span></span> 
  
<span data-ttu-id="350f8-112">Существует два метода вызова этого диалогового окна: [IAddrBook::D етаилс](iaddrbook-details.md) и [имаписуппорт::D етаилс](imapisupport-details.md).</span><span class="sxs-lookup"><span data-stu-id="350f8-112">There are two methods for invoking this dialog box: [IAddrBook::Details](iaddrbook-details.md) and [IMAPISupport::Details](imapisupport-details.md).</span></span> <span data-ttu-id="350f8-113">Когда поставщик вызывает один из этих методов для запроса сведений о получателе, MAPI сначала открывает получателя, вызывая метод [IMAPIContainer:: OpenEntry](imapicontainer-openentry.md) контейнера.</span><span class="sxs-lookup"><span data-stu-id="350f8-113">When your provider calls one of these methods to request details for a recipient, MAPI first opens the recipient by calling its container's [IMAPIContainer::OpenEntry](imapicontainer-openentry.md) method.</span></span> <span data-ttu-id="350f8-114">Затем вызывается метод получателя [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) для запроса свойства **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)).</span><span class="sxs-lookup"><span data-stu-id="350f8-114">Next it calls the recipient's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to request the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property.</span></span> <span data-ttu-id="350f8-115">**Пр_детаилс_табле** — это свойство, представляющее таблицу отображения сведений о получателе.</span><span class="sxs-lookup"><span data-stu-id="350f8-115">**PR_DETAILS_TABLE** is the property that represents a recipient's details display table.</span></span> 
  
<span data-ttu-id="350f8-116">Интерфейс [ипропдата: IMAPIProp](ipropdataimapiprop.md) можно использовать для отслеживания изменений в элементах управления "таблица отображения", как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="350f8-116">The [IPropData : IMAPIProp](ipropdataimapiprop.md) interface can be used to monitor changes on display table controls as described in the following procedure.</span></span> 
  
## <a name="monitor-changes-to-a-control"></a><span data-ttu-id="350f8-117">Отслеживание изменений элемента управления</span><span class="sxs-lookup"><span data-stu-id="350f8-117">Monitor changes to a control</span></span>
  
1. <span data-ttu-id="350f8-118">Прежде чем пользователь получит доступ к элементу управления, вызовите метод [ипропдата:: хрсетобжакцесс](ipropdata-hrsetobjaccess.md) , чтобы задать для элемента управления доступ к ипроп_клеан.</span><span class="sxs-lookup"><span data-stu-id="350f8-118">Before the user gains access to the control, call [IPropData::HrSetObjAccess](ipropdata-hrsetobjaccess.md) to set the control's access to IPROP_CLEAN.</span></span> 
    
2. <span data-ttu-id="350f8-119">Разрешить пользователю работать с диалоговым окном.</span><span class="sxs-lookup"><span data-stu-id="350f8-119">Allow the user to work with the dialog box.</span></span> 
    
3. <span data-ttu-id="350f8-120">По завершении работы пользователя вызовите метод [ипропдата:: хржетпропакцесс](ipropdata-hrgetpropaccess.md) , чтобы получить текущий уровень доступа элемента управления.</span><span class="sxs-lookup"><span data-stu-id="350f8-120">When the user has finished, call [IPropData::HrGetPropAccess](ipropdata-hrgetpropaccess.md) to retrieve the current access level of the control.</span></span> 
    
4. <span data-ttu-id="350f8-121">Если уровень доступа — ИПРОП_ДИРТИ, пользователь изменил элемент управления.</span><span class="sxs-lookup"><span data-stu-id="350f8-121">If the access level is IPROP_DIRTY, the user has modified the control.</span></span> <span data-ttu-id="350f8-122">Поставщик должен выполнять следующие действия:</span><span class="sxs-lookup"><span data-stu-id="350f8-122">Your provider should:</span></span>
    
   - <span data-ttu-id="350f8-123">Call [ипропдата:: хрсетпропакцесс](ipropdata-hrsetpropaccess.md) , чтобы установить уровень доступа обратно в ипроп_клеан.</span><span class="sxs-lookup"><span data-stu-id="350f8-123">Call [IPropData::HrSetPropAccess](ipropdata-hrsetpropaccess.md) to set the access level back to IPROP_CLEAN.</span></span> 
    
   - <span data-ttu-id="350f8-124">ВыЗовите метод [IMAPIProp:: и Prop](imapiprop-getprops.md) объекта данных свойства, чтобы получить свойство Changed и обновить его, вызвав [IMAPIProp:: SetProps](imapiprop-setprops.md).</span><span class="sxs-lookup"><span data-stu-id="350f8-124">Call the property data object's [IMAPIProp::GetProps](imapiprop-getprops.md) method to retrieve the changed property and update it by calling [IMAPIProp::SetProps](imapiprop-setprops.md).</span></span>
    
5. <span data-ttu-id="350f8-125">Если уровень доступа по-прежнему ИПРОП_КЛЕАН, элемент управления не был изменен.</span><span class="sxs-lookup"><span data-stu-id="350f8-125">If the access level is still IPROP_CLEAN, the control has not been modified.</span></span> 
    
<span data-ttu-id="350f8-126">Дополнительные сведения о создании таблиц отображения можно узнать в статье [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="350f8-126">For more information about creating display tables, see [Display Tables](display-tables.md).</span></span>
  

