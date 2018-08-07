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
ms.openlocfilehash: 406451adac3cd73286feb787bd6b4d2f356aa283
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812079"
---
# <a name="property-sheet-implementation"></a><span data-ttu-id="374c1-103">Реализация страницы свойств</span><span class="sxs-lookup"><span data-stu-id="374c1-103">Property Sheet Implementation</span></span>

  
  
<span data-ttu-id="374c1-104">**Относится к**: Outlook</span><span class="sxs-lookup"><span data-stu-id="374c1-104">**Applies to**: Outlook</span></span> 
  
<span data-ttu-id="374c1-105">Окно свойств — это диалоговое окно для отображения свойств объекта.</span><span class="sxs-lookup"><span data-stu-id="374c1-105">A property sheet is a dialog box for displaying the properties of an object.</span></span> <span data-ttu-id="374c1-106">Свойства может быть доступна только для чтения Включение пользователю только просматривать их, или чтения и записи, позволяя пользователям для внесения изменений.</span><span class="sxs-lookup"><span data-stu-id="374c1-106">The properties can be read-only, enabling the user only to view them, or read/write, enabling the user to make changes.</span></span> <span data-ttu-id="374c1-107">Окно свойств содержит один или несколько перекрывающиеся дочернего окна вызывается страниц.</span><span class="sxs-lookup"><span data-stu-id="374c1-107">A property sheet contains one or more overlapping child windows called pages.</span></span> <span data-ttu-id="374c1-108">Каждая страница содержит элемент управления windows для настройки группы свойств, связанных с ними.</span><span class="sxs-lookup"><span data-stu-id="374c1-108">Each page contains control windows for setting a group of related properties.</span></span> <span data-ttu-id="374c1-109">Пользователи переходить между страницами, выбрав вкладку, которая переводит соответствующую страницу на передний план страницы свойств.</span><span class="sxs-lookup"><span data-stu-id="374c1-109">Users navigate from page to page by selecting a tab that brings the corresponding page to the foreground of the property sheet.</span></span>
  
<span data-ttu-id="374c1-110">Поставщики услуг должен реализовывать свойств, которая отображает минимальный набор свойств, связанные с настройкой службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="374c1-110">Service providers must implement a property sheet that displays a minimal set of properties related to configuration in the message service.</span></span> <span data-ttu-id="374c1-111">Если разрешить эти свойства службы сообщений нужно изменить, можно либо разрешить пользователям клиентских приложений, таких как панель управления, внесите необходимые изменения или программным путем реализации изменения.</span><span class="sxs-lookup"><span data-stu-id="374c1-111">If you allow these message service properties to be changed, you can either allow users of client applications, such as the Control Panel, to make the changes or implement the changes programmatically.</span></span> <span data-ttu-id="374c1-112">Реализация свойств для отображения и редактирования других типов свойств не является обязательным.</span><span class="sxs-lookup"><span data-stu-id="374c1-112">Implementing property sheets to display and edit other types of properties is optional.</span></span> 
  
<span data-ttu-id="374c1-113">Как правило необходимо открыть окно свойств в следующих ситуациях:</span><span class="sxs-lookup"><span data-stu-id="374c1-113">Typically, you will need to display a property sheet in the following situations:</span></span>
  
- <span data-ttu-id="374c1-114">Когда клиент вызывает метод [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) состояние объекта.</span><span class="sxs-lookup"><span data-stu-id="374c1-114">When a client calls your status object's [IMAPIStatus::SettingsDialog](imapistatus-settingsdialog.md) method.</span></span> 
    
- <span data-ttu-id="374c1-115">Если MAPI вызывает метод объект поставщика входа в систему.</span><span class="sxs-lookup"><span data-stu-id="374c1-115">When MAPI calls your provider object's logon method.</span></span>
    
- <span data-ttu-id="374c1-116">Если MAPI вызывает функцию точки входа для вашего поставщика службы сообщений.</span><span class="sxs-lookup"><span data-stu-id="374c1-116">When MAPI calls the entry point function for your provider's message service.</span></span>
    
