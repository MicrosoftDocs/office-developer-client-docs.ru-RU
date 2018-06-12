---
title: Реализация таблица отображения
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: eb17675a-35e0-4545-b394-789d343510aa
description: '���� ���������� ���������: 23 ���� 2011 �.'
ms.openlocfilehash: 07ad94c423c3be425dc905dc578f55ad2c467a95
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19808298"
---
# <a name="display-table-implementation"></a><span data-ttu-id="653c5-103">Реализация таблица отображения</span><span class="sxs-lookup"><span data-stu-id="653c5-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="653c5-104">**Применимо к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="653c5-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="653c5-105">Таблица отображения используется для отображения свойств специальных диалоговое окно, которое состоит из одной или нескольких страниц с вкладками свойство, выделенным для отображения и возможно редактирование одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="653c5-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="653c5-106">Связанные с каждой отображения таблица — [IAttach: IMAPIProp](iattachimapiprop.md) реализация интерфейса.</span><span class="sxs-lookup"><span data-stu-id="653c5-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="653c5-107">Реализация [IMAPIProp](imapipropiunknown.md) поддерживает свойство данные, представленные в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="653c5-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="653c5-108">Строки в таблице отображения представляют элементы управления в окне свойств.</span><span class="sxs-lookup"><span data-stu-id="653c5-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="653c5-109">Элементы управления могут быть связаны со свойствами, задаваемые с реализацией **IMAPIProp** .</span><span class="sxs-lookup"><span data-stu-id="653c5-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="653c5-110">Когда пользователь изменяет значение можно изменить элемент управления, обновляется соответствующего свойства.</span><span class="sxs-lookup"><span data-stu-id="653c5-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="653c5-111">Столбцы в таблице отображения представления свойств элемента управления, такие как положение в окно свойств, его тип, связанную с ней структуру и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="653c5-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="653c5-112">Полный список необходимых отображения столбцов таблицы содержатся в разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="653c5-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="653c5-113">MAPI отображает окно свойств для пользователя из клиентского приложения, прочитав статью значения свойств из реализации **IMAPIProp** , связанный с таблицей отображения или в таблице отображения напрямую.</span><span class="sxs-lookup"><span data-stu-id="653c5-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="653c5-114">Как пользователь работает со страницы свойств, изменяя значения в элементах управления, MAPI вызывает [IMAPIProp::SetProps](imapiprop-setprops.md) , чтобы сохранить измененный элемент управления, если значение флага DT_SET_IMMEDIATE элемента управления.</span><span class="sxs-lookup"><span data-stu-id="653c5-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="653c5-115">Для элементов управления без установленного флага DT_SET_IMMEDIATE изменения свойств сохраняются, когда пользователь закрывает диалоговое окно, нажав кнопку **ОК** или **Применить** .</span><span class="sxs-lookup"><span data-stu-id="653c5-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="653c5-116">При нажатии любой из этих кнопок или кнопку **Отмена** MAPI удаляет окно свойств из представления.</span><span class="sxs-lookup"><span data-stu-id="653c5-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="653c5-117">MAPI получает доступ к таблице отображения путем вызова метода [IMAPIProp::OpenProperty](imapiprop-openproperty.md) в реализации **IMAPIProp** и разрешения на запрос свойства **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) или путем наследования его в вызов, внесенные в MAPI, такие как [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="653c5-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="653c5-118">Первый способ доступа используется, если запрос поставщиками адресной книги для отображения сведений о системы обмена сообщениями пользователи или списки рассылки.</span><span class="sxs-lookup"><span data-stu-id="653c5-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="653c5-119">Обработка следующие события:</span><span class="sxs-lookup"><span data-stu-id="653c5-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="653c5-120">Клиент вызывает метод [IAddrBook::Details](iaddrbook-details.md) .</span><span class="sxs-lookup"><span data-stu-id="653c5-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="653c5-121">MAPI вызывает метод [IABLogon::OpenEntry](iablogon-openentry.md) поставщик адресной книги для доступа к обмена сообщениями пользователя, который представляет элемент, выбранный.</span><span class="sxs-lookup"><span data-stu-id="653c5-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="653c5-122">MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) обмена сообщениями пользователя для получения свойства **PR_DETAILS_TABLE** в таблице отображения диалогового окна сведений.</span><span class="sxs-lookup"><span data-stu-id="653c5-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="653c5-123">MAPI отображает диалоговое окно, взаимодействия с пользователем с данными и удаляет его после завершения работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="653c5-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="653c5-124">См. также</span><span class="sxs-lookup"><span data-stu-id="653c5-124">See also</span></span>



[<span data-ttu-id="653c5-125">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="653c5-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

