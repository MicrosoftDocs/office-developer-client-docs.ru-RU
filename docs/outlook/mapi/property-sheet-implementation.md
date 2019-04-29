---
title: Реализация страницы свойств
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
# <a name="property-sheet-implementation"></a><span data-ttu-id="06dc2-103">Реализация страницы свойств</span><span class="sxs-lookup"><span data-stu-id="06dc2-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="06dc2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="06dc2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="06dc2-105">Страница свойств — это диалоговое окно для отображения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="06dc2-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="06dc2-106">Свойства могут быть доступны только для чтения, что позволяет пользователю только просматривать их или читать и записывать, позволяя пользователю вносить изменения.</span><span class="sxs-lookup"><span data-stu-id="06dc2-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="06dc2-107">Страница свойств содержит один или несколько перекрывающихся дочерних окон, называемых страницами.</span><span class="sxs-lookup"><span data-stu-id="06dc2-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="06dc2-108">Каждая страница содержит окна элементов управления для настройки группы связанных свойств.</span><span class="sxs-lookup"><span data-stu-id="06dc2-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="06dc2-109">Пользователи переносятся со страницы на страницу, выбирая вкладку, которая переводит соответствующую страницу на передний план страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="06dc2-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="06dc2-110">Поставщики услуг должны реализовать страницу свойств, в которой отображается минимальный набор свойств, связанных с конфигурацией в службе сообщений.</span><span class="sxs-lookup"><span data-stu-id="06dc2-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="06dc2-111">Если вы разрешаете изменение этих свойств службы сообщений, вы можете либо разрешить пользователям клиентских приложений, таких как панель управления, изменить или применить изменения программным способом.</span><span class="sxs-lookup"><span data-stu-id="06dc2-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="06dc2-112">Реализация страниц свойств для отображения и изменения других типов свойств является необязательной.</span><span class="sxs-lookup"><span data-stu-id="06dc2-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="06dc2-113">Как правило, необходимо отображать страницу свойств в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="06dc2-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="06dc2-114">Когда клиент вызывает метод [имапистатус:: сеттингсдиалог](imapistatus-settingsdialog.md) объекта Status.</span><span class="sxs-lookup"><span data-stu-id="06dc2-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="06dc2-115">Когда MAPI вызывает метод входа объекта поставщика.</span><span class="sxs-lookup"><span data-stu-id="06dc2-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="06dc2-116">Когда MAPI вызывает функцию точки входа для службы сообщений поставщика.</span><span class="sxs-lookup"><span data-stu-id="06dc2-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="06dc2-117">Поставщики транспорта также реализуют страницы свойств для отображения свойств, связанных с параметрами сообщений, а поставщики адресных книг реализуют страницы свойств для просмотра и редактирования подробных сведений об обмене сообщениями и списках рассылки, расширенном поиске условия и шаблоны для ввода новых пользователей.</span><span class="sxs-lookup"><span data-stu-id="06dc2-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="06dc2-118">Для создания страницы свойств можно использовать один из следующих трех способов:</span><span class="sxs-lookup"><span data-stu-id="06dc2-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="06dc2-119">Вручную, как любое из диалоговых окон.</span><span class="sxs-lookup"><span data-stu-id="06dc2-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="06dc2-120">С помощью общего элемента управления листа свойств, включенного в пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="06dc2-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="06dc2-121">С помощью таблицы отображения MAPI.</span><span class="sxs-lookup"><span data-stu-id="06dc2-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="06dc2-122">Поставщики должны выбрать последний вариант (создать страницу свойств с помощью таблицы отображения).</span><span class="sxs-lookup"><span data-stu-id="06dc2-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="06dc2-123">Это самый простой вариант, так как он избавляет от необходимости работы с пользовательским интерфейсом Windows.</span><span class="sxs-lookup"><span data-stu-id="06dc2-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="06dc2-124">Чтобы реализовать страницу свойств, созданную из таблицы отображения для свойств службы сообщений, используйте следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="06dc2-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="06dc2-125">Call [имаписуппорт:: опенпрофилесектион](imapisupport-openprofilesection.md) , чтобы открыть раздел в текущем профиле.</span><span class="sxs-lookup"><span data-stu-id="06dc2-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="06dc2-126">Передайте [мапиуид](mapiuid.md) или значение null, чтобы открыть раздел профиля поставщика.</span><span class="sxs-lookup"><span data-stu-id="06dc2-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="06dc2-127">Call [креатеипроп](createiprop.md) для создания объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="06dc2-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="06dc2-128">ВыЗовите метод [IMAPIProp:: CopyTo](imapiprop-copyto.md) раздела profile, чтобы скопировать все свойства раздела в объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="06dc2-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="06dc2-129">Создайте таблицу отображения, создав одну или несколько структур [дтпаже](dtpage.md) , описывающих элементы управления, которые будут отображаться на странице свойств и вызвав функцию [буилддисплайтабле](builddisplaytable.md) , или реализовав пользовательский код.</span><span class="sxs-lookup"><span data-stu-id="06dc2-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="06dc2-130">Call [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) для отображения страницы свойств с скопированными свойствами.</span><span class="sxs-lookup"><span data-stu-id="06dc2-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="06dc2-131">Передайте указатель на объект данных Property в качестве параметра _лпконфигдата_ и указателя на таблицу отображения в качестве параметра _лпдисплайтабле_ .</span><span class="sxs-lookup"><span data-stu-id="06dc2-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="06dc2-132">Если вы хотите переопределить режим доступа по умолчанию для этой страницы свойств, не задавайте флаг ДТ_ЕДИТАБЛЕ для каждого элемента управления в таблице отображения, который представляет свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="06dc2-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="06dc2-133">После внесения всех изменений на странице свойств вызовите метод **IMAPIProp:: CopyTo** объекта данных Property, чтобы скопировать измененные свойства обратно в раздел profile.</span><span class="sxs-lookup"><span data-stu-id="06dc2-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="06dc2-134">Общие сведения о отображаемых таблицах приведены в разделе [Display Tables](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="06dc2-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="06dc2-135">Подробную информацию о таблицах отображения можно узнать в статье [Реализация отображения таблицы](display-table-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="06dc2-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="06dc2-136">Сведения о реализации элемента управления можно найти в разделе [Реализация объекта Control](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="06dc2-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="06dc2-137">Чтобы получить индекс элемента управления, выбираемого пользователем в списке отображаемой таблицы, подождите, пока пользователь нажмет кнопку **ОК** или **Применить**.</span><span class="sxs-lookup"><span data-stu-id="06dc2-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="06dc2-138">На этом шаге идентификатор записи выбранного элемента записывается обратно в интерфейс [IMAPIProp: IUnknown](imapipropiunknown.md) в качестве значения свойства, указанного элементом **Улпрсетпроперти** в структуре [дтбллбкс](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="06dc2-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="06dc2-139">Если вам нужно иметь возможность добавлять и удалять элементы из списка, с помощью таблицы отображения и метода [имаписуппорт::D оконфигпропшит](imapisupport-doconfigpropsheet.md) не будут работать.</span><span class="sxs-lookup"><span data-stu-id="06dc2-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="06dc2-140">Вместо этого рекомендуется реализовать страницу свойств с помощью API страницы свойств Win32, содержащегося в файле COMDLG32. dll.</span><span class="sxs-lookup"><span data-stu-id="06dc2-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="06dc2-141">См. также</span><span class="sxs-lookup"><span data-stu-id="06dc2-141">See also</span></span>



[<span data-ttu-id="06dc2-142">Поставщики службы MAPI</span><span class="sxs-lookup"><span data-stu-id="06dc2-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