<span data-ttu-id="374c1-117">Поставщики транспорта также реализовать свойств для отображения свойств, связанных с параметрами сообщения и свойств, просматривать и редактировать подробные сведения об обмене сообщениями пользователей и списки рассылки, расширенный поиск, реализуемые поставщиками адресных книг критерии, шаблоны и для ввода новых пользователей.</span><span class="sxs-lookup"><span data-stu-id="374c1-117">Transport providers also implement property sheets to display properties related to message options, and address book providers implement property sheets to view and edit detailed information about messaging users and distribution lists, advanced search criteria, and templates for entering new users.</span></span>
  
<span data-ttu-id="374c1-118">Для создания свойств, можно использовать один из следующих трех способов:</span><span class="sxs-lookup"><span data-stu-id="374c1-118">You can use one of the following three techniques to create a property sheet:</span></span>
  
- <span data-ttu-id="374c1-119">Вручную, как и любой диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="374c1-119">Manually, as you would any dialog box.</span></span>
    
- <span data-ttu-id="374c1-120">С помощью свойства листа распространенных элемента управления в пакет SDK для Windows.</span><span class="sxs-lookup"><span data-stu-id="374c1-120">By using the property sheet common control provided in the Windows SDK.</span></span>
    
- <span data-ttu-id="374c1-121">С помощью MAPI отображения таблицы.</span><span class="sxs-lookup"><span data-stu-id="374c1-121">By using a MAPI display table.</span></span>
    
<span data-ttu-id="374c1-122">Поставщики должен выбрать параметр последнего (создать страницу свойств с помощью таблицы отображения).</span><span class="sxs-lookup"><span data-stu-id="374c1-122">Providers should choose the last option (create a property sheet by using a display table).</span></span> <span data-ttu-id="374c1-123">Это самый простой вариант, поскольку устраняет необходимость работать с пользовательским интерфейсом Windows.</span><span class="sxs-lookup"><span data-stu-id="374c1-123">This is the simplest option because it eliminates the need to work with the Windows user interface.</span></span> 
  
<span data-ttu-id="374c1-124">Для реализации свойств, построенная на основе таблицы отображения для свойств службы сообщений, используйте следующую процедуру:</span><span class="sxs-lookup"><span data-stu-id="374c1-124">To implement a property sheet built from a display table for your message service properties, use the following procedure:</span></span>
  
1. <span data-ttu-id="374c1-125">Вызовите [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) , чтобы открыть отдельный раздел текущего профиля.</span><span class="sxs-lookup"><span data-stu-id="374c1-125">Call [IMAPISupport::OpenProfileSection](imapisupport-openprofilesection.md) to open a section in the current profile.</span></span> <span data-ttu-id="374c1-126">Передайте [MAPIUID](mapiuid.md) или значение NULL, чтобы открыть раздел ваш поставщик профилей.</span><span class="sxs-lookup"><span data-stu-id="374c1-126">Pass your [MAPIUID](mapiuid.md) or NULL to open your provider's profile section.</span></span> 
    
2. <span data-ttu-id="374c1-127">Вызов [CreateIProp](createiprop.md) для создания объекта данных свойства.</span><span class="sxs-lookup"><span data-stu-id="374c1-127">Call [CreateIProp](createiprop.md) to create a property data object.</span></span> 
    
3. <span data-ttu-id="374c1-128">Вызовите метод [IMAPIProp::CopyTo](imapiprop-copyto.md) раздела профиля, чтобы скопировать все свойства раздела объект данных свойства.</span><span class="sxs-lookup"><span data-stu-id="374c1-128">Call the profile section's [IMAPIProp::CopyTo](imapiprop-copyto.md) method to copy all of the section's properties to the property data object.</span></span> 
    
4. <span data-ttu-id="374c1-129">Создание таблицы отображения путем создания структуры один или несколько [DTPAGE](dtpage.md) , которые описывают элементы управления для отображения на странице свойств и вызов функции [BuildDisplayTable](builddisplaytable.md) или при помощи пользовательского кода.</span><span class="sxs-lookup"><span data-stu-id="374c1-129">Create a display table either by building one or more [DTPAGE](dtpage.md) structures that describe the controls to appear on the property sheet and calling the [BuildDisplayTable](builddisplaytable.md) function, or by implementing custom code.</span></span> 
    
