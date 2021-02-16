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
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33435266"
---
# <a name="display-table-implementation"></a><span data-ttu-id="66bc8-103">Реализация таблицы отображения</span><span class="sxs-lookup"><span data-stu-id="66bc8-103">Display Table Implementation</span></span>

  
  
<span data-ttu-id="66bc8-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="66bc8-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="66bc8-105">Таблица отображения используется для отображения листа свойств, специального диалоговое окно, состоящее из одной или нескольких страниц свойств вкладок, предназначенных для отображения и, возможно, редактирования одного или нескольких свойств.</span><span class="sxs-lookup"><span data-stu-id="66bc8-105">A display table is used to show a property sheet, a special dialog box that is composed of one or more tabbed property pages dedicated to displaying and possibly editing one or more properties.</span></span> <span data-ttu-id="66bc8-106">С каждой таблицей отображения связана реализация [интерфейса IMAPIProp.](iattachimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="66bc8-106">Associated with every display table is an [IAttach : IMAPIProp](iattachimapiprop.md) interface implementation.</span></span> <span data-ttu-id="66bc8-107">Реализация [IMAPIProp](imapipropiunknown.md) поддерживает данные свойств, представленные на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="66bc8-107">The [IMAPIProp](imapipropiunknown.md) implementation maintains the property data that is presented in the property sheet.</span></span> 
  
<span data-ttu-id="66bc8-108">Строки в таблице отображения представляют элементы управления на листе свойств.</span><span class="sxs-lookup"><span data-stu-id="66bc8-108">The rows in a display table represent the controls in the property sheet.</span></span> <span data-ttu-id="66bc8-109">Большинство элементов управления можно связывать со свойствами, поддерживаемые реализацией **IMAPIProp.**</span><span class="sxs-lookup"><span data-stu-id="66bc8-109">Most controls can be associated with properties maintained with the **IMAPIProp** implementation.</span></span> <span data-ttu-id="66bc8-110">Когда пользователь изменяет значение изменимого управления, соответствующее свойство обновляется.</span><span class="sxs-lookup"><span data-stu-id="66bc8-110">When a user changes the value of a modifiable control, the corresponding property is updated.</span></span> 
  
<span data-ttu-id="66bc8-111">Столбцы в таблице отображения представляют свойства этого управления, такие как его положение на листе свойств, его тип, связанная структура и идентификатор.</span><span class="sxs-lookup"><span data-stu-id="66bc8-111">The columns in a display table represent properties of the control, such as its position in the property sheet, its type, associated structure, and identifier.</span></span> <span data-ttu-id="66bc8-112">Полный список необходимых столбцов таблицы отображения см. в [статье "Таблицы отображения".](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="66bc8-112">For a complete list of required display table columns, see [Display Tables](display-tables.md).</span></span>
  
<span data-ttu-id="66bc8-113">MAPI отображает лист свойств для пользователя клиентского приложения, считывая значения свойств из реализации **IMAPIProp,** связанной с таблицей отображения или непосредственно из таблицы отображения.</span><span class="sxs-lookup"><span data-stu-id="66bc8-113">MAPI displays a property sheet to the user of a client application by reading property values from the **IMAPIProp** implementation associated with the display table or from the display table directly.</span></span> <span data-ttu-id="66bc8-114">Когда пользователь работает с листом свойств, меняя значения элементов управления, MAPI вызывает [IMAPIProp::SetProps,](imapiprop-setprops.md) чтобы сохранить измененный элемент управления, если установлен флаг DT_SET_IMMEDIATE элемент управления.</span><span class="sxs-lookup"><span data-stu-id="66bc8-114">As the user works with the property sheet, changing values in the controls, MAPI calls [IMAPIProp::SetProps](imapiprop-setprops.md) to save a changed control if the control's DT_SET_IMMEDIATE flag is set.</span></span> <span data-ttu-id="66bc8-115">Для элементов управления без DT_SET_IMMEDIATE флага изменения свойств сохраняются, когда пользователь зажимает диалоговое окно, нажимая кнопку "ОК" или **"Применить** сейчас". </span><span class="sxs-lookup"><span data-stu-id="66bc8-115">For controls without the DT_SET_IMMEDIATE flag set, changes to properties are saved when the user dismisses the dialog box by clicking the **OK** or **Apply Now** button.</span></span> <span data-ttu-id="66bc8-116">При нажатии одной  из этих кнопок или кнопки "Отмена" MAPI удаляет лист свойств из представления.</span><span class="sxs-lookup"><span data-stu-id="66bc8-116">When either of these buttons or the **Cancel** button is clicked, MAPI removes the property sheet from view.</span></span> 
  
<span data-ttu-id="66bc8-117">MAPI получает доступ к таблице отображения, вызывая метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) в реализации **IMAPIProp** и запрашивая свойство **PR_DETAILS_TABLE** ([PidTagDetailsTable)](pidtagdetailstable-canonical-property.md)или наследуя его в вызове MAPI, например [IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md).</span><span class="sxs-lookup"><span data-stu-id="66bc8-117">MAPI gains access to your display table either by calling the [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method in the **IMAPIProp** implementation and requesting the **PR_DETAILS_TABLE** ([PidTagDetailsTable](pidtagdetailstable-canonical-property.md)) property or by inheriting it in a call that you have made to MAPI, such as [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md).</span></span>
  
<span data-ttu-id="66bc8-118">Первый способ доступа используется, когда поставщикам адресных книг предложено показать сведения о пользователях сообщений или списках рассылки.</span><span class="sxs-lookup"><span data-stu-id="66bc8-118">The first access technique is used when address book providers are asked to show details about messaging users or distribution lists.</span></span> <span data-ttu-id="66bc8-119">Происходит следующая обработка:</span><span class="sxs-lookup"><span data-stu-id="66bc8-119">The following processing occurs:</span></span>
  
1. <span data-ttu-id="66bc8-120">Клиент вызывает метод [IAddrBook::D etails.](iaddrbook-details.md)</span><span class="sxs-lookup"><span data-stu-id="66bc8-120">A client calls the [IAddrBook::Details](iaddrbook-details.md) method.</span></span> 
    
2. <span data-ttu-id="66bc8-121">MAPI вызывает метод [IABLogon::OpenEntry](iablogon-openentry.md) поставщика адресной книги для доступа к пользователю обмена сообщениями, который представляет выбранную запись.</span><span class="sxs-lookup"><span data-stu-id="66bc8-121">MAPI calls the address book provider's [IABLogon::OpenEntry](iablogon-openentry.md) method to access the messaging user that represents the selected entry.</span></span> 
    
3. <span data-ttu-id="66bc8-122">MAPI вызывает метод [IMAPIProp::OpenProperty](imapiprop-openproperty.md) пользователя обмена сообщениями для получения **свойства PR_DETAILS_TABLE,** отображаемой таблицы для диалоговых окна сведений.</span><span class="sxs-lookup"><span data-stu-id="66bc8-122">MAPI calls the messaging user's [IMAPIProp::OpenProperty](imapiprop-openproperty.md) method to retrieve the **PR_DETAILS_TABLE** property, the display table for the details dialog box.</span></span> 
    
4. <span data-ttu-id="66bc8-123">MAPI отображает диалоговое окно с обработкой взаимодействия пользователя с информацией и удаляет его после завершения работы пользователя.</span><span class="sxs-lookup"><span data-stu-id="66bc8-123">MAPI displays the dialog box, handling the user's interaction with the information, and removes it when the user has finished.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="66bc8-124">См. также</span><span class="sxs-lookup"><span data-stu-id="66bc8-124">See also</span></span>



[<span data-ttu-id="66bc8-125">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="66bc8-125">MAPI Service Providers</span></span>](mapi-service-providers.md)

