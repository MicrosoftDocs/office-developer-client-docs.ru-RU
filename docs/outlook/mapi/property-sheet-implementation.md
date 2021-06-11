---
title: Реализация листа свойств
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: f3475206-0237-4b5b-8efd-abd5d5e0b6c3
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 3f1c6497a182231645691f669d8900d33b495503
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33430051"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="82bc3-103">Реализация листа свойств</span><span class="sxs-lookup"><span data-stu-id="82bc3-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="82bc3-104">**Область применения**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="82bc3-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="82bc3-105">Лист свойств — диалоговое окно для отображения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="82bc3-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="82bc3-106">Свойства могут быть только для чтения, что позволяет пользователю просматривать их или читать или писать, что позволяет пользователю вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="82bc3-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="82bc3-107">В листе свойств содержится одно или несколько перекрывающихся детских окон, называемых страницами.</span><span class="sxs-lookup"><span data-stu-id="82bc3-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="82bc3-108">Каждая страница содержит окна управления для настройки группы связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="82bc3-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="82bc3-109">Пользователи перемещаются со страницы на страницу, выбрав вкладку, которая выводит соответствующую страницу на первый план листа свойств.</span><span class="sxs-lookup"><span data-stu-id="82bc3-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="82bc3-110">Поставщики услуг должны реализовать лист свойств, отображает минимальный набор свойств, связанных с конфигурацией в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="82bc3-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="82bc3-111">Если вы позволите изменить эти свойства службы сообщений, вы можете разрешить пользователям клиентских приложений, например панели управления, вносить изменения или осуществлять изменения программным образом.</span><span class="sxs-lookup"><span data-stu-id="82bc3-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="82bc3-112">Реализация листов свойств для отображения и редактирования других типов свойств необязательна.</span><span class="sxs-lookup"><span data-stu-id="82bc3-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="82bc3-113">Как правило, в следующих ситуациях необходимо отобразить лист свойств:</span><span class="sxs-lookup"><span data-stu-id="82bc3-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="82bc3-114">При вызове клиентом объекта [IMAPIStatus::SettingsDialog используется метод IMAPIStatus::SettingsDialog.](imapistatus-settingsdialog.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="82bc3-115">Когда MAPI вызывает метод логона объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="82bc3-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="82bc3-116">Когда MAPI вызывает функцию точки входа для службы сообщений поставщика.</span><span class="sxs-lookup"><span data-stu-id="82bc3-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="82bc3-117">Поставщики транспорта также реализуют листы свойств для отображения свойств, связанных с вариантами сообщений, а поставщики адресных книг реализуют листы свойств для просмотра и редактирования подробных сведений о пользователях сообщений и списках рассылки, расширенных критериях поиска и шаблонах для ввода новых пользователей.</span><span class="sxs-lookup"><span data-stu-id="82bc3-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="82bc3-118">Для создания листа свойств можно использовать один из следующих трех методов:</span><span class="sxs-lookup"><span data-stu-id="82bc3-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="82bc3-119">Вручную, как и любое диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="82bc3-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="82bc3-120">С помощью общего управления листом свойств, предоставляемым в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="82bc3-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="82bc3-121">С помощью таблицы отображения MAPI.</span><span class="sxs-lookup"><span data-stu-id="82bc3-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="82bc3-122">Поставщики должны выбрать последний вариант (создать лист свойств с помощью таблицы отображения).</span><span class="sxs-lookup"><span data-stu-id="82bc3-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="82bc3-123">Это самый простой вариант, так как он устраняет необходимость работы с пользовательским Windows интерфейсом.</span><span class="sxs-lookup"><span data-stu-id="82bc3-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="82bc3-124">Чтобы реализовать лист свойств, построенный из таблицы отображения для свойств службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="82bc3-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="82bc3-125">Вызов [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md) чтобы открыть раздел в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="82bc3-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="82bc3-126">[Передай mapIUID](mapiuid.md) или NULL, чтобы открыть профильный раздел поставщика.</span><span class="sxs-lookup"><span data-stu-id="82bc3-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="82bc3-127">Вызов [CreateIProp для](createiprop.md) создания объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="82bc3-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="82bc3-128">Вызовите метод [IMAPIProp::CopyTo в разделе IMAPIProp::CopyTo,](imapiprop-copyto.md) чтобы скопировать все свойства раздела в объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="82bc3-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="82bc3-129">Создайте таблицу отображения, создав одну или несколько структур [DTPAGE,](dtpage.md) описывающие элементы управления, отображаемые на листе свойств и вызываемые функцией [BuildDisplayTable,](builddisplaytable.md) или реализуя настраиваемый код.</span><span class="sxs-lookup"><span data-stu-id="82bc3-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="82bc3-130">Вызов [IMAPISupport::D oConfigPropsheet,](imapisupport-doconfigpropsheet.md) чтобы отобразить лист свойств с скопированные свойствами.</span><span class="sxs-lookup"><span data-stu-id="82bc3-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="82bc3-131">Передай указатель объекту данных свойств в качестве _параметра lpConfigData_ и указатель на таблицу отображения в качестве _параметра lpDisplayTable._</span><span class="sxs-lookup"><span data-stu-id="82bc3-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="82bc3-132">Если вы хотите переопредить режим доступа по умолчанию для этого листа свойств, не задайте флаг DT_EDITABLE для каждого управления в таблице отображения, которая представляет свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="82bc3-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="82bc3-133">После внесения всех изменений в лист свойств вызываем метод **IMAPIProp::CopyTo** объекта свойств, чтобы скопировать измененные свойства обратно в профильный раздел.</span><span class="sxs-lookup"><span data-stu-id="82bc3-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="82bc3-134">Обзор таблиц отображения см. в таблице [Display Tables.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="82bc3-135">Подробные сведения о таблицах отображения см. в [таблице Display Table Implementation.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="82bc3-136">Сведения о внедрении управления см. в см. в нем [Control Object Implementation.](control-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="82bc3-137">Чтобы получить индекс управления, выбранный пользователем в поле списка таблицы отображения, подождите, пока пользователь не нажмет **кнопку ОК** или **Применить**.</span><span class="sxs-lookup"><span data-stu-id="82bc3-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="82bc3-138">На этом этапе идентификатор входа выбранного элемента возвращается в [интерфейс IMAPIProp : IUnknown](imapipropiunknown.md) как значение свойства, указанного участником **ulPRSetProperty** в структуре [DTBLLBX.](dtbllbx.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="82bc3-139">Если необходимо добавить или удалить элементы из списка, не будет работать таблица отображения и метод [IMAPISupport::D ConfigPropsheet.](imapisupport-doconfigpropsheet.md)</span><span class="sxs-lookup"><span data-stu-id="82bc3-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="82bc3-140">Вместо этого рассмотрите возможность реализации листа свойств с API свойств Win32, который содержится в comdlg32.dll файле.</span><span class="sxs-lookup"><span data-stu-id="82bc3-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="82bc3-141">См. также</span><span class="sxs-lookup"><span data-stu-id="82bc3-141">See also</span></span>



[<span data-ttu-id="82bc3-142">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="82bc3-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