5. <span data-ttu-id="374c1-130">Вызов [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) для отображения свойств, имеющей скопированные свойства.</span><span class="sxs-lookup"><span data-stu-id="374c1-130">Call [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) to display a property sheet that has the copied properties.</span></span> <span data-ttu-id="374c1-131">Передайте указатель на объект данных свойство как параметр _lpConfigData_ и указатель в таблице отображения и параметр _lpDisplayTable_ .</span><span class="sxs-lookup"><span data-stu-id="374c1-131">Pass a pointer to the property data object as the  _lpConfigData_ parameter and a pointer to the display table as the  _lpDisplayTable_ parameter.</span></span> <span data-ttu-id="374c1-132">Если вы хотите переопределить режим доступа по умолчанию для этой страницы свойств, не задан флаг DT_EDITABLE для каждого элемента управления в таблице отображения, который представляет свойство только для чтения.</span><span class="sxs-lookup"><span data-stu-id="374c1-132">If you want to override the default access mode for this property sheet, do not set the DT_EDITABLE flag for each control in the display table that represents a read-only property.</span></span> 
    
6. <span data-ttu-id="374c1-133">Когда все изменения, внесенные в окне свойств, вызовите метод **IMAPIProp::CopyTo** объект данных свойств для копирования изменения свойств в разделе профилей.</span><span class="sxs-lookup"><span data-stu-id="374c1-133">When all of the changes have been made in the property sheet, call the property data object's **IMAPIProp::CopyTo** method to copy the changed properties back to the profile section.</span></span> 
    
<span data-ttu-id="374c1-134">Общие сведения о таблицах отображения разделе [Отображение таблиц](display-tables.md).</span><span class="sxs-lookup"><span data-stu-id="374c1-134">For an overview of display tables, see [Display Tables](display-tables.md).</span></span> 
  
<span data-ttu-id="374c1-135">Подробные сведения о таблицах отображения [Отображения реализации таблицы](display-table-implementation.md)см.</span><span class="sxs-lookup"><span data-stu-id="374c1-135">For detailed information about display tables, see [Display Table Implementation](display-table-implementation.md).</span></span> 
  
<span data-ttu-id="374c1-136">Сведения о реализации элемента управления содержатся в разделе [Реализация объекта элемента управления](control-object-implementation.md).</span><span class="sxs-lookup"><span data-stu-id="374c1-136">For information about implementing a control, see [Control Object Implementation](control-object-implementation.md).</span></span>
  
<span data-ttu-id="374c1-137">Чтобы получить индекс элемента управления, выбранной пользователем в поле со списком отображения таблицы, подождите, пока пользователь нажимает **кнопку ОК** или **Применить**.</span><span class="sxs-lookup"><span data-stu-id="374c1-137">To retrieve the index of a control that a user selects in a display table list box, wait until the user clicks **OK** or **Apply**.</span></span> <span data-ttu-id="374c1-138">На этом этапе идентификатор записи выбранного элемента, записывается обратно [IMAPIProp: IUnknown](imapipropiunknown.md) интерфейс в качестве значения свойства, указанного в член **ulPRSetProperty** в структуре [DTBLLBX](dtbllbx.md) .</span><span class="sxs-lookup"><span data-stu-id="374c1-138">At this point, the entry identifier of the selected item is written back to the [IMAPIProp : IUnknown](imapipropiunknown.md) interface as the value of the property specified by the **ulPRSetProperty** member in the [DTBLLBX](dtbllbx.md) structure.</span></span> 
  
<span data-ttu-id="374c1-139">Если требуется иметь возможность добавлять или удалять элементы из списка с помощью метода [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) и отображения таблицы не будут работать.</span><span class="sxs-lookup"><span data-stu-id="374c1-139">If you need to be able to add or remove items from your list box, using a display table and the [IMAPISupport::DoConfigPropsheet](imapisupport-doconfigpropsheet.md) method will not work.</span></span> <span data-ttu-id="374c1-140">Вместо этого рассмотрите возможность реализации свойств с помощью API листа свойство Win32, содержащийся в файле comdlg32.dll.</span><span class="sxs-lookup"><span data-stu-id="374c1-140">Instead, consider implementing a property sheet with the Win32 property sheet API contained in the comdlg32.dll file.</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="374c1-141">См. также</span><span class="sxs-lookup"><span data-stu-id="374c1-141">See also</span></span>



[<span data-ttu-id="374c1-142">Поставщиков служб MAPI</span><span class="sxs-lookup"><span data-stu-id="374c1-142">MAPI Service Providers</span></span>](mapi-service-providers.md)

