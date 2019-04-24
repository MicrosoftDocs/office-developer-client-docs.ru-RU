---
title: Реализация таблицы отображения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 6990e32445083c3465693df2c1a3d40b980853c4
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32339951"
---
# <a name="display-table-implementation"></a><span data-ttu-id="c7f23-103">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="c7f23-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="c7f23-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="c7f23-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="c7f23-105">Таблица отображения используется для отображения страницы свойств, специального диалогового окна, которое состоит из одной или нескольких страниц свойств с вкладками, выделенных для отображения и, возможно, редактирования одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="c7f23-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="c7f23-106">Связанная со всеми таблицами отображения — это реализация интерфейса [иаттач: IMAPIProp](iattachimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="c7f23-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="c7f23-107">Реализация [IMAPIProp](imapipropiunknown.md) поддерживает данные свойств, которые представлены на странице свойств.</span><span class="sxs-lookup"><span data-stu-id="c7f23-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="c7f23-108">Строки в таблице отображения представляют элементы управления в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="c7f23-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="c7f23-109">Большинство элементов управления могут быть связаны со свойствами, которые поддерживаются реализацией **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="c7f23-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="c7f23-110">Когда пользователь изменяет значение изменяемого элемента управления, соответствующее свойство обновляется.</span><span class="sxs-lookup"><span data-stu-id="c7f23-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="c7f23-111">Столбцы в таблице отображения представляют свойства элемента управления, такие как его положение в таблице свойств, его тип, связанную структуру и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="c7f23-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="c7f23-112">Полный список обязательных столбцов таблицы отображения приведен в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="c7f23-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="c7f23-113">MAPI отображает страницу свойств для пользователя клиентского приложения, считывая значения свойств из реализации **IMAPIProp** , связанной с таблицей отображения или непосредственно из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="c7f23-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="c7f23-114">Так как пользователь работает со страницей свойств, изменяя значения в элементах управления, MAPI вызывает [IMAPIProp:: SetProps](imapiprop-setprops.md) для сохранения измененного элемента управления, если установлен флаг дт_сет_иммедиате элемента управления.</span><span class="sxs-lookup"><span data-stu-id="c7f23-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="c7f23-115">Для элементов управления без установленного флага ДТ_СЕТ_ИММЕДИАТЕ изменения свойств сохраняются, когда пользователь закрывает диалоговое окно, нажав кнопку **ОК** или **Применить сейчас** .</span><span class="sxs-lookup"><span data-stu-id="c7f23-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="c7f23-116">Когда вы нажимаете любую из этих кнопок или кнопка **Cancel (Отмена** ), MAPI Удаляет страницу свойств из представления.</span><span class="sxs-lookup"><span data-stu-id="c7f23-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="c7f23-117">MAPI получает доступ к таблице отображения, вызывая метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) в реализации **IMAPIProp** и запрашивает свойство **пр_детаилс_табле** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) или наследуя его в элементе вызов, выполненный для MAPI, например [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="c7f23-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="c7f23-118">Первый способ доступа используется при запросе поставщиков адресных книг для отображения сведений о пользователях системы обмена сообщениями или списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="c7f23-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="c7f23-119">Выполняется следующая обработка:</span><span class="sxs-lookup"><span data-stu-id="c7f23-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="c7f23-120">Клиент вызывает метод [IAddrBook::D етаилс](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="c7f23-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="c7f23-121">MAPI вызывает метод [иаблогон:: OpenEntry](iablogon-openentry.md) поставщика адресных книг для доступа к пользователю обмена сообщениями, представляющему выбранную запись.</span><span class="sxs-lookup"><span data-stu-id="c7f23-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="c7f23-122">MAPI вызывает метод [IMAPIProp:: опенпроперти](imapiprop-openproperty.md) пользователя обмена сообщениями для получения свойства **пр_детаилс_табле** , таблицы отображения для диалогового окна "сведения".</span><span class="sxs-lookup"><span data-stu-id="c7f23-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="c7f23-123">MAPI отображает диалоговое окно, обрабатывает взаимодействие пользователя с данными и удаляет его после завершения работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="c7f23-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="c7f23-124">См. также</span><span class="sxs-lookup"><span data-stu-id="c7f23-124">See also</span></span>



[<span data-ttu-id="c7f23-125">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="c7f23-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

