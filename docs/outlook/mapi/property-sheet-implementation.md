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
# <a name="property-sheet-implementation"></a><span data-ttu-id="27b83-103">Реализация листа свойств</span><span class="sxs-lookup"><span data-stu-id="27b83-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="27b83-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="27b83-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="27b83-105">Лист свойств — это диалоговое окно для отображения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="27b83-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="27b83-106">Свойства могут быть только для чтения, позволяя пользователю только просматривать их или читать и записывать, позволяя пользователю вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="27b83-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="27b83-107">Лист свойств содержит одно или несколько перекрывающихся окон, называемых страницами.</span><span class="sxs-lookup"><span data-stu-id="27b83-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="27b83-108">Каждая страница содержит окна управления для настройки группы связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="27b83-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="27b83-109">Пользователи переходят со страницы на страницу, выбирая вкладку, которая выводит соответствующую страницу на переднем плане листа свойств.</span><span class="sxs-lookup"><span data-stu-id="27b83-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="27b83-110">Поставщики услуг должны реализовать таблицу свойств, которая отображает минимальный набор свойств, связанных с конфигурацией в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="27b83-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="27b83-111">Если эти свойства службы сообщений можно изменить, можно разрешить пользователям клиентских приложений, например панели управления, вносить изменения или программными средствами.</span><span class="sxs-lookup"><span data-stu-id="27b83-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="27b83-112">Реализация листов свойств для отображения и редактирования других типов свойств является необязательным.</span><span class="sxs-lookup"><span data-stu-id="27b83-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="27b83-113">Обычно лист свойств требуется отображать в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="27b83-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="27b83-114">Когда клиент вызывает метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) объекта состояния.</span><span class="sxs-lookup"><span data-stu-id="27b83-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="27b83-115">Когда MAPI вызывает метод для работы с объектом поставщика.</span><span class="sxs-lookup"><span data-stu-id="27b83-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="27b83-116">Когда MAPI вызывает функцию точки входа для службы сообщений поставщика.</span><span class="sxs-lookup"><span data-stu-id="27b83-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="27b83-117">Поставщики транспорта также реализуют листы свойств для отображения свойств, связанных с параметрами сообщений, а поставщики адресных книг реализуют листы свойств для просмотра и изменения подробных сведений о пользователях сообщений и списках рассылки, расширенных критериях поиска и шаблонах для ввода новых пользователей.</span><span class="sxs-lookup"><span data-stu-id="27b83-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="27b83-118">Для создания листа свойств можно использовать один из следующих трех методов:</span><span class="sxs-lookup"><span data-stu-id="27b83-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="27b83-119">Вручную, как в любом диалоговом окне.</span><span class="sxs-lookup"><span data-stu-id="27b83-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="27b83-120">С помощью общего управления листа свойств, предоставленного в Windows SDK.</span><span class="sxs-lookup"><span data-stu-id="27b83-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="27b83-121">С помощью отображаемой таблицы MAPI.</span><span class="sxs-lookup"><span data-stu-id="27b83-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="27b83-122">Поставщики должны выбрать последний вариант (создать лист свойств с помощью таблицы отображения).</span><span class="sxs-lookup"><span data-stu-id="27b83-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="27b83-123">Это самый простой вариант, так как он устраняет необходимость работы с пользовательским интерфейсом Windows.</span><span class="sxs-lookup"><span data-stu-id="27b83-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="27b83-124">Чтобы реализовать лист свойств, построенный из таблицы отображения для свойств службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="27b83-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="27b83-125">Вызовите [IMAPISupport::OpenProfileSection,](imapisupport-openprofilesection.md) чтобы открыть раздел в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="27b83-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="27b83-126">[Передайте mapIUID](mapiuid.md) или NULL, чтобы открыть раздел профиля поставщика.</span><span class="sxs-lookup"><span data-stu-id="27b83-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="27b83-127">Вызовите [CreateIProp,](createiprop.md) чтобы создать объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="27b83-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="27b83-128">Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля, чтобы скопировать все свойства раздела в объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="27b83-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="27b83-129">Создайте таблицу отображения, создав одну или несколько структур [DTPAGE,](dtpage.md) описывающих элементы управления для отображения на листе свойств и вызывая функцию [BuildDisplayTable](builddisplaytable.md) или реализуя пользовательский код.</span><span class="sxs-lookup"><span data-stu-id="27b83-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="27b83-130">Вызовите [IMAPISupport::D oConfigPropsheet,](imapisupport-doconfigpropsheet.md) чтобы отобразить лист свойств с скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="27b83-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="27b83-131">Передав указатель на объект данных свойства в качестве параметра _lpConfigData_ и указатель на таблицу отображения в качестве параметра _lpDisplayTable._</span><span class="sxs-lookup"><span data-stu-id="27b83-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="27b83-132">Если вы хотите переопредить режим доступа по умолчанию для этого листа свойств, не устанавливайте флаг DT_EDITABLE для каждого из них в таблице отображения, который представляет свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="27b83-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="27b83-133">После внесения всех изменений на лист свойств вызовите метод **IMAPIProp::CopyTo** объекта данных свойства, чтобы скопировать измененные свойства обратно в раздел профиля.</span><span class="sxs-lookup"><span data-stu-id="27b83-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="27b83-134">Обзор таблиц отображения см. в [таблице отображения.](display-tables.md)</span><span class="sxs-lookup"><span data-stu-id="27b83-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="27b83-135">Подробные сведения о таблицах отображения см. в [описании реализации таблицы отображения.](display-table-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="27b83-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="27b83-136">Сведения о реализации управления см. в реализации [объекта control.](control-object-implementation.md)</span><span class="sxs-lookup"><span data-stu-id="27b83-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="27b83-137">Чтобы получить индекс выбранного пользователем в списке таблицы отображения, подождите, пока пользователь не нажмет кнопку **"ОК"** или **"Применить".**</span><span class="sxs-lookup"><span data-stu-id="27b83-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="27b83-138">На этом этапе идентификатор записи выбранного элемента записи обратно в интерфейс [IMAPIProp : IUnknown](imapipropiunknown.md) в качестве значения свойства, указанного элементом **ulPRSetProperty** в [структуре DTBLLBX.](dtbllbx.md)</span><span class="sxs-lookup"><span data-stu-id="27b83-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="27b83-139">Если требуется возможность добавления или удаления элементов из списка, использование таблицы отображения и [метода IMAPISupport::D oConfigPropsheet](imapisupport-doconfigpropsheet.md) не будет работать.</span><span class="sxs-lookup"><span data-stu-id="27b83-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="27b83-140">Вместо этого рассмотрите возможность реализации листа свойств с API-файлом таблицы свойств Win32, содержа comdlg32.dll файла.</span><span class="sxs-lookup"><span data-stu-id="27b83-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="27b83-141">См. также</span><span class="sxs-lookup"><span data-stu-id="27b83-141">See also</span></span>



[<span data-ttu-id="27b83-142">Поставщики услуг MAPI</span><span class="sxs-lookup"><span data-stu-id="27b83-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

