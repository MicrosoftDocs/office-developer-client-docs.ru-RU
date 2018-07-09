---
title: Интеграция приложений обмена мгновенными Сообщениями с помощью приложений Office
manager: soliver
ms.date: 07/25/2016
ms.audience: Developer
localization_priority: Normal
ms.assetid: beba316b-1dfe-4e1b-adae-42418906c177
description: В этой статье описывается настройка клиентского приложения мгновенные сообщения (IM), чтобы он интегрируется с использованием социальных функций в Office 2013, включая отображение сведений о присутствии и отправлять мгновенные сообщения из карточки контакта.
ms.openlocfilehash: 383aac24be347cf637d9e2f255623035eea8bc40
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813076"
---
# <a name="integrating-im-applications-with-office"></a><span data-ttu-id="ef468-103">Интеграция приложений обмена мгновенными Сообщениями с помощью приложений Office</span><span class="sxs-lookup"><span data-stu-id="ef468-103">Integrating IM applications with Office</span></span>

<span data-ttu-id="ef468-104">В этой статье описывается настройка клиентского приложения мгновенные сообщения (IM), чтобы он интегрируется с использованием социальных функций в Office 2013, включая отображение сведений о присутствии и отправлять мгновенные сообщения из карточки контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-104">This article describes how to configure an instant message (IM) client application so that it integrates with the social features in Office 2013, including displaying presence and sending instant messages from the contact card.</span></span>
  
<span data-ttu-id="ef468-105">Если у вас есть вопросы или комментарии о данной технической статье или процессами, его описание, можно напрямую, отправив сообщение электронной почты для [docthis@microsoft.com](mailto:docthis@microsoft.com)обратитесь в Майкрософт.</span><span class="sxs-lookup"><span data-stu-id="ef468-105">If you have any questions or comments about this technical article or the processes that it describes, you can contact Microsoft directly by sending an email to [docthis@microsoft.com](mailto:docthis@microsoft.com).</span></span>
  
## <a name="introduction"></a><span data-ttu-id="ef468-106">Введение</span><span class="sxs-lookup"><span data-stu-id="ef468-106">Introduction</span></span>
<span data-ttu-id="ef468-107"><a name="off15_IMIntegration_Intro"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-107"></span></span>

<span data-ttu-id="ef468-108">Office 2013 предоставляет приложениям, включая Lync 2013 расширенными возможностями интеграции с клиентом обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-108">Office 2013 provides rich integration with IM client applications, including Lync 2013.</span></span> <span data-ttu-id="ef468-109">В этом интеграции предоставляет пользователям возможности обмена мгновенными Сообщениями из в Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013 и OneNote 2013, а также обеспечивает интеграцию присутствия на страницах SharePoint 2013.</span><span class="sxs-lookup"><span data-stu-id="ef468-109">This integration provides users with IM capabilities from within Word 2013, Excel 2013, PowerPoint 2013, Outlook 2013, Visio 2013, Project 2013, and OneNote 2013 as well as providing presence integration on SharePoint 2013 pages.</span></span> <span data-ttu-id="ef468-110">Пользователей можно увидеть фотографий, имя, состояние присутствия и контактных данных людей в свой список контактов.</span><span class="sxs-lookup"><span data-stu-id="ef468-110">Users can see the photo, name, presence status, and contact data for people in their contacts list.</span></span> <span data-ttu-id="ef468-111">Их можно начать сеанс, видеозвонок или телефонный звонок обмена мгновенными Сообщениями непосредственно из карточки контакта (элемент пользовательского интерфейса в Office 2013, что параметры информации и связи контактов поверхности).</span><span class="sxs-lookup"><span data-stu-id="ef468-111">They can start an IM session, video call, or phone call directly from the contact card (the UI element in Office 2013 that surfaces contact information and communication options).</span></span> <span data-ttu-id="ef468-112">Office 2013 упрощает Оставайтесь на связи контактам, без учета вы не из электронной почты или документов.</span><span class="sxs-lookup"><span data-stu-id="ef468-112">Office 2013 makes it easy to stay connected to your contacts without taking you outside of your email or documents.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ef468-113">В этой статье термин обмена мгновенными Сообщениями клиентского приложения для указания специально для приложения, установленные на компьютере пользователя, который подключается к службе обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-113">This article uses the term IM client application to refer specifically to the application installed on a user's computer that communicates to the IM service.</span></span> <span data-ttu-id="ef468-114">Например Lync 2013 считается клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-114">For example, Lync 2013 is considered an IM client application.</span></span> <span data-ttu-id="ef468-115">В этой статье отсутствуют подробные сведения о взаимодействии клиентское приложение обмена мгновенными Сообщениями к службе обмена мгновенными Сообщениями или о самой службы обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-115">This article does not provide details about how the IM client application communicates to the IM service or about the IM service itself.</span></span> 
  
<span data-ttu-id="ef468-116">Клиентского приложения обмена мгновенными Сообщениями можно настроить таким образом, чтобы он взаимодействует с Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-116">You can customize an IM client application so that it communicates with Office.</span></span> <span data-ttu-id="ef468-117">В частности можно изменить приложение обмена мгновенными Сообщениями, чтобы она отображала следующие сведения в рамках пользовательского интерфейса Office:</span><span class="sxs-lookup"><span data-stu-id="ef468-117">Specifically, you can modify your IM application so that it displays the following information within the Office UI:</span></span>
  
- <span data-ttu-id="ef468-118">Фотография контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-118">Contact photo.</span></span>
    
- <span data-ttu-id="ef468-119">Имя контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-119">Contact name.</span></span>
    
- <span data-ttu-id="ef468-120">Заметки о состоянии контакта личные.</span><span class="sxs-lookup"><span data-stu-id="ef468-120">Contact personal status note.</span></span>
    
- <span data-ttu-id="ef468-121">Состояние присутствия контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-121">Contact presence status.</span></span>
    
- <span data-ttu-id="ef468-122">Обратитесь в доступности строка (например, «Доступен» или «нет на работе»).</span><span class="sxs-lookup"><span data-stu-id="ef468-122">Contact availability string (for example, "Available" or "Out of Office").</span></span>
    
- <span data-ttu-id="ef468-123">Обратитесь в строку возможность (например, «видео Готово»).</span><span class="sxs-lookup"><span data-stu-id="ef468-123">Contact capability string (for example, "Video Ready").</span></span>
    
- <span data-ttu-id="ef468-124">Запуск обмена мгновенными Сообщениями одним щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="ef468-124">One-click IM launch.</span></span>
    
- <span data-ttu-id="ef468-125">Запуск видео звонка одним щелчком мыши.</span><span class="sxs-lookup"><span data-stu-id="ef468-125">One-click video call launch.</span></span>
    
- <span data-ttu-id="ef468-126">Запуск телефонного звонка одним щелчком мыши (включая SIP, номер телефона, голосовой почты и новый номер звонка).</span><span class="sxs-lookup"><span data-stu-id="ef468-126">One-click phone call launch (including SIP, phone number, voice mail, and call new number).</span></span>
    
- <span data-ttu-id="ef468-127">Управление контактами (Добавить группу обмена мгновенными Сообщениями).</span><span class="sxs-lookup"><span data-stu-id="ef468-127">Contact management (add to IM group).</span></span>
    
- <span data-ttu-id="ef468-128">Обратитесь в расположение и часовой пояс.</span><span class="sxs-lookup"><span data-stu-id="ef468-128">Contact location and time zone.</span></span>
    
- <span data-ttu-id="ef468-129">Контактные данные, номер телефона, адрес электронной почты, должность и название компании.</span><span class="sxs-lookup"><span data-stu-id="ef468-129">Contact data, phone number, email address, title, and company name.</span></span>
    
<span data-ttu-id="ef468-130">**На рисунке 1. Карточка контакта в Office 2013**</span><span class="sxs-lookup"><span data-stu-id="ef468-130">**Figure 1. Contact card in Office 2013**</span></span>

<span data-ttu-id="ef468-131">![Карточка контакта в Office 2013] (media/ocom15_peoplecard.png "Карточка контакта в Office 2013")</span><span class="sxs-lookup"><span data-stu-id="ef468-131">![The People Card in Office 2013](media/ocom15_peoplecard.png "The People Card in Office 2013")</span></span>
  
<span data-ttu-id="ef468-132">Чтобы включить этот интеграции с Office, клиентского приложения обмена мгновенными Сообщениями необходимо реализовать набор интерфейсов, предоставляемых Office, чтобы подключиться к ней.</span><span class="sxs-lookup"><span data-stu-id="ef468-132">To enable this integration with Office, an IM client application must implement a set of interfaces that Office provides to connect to it.</span></span> <span data-ttu-id="ef468-133">Интерфейсы API для интеграции включены в пространстве имен [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) , который содержится в файле Microsoft.Office.UC.dll, который устанавливается вместе с версиями Office 2013, включая Lync / Скайп для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="ef468-133">The APIs for this integration are included in the [UCCollborationLib](http://msdn.microsoft.com/en-au/library/uccollaborationlib.aspx) namespace that is contained in the Microsoft.Office.UC.dll file, which is installed with versions of Office 2013 that include Lync / Skype for Business.</span></span> <span data-ttu-id="ef468-134">Пространство имен **UCCollaborationLib** включает в себя интерфейсы, которые должны быть реализованы для интеграции с Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-134">The **UCCollaborationLib** namespace includes the interfaces that you must implement to integrate with Office.</span></span> 
  
> [!IMPORTANT] 
> <span data-ttu-id="ef468-135">Библиотека типов для необходимых интерфейсов встраивается в Lync 2013/Скайп для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="ef468-135">The type library for the required interfaces is embedded in Lync 2013/Skype for Business.</span></span> <span data-ttu-id="ef468-136">Для интеграторов сторонних производителей это работает только в том случае, если на целевом компьютере установлены Lync 2013 и Скайп для бизнеса.</span><span class="sxs-lookup"><span data-stu-id="ef468-136">For third-party integrators, this works only when both Lync 2013 and Skype for Business are installed on the target machine.</span></span> <span data-ttu-id="ef468-137">Если вы реализуете интеграцию с помощью Office Standard, необходимо извлечь библиотеку типов и установить его на целевом компьютере.</span><span class="sxs-lookup"><span data-stu-id="ef468-137">If you are integrating using Office Standard, you need to extract the type library and install it on the target machine.</span></span> <span data-ttu-id="ef468-138">[Пакет SDK для Lync 2013](https://www.microsoft.com/en-us/download/details.aspx?id=36824) включает в себя файл Microsoft.Office.UC.dll.</span><span class="sxs-lookup"><span data-stu-id="ef468-138">The [Lync 2013 SDK](https://www.microsoft.com/en-us/download/details.aspx?id=36824) includes the Microsoft.Office.UC.dll file.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="ef468-139">Аналогичным образом интеграции небольшое количество приложений Office 2010 в приложение поставщика обмена мгновенными Сообщениями сторонних производителей: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010 и SharePoint Server 2010 (с помощью элемента управления ActiveX).</span><span class="sxs-lookup"><span data-stu-id="ef468-139">A handful of Office 2010 applications can integrate similarly with a third-party IM provider application: Outlook 2010, Word 2010, Excel 2010, PowerPoint 2010, and SharePoint Server 2010 (using an ActiveX control).</span></span> <span data-ttu-id="ef468-140">Многие из действий, необходимых для интеграции с Office 2013 относятся к Office 2010 также.</span><span class="sxs-lookup"><span data-stu-id="ef468-140">Many of the steps required for integration with Office 2013 apply to Office 2010 as well.</span></span> <span data-ttu-id="ef468-141">Существует ряд ключевых различий в интеграции Office 2010 с помощью поставщика приложения обмена мгновенными Сообщениями:</span><span class="sxs-lookup"><span data-stu-id="ef468-141">There are several key differences in how Office 2010 integrates with an IM provider application:</span></span> 
>  - <span data-ttu-id="ef468-142">Office 2010 не отображать фотографии контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-142">Office 2010 does not display the contact's photo.</span></span> 
>  - <span data-ttu-id="ef468-143">Файл Microsoft.Office.Uc.dll необходимо загрузить отдельно с Office 2010.</span><span class="sxs-lookup"><span data-stu-id="ef468-143">You must download the Microsoft.Office.Uc.dll file separately from Office 2010.</span></span> <span data-ttu-id="ef468-144">[Пакет SDK для Lync 2010](http://www.microsoft.com/en-us/download/details.aspx?id=18898) включает в себя файл Microsoft.Office.UC.dll для Office 2010.</span><span class="sxs-lookup"><span data-stu-id="ef468-144">The [Lync 2010 SDK](http://www.microsoft.com/en-us/download/details.aspx?id=18898) includes the Microsoft.Office.UC.dll file for Office 2010.</span></span> 
>  - <span data-ttu-id="ef468-145">Когда приложение Office вызывает метод [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) в клиентском приложении обмена мгновенными Сообщениями, передается в строку «14.0.0.0».</span><span class="sxs-lookup"><span data-stu-id="ef468-145">When the Office application calls the [IUCOfficeIntegration.GetAuthenticationInfo](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) method on the IM client application, it passes in the string "14.0.0.0".</span></span> 
>  - <span data-ttu-id="ef468-146">Office 2010 перечисляет все группы или контактов сразу же подключается к клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-146">Office 2010 enumerates all groups and contacts as soon as it connects to an IM client application.</span></span> 
  
## <a name="how-office-integrates-with-an-im-client-application"></a><span data-ttu-id="ef468-147">Как Office интегрируется с клиентского приложения обмена мгновенными Сообщениями</span><span class="sxs-lookup"><span data-stu-id="ef468-147">How Office integrates with an IM client application</span></span>
<span data-ttu-id="ef468-148"><a name="off15_IMIntegration_How"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-148"></span></span>

<span data-ttu-id="ef468-149">При запуске приложения Office 2013 проходит через процесс интеграции с клиентского приложения обмена мгновенными Сообщениями по умолчанию:</span><span class="sxs-lookup"><span data-stu-id="ef468-149">When an Office 2013 application starts, it goes through the following process to integrate with the default IM client application:</span></span>
  
1. <span data-ttu-id="ef468-150">Он проверяет реестр, чтобы обнаружить клиентского приложения обмена мгновенными Сообщениями по умолчанию и затем подключается к нему.</span><span class="sxs-lookup"><span data-stu-id="ef468-150">It checks the registry to discover the default IM client application and then connects to it.</span></span>
    
2. <span data-ttu-id="ef468-151">Оно выполняет проверку подлинности с помощью клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-151">It authenticates with the IM client application.</span></span>
    
3. <span data-ttu-id="ef468-152">Осуществляет подключение к определенным интерфейсы, предоставляемые интерфейсом клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-152">It connects to specific interfaces that are exposed by the IM client application.</span></span>
    
4. <span data-ttu-id="ef468-153">Он определяет возможности вошедшего в систему пользователя (локальный), включая начало контактов пользователя, определения присутствия пользователя, а также для определения возможности обмена мгновенными Сообщениями пользователя (обмен мгновенными сообщениями, видео-чат, VOIP и т. п.).</span><span class="sxs-lookup"><span data-stu-id="ef468-153">It determines the capabilities of the currently signed-in user (local user), including getting the user's contacts, determining the user's presence, and determining the user's IM capabilities (instant messaging, video chat, VOIP, and so on).</span></span>
    
5. <span data-ttu-id="ef468-154">Он получает сведения о присутствии для контактов с локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-154">It gets presence information for the local user's contacts.</span></span>
    
6. <span data-ttu-id="ef468-155">При завершении работы приложения клиент обмена мгновенными Сообщениями, приложение Office 2013 отключает без уведомления.</span><span class="sxs-lookup"><span data-stu-id="ef468-155">When the IM client application shuts down, the Office 2013 application silently disconnects.</span></span>
    
### <a name="discovering-the-im-application"></a><span data-ttu-id="ef468-156">Обнаружение приложений обмена мгновенными Сообщениями</span><span class="sxs-lookup"><span data-stu-id="ef468-156">Discovering the IM application</span></span>

<span data-ttu-id="ef468-157">Приложение Office выполняет поиск для нескольких конкретных ключей и записей в реестр, чтобы обнаружить клиентского приложения обмена мгновенными Сообщениями по умолчанию.</span><span class="sxs-lookup"><span data-stu-id="ef468-157">The Office application looks for several specific keys and entries in the registry to discover the default IM client application.</span></span> <span data-ttu-id="ef468-158">При обнаружении клиентского приложения обмена мгновенными Сообщениями по умолчанию она пытается подключиться к ней.</span><span class="sxs-lookup"><span data-stu-id="ef468-158">If it discovers a default IM client application, it then attempts to connect to it.</span></span>
  
<span data-ttu-id="ef468-159">Процесс, который проходит приложение Office для обнаружения клиентского приложения обмена мгновенными Сообщениями по умолчанию выглядит следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef468-159">The process that the Office application goes through to discover the default IM client application is as follows:</span></span>
  
1. <span data-ttu-id="ef468-160">Приложение Office проверяет, если HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp раздел реестра имеет значение и считывает списке имя приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-160">The Office application looks to see if the HKEY_CURRENT_USER\Software\IM Providers\DefaultIMApp subkey in the registry is set and reads the application name listed there.</span></span>
    
2. <span data-ttu-id="ef468-161">Приложение Office выберите считывает ключа \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_и отслеживает значение для изменения.</span><span class="sxs-lookup"><span data-stu-id="ef468-161">The Office application then reads the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key and monitors the value for changes.</span></span>
    
3. <span data-ttu-id="ef468-162">Затем приложение Office считывает раздел реестра HKEY_LOCAL_MACHINE\Software\IM Providers\ _имя приложения_ и получает значения ID (CLSID) ProcessName и классов, хранящимся в нем.</span><span class="sxs-lookup"><span data-stu-id="ef468-162">The Office application next reads the HKEY_LOCAL_MACHINE\Software\IM Providers\ _Application name_ registry key and gets the ProcessName and class ID (CLSID) values stored there.</span></span> 
    
4. <span data-ttu-id="ef468-163">После клиентского приложения обмена мгновенными Сообщениями имеет успешно завершена последовательность start и зарегистрирован все классы для интеграции сведений о присутствии, он задает ключ \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_, «2» Указывает, клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-163">Once the IM client application has completed its start sequence successfully and registered all of the classes correctly for the presence integration, it sets the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key to "2", indicating that the client application is running.</span></span>
    
5. <span data-ttu-id="ef468-164">Когда приложение Office обнаруживает, что ключ \UpAndRunning HKEY_CURRENT_USER\Software\IM Providers\ _имя приложения_имеет значение «2», проверяет список выполняющихся процессов на компьютере для имя процесса клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-164">When the Office application discovers that the HKEY_CURRENT_USER\Software\IM Providers\ _Application name_\UpAndRunning key has been set to "2", it checks the list of running processes on the computer for the process name of the IM client application.</span></span>
    
6. <span data-ttu-id="ef468-165">Когда приложение Office обнаруживает процесс, который использует клиентское приложение обмена мгновенными Сообщениями, приложение Office вызывает **CoCreateInstance** с помощью CLSID для соединения с клиентского приложения обмена мгновенными Сообщениями как сервер COM ожидания процесса.</span><span class="sxs-lookup"><span data-stu-id="ef468-165">Once the Office application finds the process that the IM client application uses, the Office application calls **CoCreateInstance** using the CLSID to establish a connection to the IM client application as an out-of-process COM server.</span></span> 
    
### <a name="authenticating-the-connection-to-the-im-application"></a><span data-ttu-id="ef468-166">Проверка подлинности подключения к приложению обмена мгновенными Сообщениями</span><span class="sxs-lookup"><span data-stu-id="ef468-166">Authenticating the connection to the IM application</span></span>

<span data-ttu-id="ef468-167">После приложение Office устанавливает подключение к клиентское приложение обмена мгновенными Сообщениями, затем происходит следующее:</span><span class="sxs-lookup"><span data-stu-id="ef468-167">After the Office application establishes a connection to the IM client application, it then does the following:</span></span>
  
1. <span data-ttu-id="ef468-168">Приложение Office вызывает метод [IUnknown::QueryInterface](http://msdn.microsoft.com/ru-ru/library/ms682521%28v=VS.85%29.aspx) для проверки для интерфейса [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) .</span><span class="sxs-lookup"><span data-stu-id="ef468-168">The Office application calls [IUnknown::QueryInterface](http://msdn.microsoft.com/ru-ru/library/ms682521%28v=VS.85%29.aspx) method to check for the [IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) interface.</span></span> 
    
2. <span data-ttu-id="ef468-169">Затем приложение Office вызывает метод **IUCOfficeIntegration.GetAuthenticationInfo** , передав в наибольший интеграции поддерживаемые версии (например, «15.0.0.0»).</span><span class="sxs-lookup"><span data-stu-id="ef468-169">The Office application then calls the **IUCOfficeIntegration.GetAuthenticationInfo** method, passing in the highest supported integration version (for example, "15.0.0.0").</span></span> 
    
3. <span data-ttu-id="ef468-170">Если клиентское приложение обмена мгновенными Сообщениями поддерживает версии Office, переданное в качестве параметра, приложение возвращает следующую строку XML-кодом коду вызова:</span><span class="sxs-lookup"><span data-stu-id="ef468-170">If the IM client application supports the version of Office passed in as a parameter, the application returns the following hard-coded XML string to the calling code:</span></span>
    
    `<authenticationinfo>`
    
   > [!NOTE]
   > <span data-ttu-id="ef468-171">В целях прежних версий клиентского приложения обмена мгновенными Сообщениями должен возвращать значение `<authenticationinfo>` для вызова **GetAuthenticationInfo** если оно поддерживает версию Office переданную как параметр.</span><span class="sxs-lookup"><span data-stu-id="ef468-171">For legacy reasons, the IM client application must return the exact value  `<authenticationinfo>` to the call to **GetAuthenticationInfo** if it supports the version of Office passed in as a parameter.</span></span> 
  
4. <span data-ttu-id="ef468-172">Если клиентское приложение обмена мгновенными Сообщениями не возвращает значение, приложение Office вызывает метод **GetAuthenticationInfo** еще раз с помощью следующего наивысшей поддерживаемой версии Microsoft Office (например, «14.0.0.0»).</span><span class="sxs-lookup"><span data-stu-id="ef468-172">If the IM client application fails to return a value, the Office application calls the **GetAuthenticationInfo** method again with the next highest supported version of Office (for example, "14.0.0.0").</span></span> 
    
5. <span data-ttu-id="ef468-173">Когда Office определяет, что клиентское приложение обмена мгновенными Сообщениями поддерживает интеграцию обмена мгновенными Сообщениями и присутствия, подключается к необходимый набор интерфейсов для завершения инициализации.</span><span class="sxs-lookup"><span data-stu-id="ef468-173">Once Office determines that the IM client application supports IM and presence integration, it connects to a required set of interfaces to finish initializing.</span></span> <span data-ttu-id="ef468-174">(Для получения дополнительных сведений см [необходимых интерфейсов](#off15_IMIntegration_HowConnect).)</span><span class="sxs-lookup"><span data-stu-id="ef468-174">(For more information, see [Connecting to required interfaces](#off15_IMIntegration_HowConnect).)</span></span>
    
<span data-ttu-id="ef468-175">Если приложение Office возникает ошибка на каком указанные выше шаги, отклоняться и интеграции присутствия не установлено во время сеанса приложения Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-175">If the Office application encounters an error on any of the steps above, it backs out and presence integration is not established again during the session of the Office application.</span></span> 
  
### <a name="connecting-to-required-interfaces"></a><span data-ttu-id="ef468-176">Подключение к необходимых интерфейсов</span><span class="sxs-lookup"><span data-stu-id="ef468-176">Connecting to required interfaces</span></span>
<span data-ttu-id="ef468-177"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-177"></span></span>

<span data-ttu-id="ef468-178">После проверки подлинности подключения к клиентскому приложению обмена мгновенными Сообщениями, приложение Office пытается подключиться к набор необходимых интерфейсов, которые должны предоставлять клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-178">After authenticating the connection to the IM client application, the Office application attempts to connect to a set of required interfaces that the IM client application must expose.</span></span> <span data-ttu-id="ef468-179">Приложение Office это достигается следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ef468-179">The Office application accomplishes this by doing the following:</span></span>
  
- <span data-ttu-id="ef468-180">Приложение Office получает [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) объект путем вызова метода **IUCOfficeIntegration.GetInterface** , передав в **oiInterfaceLyncClient** константа из перечисления [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) .</span><span class="sxs-lookup"><span data-stu-id="ef468-180">The Office application gets an [ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceLyncClient** constant from the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> 
    
- <span data-ttu-id="ef468-181">Приложение Office получает [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) объект путем вызова метода **IUCOfficeIntegration.GetInterface** , передав в **oiInterfaceAutomation** константа из перечисления **OIInterface** .</span><span class="sxs-lookup"><span data-stu-id="ef468-181">The Office application gets an [IAutomation](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation) object by calling the **IUCOfficeIntegration.GetInterface** method, passing in the **oiInterfaceAutomation** constant from the **OIInterface** enumeration.</span></span> 
    
- <span data-ttu-id="ef468-182">Прослушиватель событий [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) устанавливает приложение Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-182">The Office application sets up the [_ILyncClientEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient) event listener.</span></span> 
    
- <span data-ttu-id="ef468-183">Прослушиватель событий [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) устанавливает приложение Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-183">The Office application sets up the [_IUCOfficeIntegrationEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration) event listener.</span></span> 
    
- <span data-ttu-id="ef468-184">Приложение Office получает состояние входа из клиентского приложения обмена мгновенными Сообщениями с помощью свойства **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="ef468-184">The Office application gets the sign-in state from the IM client application by accessing the **ILyncClient.State** property.</span></span> 
    
- <span data-ttu-id="ef468-185">Приложение Office получает возможности обмена мгновенными Сообщениями клиентского приложения путем вызова метода **IUCOfficeIntegration.GetSupportedFeatures** , который возвращает флаг из перечисления [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="ef468-185">The Office application gets the capabilities of the IM client application by calling the **IUCOfficeIntegration.GetSupportedFeatures** method, which returns a flag from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> 
    
- <span data-ttu-id="ef468-186">Приложение Office обращается к свойству **ILyncClient.Self** , чтобы получить ссылку на объект [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="ef468-186">The Office application accesses the **ILyncClient.Self** property to get a reference to an [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) object.</span></span> 
    
### <a name="retrieving-the-capabilities-of-the-local-user"></a><span data-ttu-id="ef468-187">Извлечение возможности локального пользователя</span><span class="sxs-lookup"><span data-stu-id="ef468-187">Retrieving the capabilities of the local user</span></span>
<span data-ttu-id="ef468-188"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-188"></span></span>

<span data-ttu-id="ef468-189">Приложение Office возвращает сведения о возможностях локального пользователя, выполните следующее:</span><span class="sxs-lookup"><span data-stu-id="ef468-189">The Office application gets the capabilities of the local user by doing the following:</span></span>
  
1. <span data-ttu-id="ef468-190">Если клиентское приложение обмена мгновенными Сообщениями поддерживает интерфейс **IClient2** , Office пытается получить объект [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) с помощью свойства **IClient2.PrivateContactManager** .</span><span class="sxs-lookup"><span data-stu-id="ef468-190">If the IM client application supports the **IClient2** interface, Office tries to get an [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) object by accessing the **IClient2.PrivateContactManager** property.</span></span> 
    
2. <span data-ttu-id="ef468-191">Если приложение обмена мгновенными Сообщениями не поддерживает интерфейс **IClient2** , приложение Office возвращает объект **IContactManager** с помощью свойства **ILyncClient.ContactManager** .</span><span class="sxs-lookup"><span data-stu-id="ef468-191">If the IM application does not support the **IClient2** interface, Office application gets an **IContactManager** object by accessing the **ILyncClient.ContactManager** property.</span></span> <span data-ttu-id="ef468-192">Клиентское приложение обмена мгновенными Сообщениями успешно должен возвращать объект **IContactManager** , прежде чем можно установить другие возможности обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-192">The IM client application must successfully return an **IContactManager** object before any other IM capabilities can be established.</span></span> 
    
3. <span data-ttu-id="ef468-193">Приложение Office обращается к свойству **ILyncClient.Uri** и затем вызывает **IContactManager.GetContactByUri** для получения объекта [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) , связанный с локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-193">The Office application accesses the **ILyncClient.Uri** property and then calls **IContactManager.GetContactByUri** to get the [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) object associated with the local user.</span></span> 
    
4. <span data-ttu-id="ef468-194">Затем приложение Office вызывает несколько **IContact.CanStart** для установления возможности локального пользователя, передав значения для **ModalityTypes.ucModalityInstantMessage** и **ModalityTypes.ucModalityAudioVideo** последовательно.</span><span class="sxs-lookup"><span data-stu-id="ef468-194">The Office application then makes several calls to **IContact.CanStart** to establish the capabilities of the local user, passing in the values for **ModalityTypes.ucModalityInstantMessage** and **ModalityTypes.ucModalityAudioVideo** successively.</span></span> 
    
### <a name="retrieving-contact-presence"></a><span data-ttu-id="ef468-195">Получение контактных сведений о присутствии</span><span class="sxs-lookup"><span data-stu-id="ef468-195">Retrieving contact presence</span></span>
<span data-ttu-id="ef468-196"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-196"></span></span>

<span data-ttu-id="ef468-197">Приложение Office возвращает контактных сведений о присутствии, включая локального пользователя, выполните следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ef468-197">The Office application gets contact presence, including the local user, by doing the following:</span></span> 
  
1. <span data-ttu-id="ef468-198">Приложение Office вызывает **IContact.GetContactInformation** для получения сведений о присутствии элемента с контактом.</span><span class="sxs-lookup"><span data-stu-id="ef468-198">The Office application calls **IContact.GetContactInformation** to get a presence item from the contact.</span></span> 
    
2. <span data-ttu-id="ef468-199">Затем приложение Office подписывается на изменения состояния присутствия контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-199">The Office application then subscribes to presence status changes from the contact.</span></span> <span data-ttu-id="ef468-200">Он вызывает **IContactManager.CreateSubscription** для получения объекта [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="ef468-200">It calls **IContactManager.CreateSubscription** to get an [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) object.</span></span> <span data-ttu-id="ef468-201">Он вызывает **IContactSubscription.AddContact** , чтобы добавить контакт с подпиской и затем вызывает **IContactSubscription.Subscribe** для получения изменений в состояние контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-201">It then calls **IContactSubscription.AddContact** to add the contact to the subscription and then calls **IContactSubscription.Subscribe** to get changes in the contact's status.</span></span> 
    
3. <span data-ttu-id="ef468-202">Если приложение обмена мгновенными Сообщениями поддерживает **IContact2**, Office пытается получить сведения о присутствии, вызвав **IContact2.BatchGetContactInformation2**.</span><span class="sxs-lookup"><span data-stu-id="ef468-202">If the IM application supports **IContact2**, Office attempts to get presence information by calling **IContact2.BatchGetContactInformation2**.</span></span>
    
4. <span data-ttu-id="ef468-203">Затем приложение Office получает свойства присутствия контакта путем вызова **IContact.BatchGetContactInformation**.</span><span class="sxs-lookup"><span data-stu-id="ef468-203">The Office application then retrieves the presence properties for the contact by calling **IContact.BatchGetContactInformation**.</span></span> <span data-ttu-id="ef468-204">Приложение Office можно получить, обратившись к свойству **IContact.Settings** второй набор свойств, сведения о присутствии.</span><span class="sxs-lookup"><span data-stu-id="ef468-204">The Office application can get a second set of presence properties by accessing the **IContact.Settings** property.</span></span> 
    
5. <span data-ttu-id="ef468-205">И, наконец приложение Office получает членство в группах контакта с помощью свойства **IContact.CustomGroups** .</span><span class="sxs-lookup"><span data-stu-id="ef468-205">Finally, the Office application gets the contact's group membership by accessing the **IContact.CustomGroups** property.</span></span> <span data-ttu-id="ef468-206">Возвращает коллекцию [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) , которая включает в себя все объекты [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) , к которым принадлежит контакт.</span><span class="sxs-lookup"><span data-stu-id="ef468-206">This returns an [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) collection that includes all of the [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) objects that the contact belongs to.</span></span> 
    
### <a name="disconnecting-from-the-im-application"></a><span data-ttu-id="ef468-207">Отключение от приложения обмена мгновенными Сообщениями</span><span class="sxs-lookup"><span data-stu-id="ef468-207">Disconnecting from the IM application</span></span>
<span data-ttu-id="ef468-208"><a name="off15_IMIntegration_HowConnect"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-208"></span></span>

<span data-ttu-id="ef468-209">Отключение когда приложение Office 2013 обнаруживает события **OnShuttingDown** из приложения обмена мгновенными Сообщениями, без уведомления.</span><span class="sxs-lookup"><span data-stu-id="ef468-209">When the Office 2013 application detects the **OnShuttingDown** event from the IM application, it disconnects silently.</span></span> <span data-ttu-id="ef468-210">Тем не менее при завершении работы приложения Office перед приложения обмена мгновенными Сообщениями, приложение Office не гарантирует, очистки подключения.</span><span class="sxs-lookup"><span data-stu-id="ef468-210">However, if the Office application shuts down before the IM application, the Office application does not guarantee that the connection is cleaned up.</span></span> <span data-ttu-id="ef468-211">Приложение обмена мгновенными Сообщениями должен обрабатывать утечки подключения клиента.</span><span class="sxs-lookup"><span data-stu-id="ef468-211">The IM application must handle client connection leaks.</span></span> 
  
## <a name="setting-registry-keys-and-entries"></a><span data-ttu-id="ef468-212">Параметр реестра и записей</span><span class="sxs-lookup"><span data-stu-id="ef468-212">Setting registry keys and entries</span></span>
<span data-ttu-id="ef468-213"><a name="off15_IMIntegration_SetRegistry"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-213"></span></span>

<span data-ttu-id="ef468-214">Как уже было сказано ранее, приложения поддержкой обмена мгновенными Сообщениями Office 2013 найдите определенных разделов, записей и значений реестра для обнаружения клиентское приложение обмена мгновенными Сообщениями для подключения к.</span><span class="sxs-lookup"><span data-stu-id="ef468-214">As mentioned previously, the IM-capable Office 2013 applications look for specific keys, entries, and values in the registry to discover the IM client application to connect to.</span></span> <span data-ttu-id="ef468-215">Если эти значения реестра предоставляют приложения Office с помощью имя процесса и CLSID класса, который выступает в качестве точки входа для объектной модели клиентское приложение обмена мгновенными Сообщениями (класс, реализующий интерфейс **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="ef468-215">These registry values provide the Office application with the process name and CLSID of the class that acts as the entry point to the IM client application's object model (that is, the class that implements the **IUCOfficeIntegration** interface).</span></span> <span data-ttu-id="ef468-216">Приложение Office совместно создает этот класс и подключается как клиент COM-сервер вне процесса в клиентском приложении обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-216">The Office application co-creates that class and connects as a client to the out-of-process COM server in the IM client application.</span></span> 
  
<span data-ttu-id="ef468-217">Используйте в таблице 1 для определения клавиши, записи и значения, которые должны быть записаны в реестр, чтобы интегрировать клиентского приложения обмена мгновенными Сообщениями с помощью приложений Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-217">Use Table 1 to identify the keys, entries, and values that must be written in the registry to integrate an IM client application with Office.</span></span>
  
<span data-ttu-id="ef468-218">**В таблице 1. Параметры реестра для настройки клиентского приложения обмена мгновенными Сообщениями по умолчанию**</span><span class="sxs-lookup"><span data-stu-id="ef468-218">**Table 1. Registry keys for setting the default IM client application**</span></span>

|<span data-ttu-id="ef468-219">**Key**</span><span class="sxs-lookup"><span data-stu-id="ef468-219">**Key**</span></span>|<span data-ttu-id="ef468-220">**Запись**</span><span class="sxs-lookup"><span data-stu-id="ef468-220">**Entry**</span></span>|<span data-ttu-id="ef468-221">**Тип**</span><span class="sxs-lookup"><span data-stu-id="ef468-221">**Type**</span></span>|<span data-ttu-id="ef468-222">**Значение**</span><span class="sxs-lookup"><span data-stu-id="ef468-222">**Value**</span></span>|<span data-ttu-id="ef468-223">**Пример**</span><span class="sxs-lookup"><span data-stu-id="ef468-223">**Example**</span></span>|
|:-----|:-----|:-----|:-----|:-----|
|<span data-ttu-id="ef468-224">Поставщики HKEY_LOCAL_MACHINE\Software\IM\\< имя приложения\></span><span class="sxs-lookup"><span data-stu-id="ef468-224">HKEY_LOCAL_MACHINE\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="ef468-225">FriendlyName</span><span class="sxs-lookup"><span data-stu-id="ef468-225">FriendlyName</span></span>  <br/> |<span data-ttu-id="ef468-226">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ef468-226">REG_SZ</span></span>  <br/> |<span data-ttu-id="ef468-227">Имя клиентского приложения обмена мгновенными Сообщениями сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="ef468-227">The name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="ef468-228">Обмен мгновенными Сообщениями Litware 2012 г.</span><span class="sxs-lookup"><span data-stu-id="ef468-228">Litware IM 2012</span></span>  <br/> |
||<span data-ttu-id="ef468-229">ProcessName</span><span class="sxs-lookup"><span data-stu-id="ef468-229">ProcessName</span></span>  <br/> |<span data-ttu-id="ef468-230">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ef468-230">REG_SZ</span></span>  <br/> |<span data-ttu-id="ef468-231">Имя процесса клиентского приложения обмена мгновенными Сообщениями сторонних производителей.</span><span class="sxs-lookup"><span data-stu-id="ef468-231">The process name of the third-party IM client application.</span></span>  <br/> |<span data-ttu-id="ef468-232">Litware.exe</span><span class="sxs-lookup"><span data-stu-id="ef468-232">litware.exe</span></span>  <br/> |
||<span data-ttu-id="ef468-233">GUID</span><span class="sxs-lookup"><span data-stu-id="ef468-233">GUID</span></span>  <br/> |<span data-ttu-id="ef468-234">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ef468-234">REG_SZ</span></span>  <br/> |<span data-ttu-id="ef468-235">Класс ID (CLSID) для корневого, создаваемых посредством функции CoCreateInstance класса в приложении обмена мгновенными Сообщениями (класс, реализующий интерфейс **IUCOfficeIntegration** ).</span><span class="sxs-lookup"><span data-stu-id="ef468-235">A class ID (CLSID) for the root, cocreatable class in the IM application (the class that implements the **IUCOfficeIntegration** interface).</span></span>  <br/> |<span data-ttu-id="ef468-236">(GUID)</span><span class="sxs-lookup"><span data-stu-id="ef468-236">(A GUID)</span></span>  <br/> |
|<span data-ttu-id="ef468-237">Поставщики HKEY_CURRENT_USER\Software\IM</span><span class="sxs-lookup"><span data-stu-id="ef468-237">HKEY_CURRENT_USER\Software\IM Providers</span></span>  <br/> |<span data-ttu-id="ef468-238">DefaultIMApp</span><span class="sxs-lookup"><span data-stu-id="ef468-238">DefaultIMApp</span></span>  <br/> |<span data-ttu-id="ef468-239">REG_SZ</span><span class="sxs-lookup"><span data-stu-id="ef468-239">REG_SZ</span></span>  <br/> |<span data-ttu-id="ef468-240">Имя клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-240">The name of the IM client application.</span></span> <span data-ttu-id="ef468-241">Это должен быть совпадает с именем в верхнего уровня реестра (куст) в разделе HKEY_LOCAL_MACHINE.</span><span class="sxs-lookup"><span data-stu-id="ef468-241">This must be the same as the name at the top-level registry key (hive) in the HKEY_LOCAL_MACHINE.</span></span>  <br/> |<span data-ttu-id="ef468-242">Litware</span><span class="sxs-lookup"><span data-stu-id="ef468-242">Litware</span></span>  <br/> |
|<span data-ttu-id="ef468-243">Поставщики HKEY_CURRENT_USER\Software\IM\\< имя приложения\></span><span class="sxs-lookup"><span data-stu-id="ef468-243">HKEY_CURRENT_USER\Software\IM Providers\\<Application name\></span></span>  <br/> |<span data-ttu-id="ef468-244">UpAndRunning</span><span class="sxs-lookup"><span data-stu-id="ef468-244">UpAndRunning</span></span>  <br/> |<span data-ttu-id="ef468-245">REG_DWORD</span><span class="sxs-lookup"><span data-stu-id="ef468-245">REG_DWORD</span></span>  <br/> | <span data-ttu-id="ef468-246">Целое число от 0 до 2:</span><span class="sxs-lookup"><span data-stu-id="ef468-246">An integer value between 0 and 2:</span></span>  <br/>  <span data-ttu-id="ef468-247">0 — не выполняется</span><span class="sxs-lookup"><span data-stu-id="ef468-247">0—Not running</span></span>  <br/>  <span data-ttu-id="ef468-248">1 — Запуск</span><span class="sxs-lookup"><span data-stu-id="ef468-248">1—Starting</span></span>  <br/>  <span data-ttu-id="ef468-249">2 — под управлением</span><span class="sxs-lookup"><span data-stu-id="ef468-249">2—Running</span></span>  <br/> <br/><span data-ttu-id="ef468-250">**Примечание**: раздел реестра имя приложения должен совпадать с значение параметра DefaultIMApp.</span><span class="sxs-lookup"><span data-stu-id="ef468-250">**NOTE**:  The application name registry key must be the same as the value of the DefaultIMApp entry.</span></span>           ||
   
## <a name="implementing-the-required-interfaces-for-integration-with-office"></a><span data-ttu-id="ef468-251">Реализация необходимые интерфейсы для интеграции с Office</span><span class="sxs-lookup"><span data-stu-id="ef468-251">Implementing the required interfaces for integration with Office</span></span>
<span data-ttu-id="ef468-252"><a name="off15_IMIntegration_ImplementRequired"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-252"></span></span>

<span data-ttu-id="ef468-253">Существует три интерфейса из пространства имен **UCCollaborationLib** , исполняемый файл (или COM-сервера) клиентского приложения обмена мгновенными Сообщениями необходимо применить, чтобы его можно интегрировать с Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-253">There are three interfaces from the **UCCollaborationLib** namespace that the executable (or COM server) of an IM client application must implement so that it can integrate with Office.</span></span> <span data-ttu-id="ef468-254">Если эти интерфейсы не реализованы, приложение Office отклоняться во время инициализации и не установить подключение с помощью клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-254">If these interfaces are not implemented, the Office application backs out during the initialization process and the connection with the IM client application is not established.</span></span> 
  
<span data-ttu-id="ef468-255">Доступны следующие обязательные интерфейсы:</span><span class="sxs-lookup"><span data-stu-id="ef468-255">The required interfaces are as follows:</span></span>
  
- <span data-ttu-id="ef468-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration), но не требуется, интерфейс **_IUCOfficeIntegrationEvents** также должен быть реализован в одном производного класса.</span><span class="sxs-lookup"><span data-stu-id="ef468-256">[IUCOfficeIntegration](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IUCOfficeIntegration)—Although not required, the **_IUCOfficeIntegrationEvents** interface should also be implemented in the same derived class.</span></span> 
    
- <span data-ttu-id="ef468-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient), но не требуется, интерфейс **_ILyncClientEvents** также должен быть реализован в одном производного класса.</span><span class="sxs-lookup"><span data-stu-id="ef468-257">[ILyncClient](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILyncClient)—Although not required, the **_ILyncClientEvents** interface should also be implemented in the same derived class.</span></span> 
    
- [<span data-ttu-id="ef468-258">IAutomation</span><span class="sxs-lookup"><span data-stu-id="ef468-258">IAutomation</span></span>](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IAutomation)
    
### <a name="iucofficeintegration-interface"></a><span data-ttu-id="ef468-259">Интерфейс IUCOfficeIntegration</span><span class="sxs-lookup"><span data-stu-id="ef468-259">IUCOfficeIntegration interface</span></span>
<span data-ttu-id="ef468-260"><a name="off15_IMIntegration_ImplementRequired_IUCOfficeIntegration"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-260"></span></span>

<span data-ttu-id="ef468-261">Интерфейс **IUCOfficeIntegration** предоставляет точки входа для приложения Office, чтобы подключиться к приложению клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-261">The **IUCOfficeIntegration** interface provides the entry-point for an Office application to connect to the IM client application.</span></span> <span data-ttu-id="ef468-262">Интерфейс определяет три метода, которые приложение Office вызывает как часть процесса осуществить соединение с клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-262">The interface defines three methods that an Office application calls as part of the process of initiating a connection with the IM client application.</span></span> <span data-ttu-id="ef468-263">Класс, реализующий интерфейс **IUCOfficeIntegration** должен быть совместного открыты, чтобы Office совместного можно создать его экземпляр.</span><span class="sxs-lookup"><span data-stu-id="ef468-263">The class that implements the **IUCOfficeIntegration** interface must be co-creatable so that Office can co-create an instance of it.</span></span> <span data-ttu-id="ef468-264">Кроме того он должен предоставлять CLSID, которое вводится как значение GUID запись в раздел реестра HKEY_LOCAL_MACHINE\Software\IM Providers\ _имя приложения_ .</span><span class="sxs-lookup"><span data-stu-id="ef468-264">In addition, it must expose the CLSID that is entered as the value for the GUID entry in the HKEY_LOCAL_MACHINE\Software\IM Providers\  _Application name_ registry key.</span></span> 
  
<span data-ttu-id="ef468-265">Класс, который наследует от **IUCOfficeIntegration** также требуется реализовать интерфейс **_IUCOfficeIntegrationEvents** .</span><span class="sxs-lookup"><span data-stu-id="ef468-265">The class that inherits from **IUCOfficeIntegration** should also implement the **_IUCOfficeIntegrationEvents** interface.</span></span> <span data-ttu-id="ef468-266">Интерфейс **_IUCOfficeIntegrationEvents** содержит элементы, которые предоставляют доступ к обработчики событий интерфейса **IUCOfficeIntegration** .</span><span class="sxs-lookup"><span data-stu-id="ef468-266">The **_IUCOfficeIntegrationEvents** interface contains the members that expose the event handlers of the **IUCOfficeIntegration** interface.</span></span> 
  
<span data-ttu-id="ef468-267">В таблице 2 показаны элементы, которые должны быть реализованы в классе, который наследует от **IUCOfficeIntegration** и **_IUCOfficeIntegration**.</span><span class="sxs-lookup"><span data-stu-id="ef468-267">Table 2 shows the members that must be implemented in the class that inherits from **IUCOfficeIntegration** and **_IUCOfficeIntegration**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-268">Дополнительные сведения о **IUCOfficeIntegration** и **_IUCOfficeIntegrationEvents** интерфейсы и их члены можно [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) и [UCCollaborationLib._IUCOfficeIntegrationEvents ](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span><span class="sxs-lookup"><span data-stu-id="ef468-268">For more information about the **IUCOfficeIntegration** and **_IUCOfficeIntegrationEvents** interfaces and their members, see [UCCollaborationLib.IUCOfficeIntegration](http://msdn.microsoft.com/library/UCCollaborationLib.IUCOfficeIntegration) and [UCCollaborationLib._IUCOfficeIntegrationEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IUCOfficeIntegrationEvents).</span></span> 
  
<span data-ttu-id="ef468-269">**В таблице 2. Реализация интерфейсов IUCOfficeIntegration и _IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-269">**Table 2. Implementation of the IUCOfficeIntegration and _IUCOfficeIntegrationEvents interfaces**</span></span>

|<span data-ttu-id="ef468-270">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="ef468-270">**Interface**</span></span>|<span data-ttu-id="ef468-271">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-271">**Member**</span></span>|<span data-ttu-id="ef468-272">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-272">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef468-273">**IUCOfficeIntegration**</span><span class="sxs-lookup"><span data-stu-id="ef468-273">**IUCOfficeIntegration**</span></span> <br/> |<span data-ttu-id="ef468-274">Метод **GetAuthenticationInfo**</span><span class="sxs-lookup"><span data-stu-id="ef468-274">**GetAuthenticationInfo** method</span></span>  <br/> |<span data-ttu-id="ef468-275">Получает строку, сведения о проверки подлинности.</span><span class="sxs-lookup"><span data-stu-id="ef468-275">Gets the authentication info string.</span></span>  <br/> |
||<span data-ttu-id="ef468-276">Метод **GetInterface**</span><span class="sxs-lookup"><span data-stu-id="ef468-276">**GetInterface** method</span></span>  <br/> |<span data-ttu-id="ef468-277">Получает интерфейс определенной версии.</span><span class="sxs-lookup"><span data-stu-id="ef468-277">Gets the interface of a particular version.</span></span>  <br/> |
||<span data-ttu-id="ef468-278">Метод **GetSupportedFeatures**</span><span class="sxs-lookup"><span data-stu-id="ef468-278">**GetSupportedFeatures** method</span></span>  <br/> |<span data-ttu-id="ef468-279">Получает поддерживаемые функции интеграции с Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-279">Gets the supported Office integration features.</span></span>  <br/> |
|<span data-ttu-id="ef468-280">**_IUCOfficeIntegrationEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-280">**_IUCOfficeIntegrationEvents**</span></span> <br/> |<span data-ttu-id="ef468-281">Событие **OnShuttingDown**</span><span class="sxs-lookup"><span data-stu-id="ef468-281">**OnShuttingDown** event</span></span>  <br/> |<span data-ttu-id="ef468-282">Событие, возникающее при попытке завершить работу клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-282">The event raised when the IM client application is trying to shut down.</span></span>  <br/> |
   
<span data-ttu-id="ef468-283">Используйте следующий код для определения класса, наследуемого от интерфейсов **IUCOfficeIntegration** и **_IUCOfficeIntegration** в приложении клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-283">Use the following code to define a class that inherits from the **IUCOfficeIntegration** and **_IUCOfficeIntegration** interfaces within an IM client application.</span></span> 
  
```cs
// An example of a class that can be co-created and can integrate
// with Office as an IM provider.
[ClassInterface(ClassInterfaceType.None)]
[ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
[Guid("{CLSID value}"), ComVisible(true)]
public class LitwareClientAppObject : IUCOfficeIntegration
{
    // Implementation details omitted.
}

```

<span data-ttu-id="ef468-284">Метод **GetAuthenticationInfo** принимает строку, в качестве аргумента для параметра _версии_ .</span><span class="sxs-lookup"><span data-stu-id="ef468-284">The **GetAuthenticationInfo** method takes a string as an argument for the  _version_ parameter.</span></span> <span data-ttu-id="ef468-285">Когда приложение Office вызывает этот метод, передается в одном из двух строк для аргумента, в зависимости от версии Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-285">When the Office application calls this method, it passes in one of two strings for the argument, depending on the version of Office.</span></span> <span data-ttu-id="ef468-286">Когда приложение Office предоставляет метод с версии Office, которая поддерживает клиентское приложение обмена мгновенными Сообщениями (то есть, поддерживает функциональные возможности), метод **GetAuthenticationInfo** возвращает строку XML-кодом `<authenticationinfo>`.</span><span class="sxs-lookup"><span data-stu-id="ef468-286">When the Office application supplies the method with the version of Office that the IM client application supports (that is, supports the functionality), the **GetAuthenticationInfo** method returns a hard-coded XML string `<authenticationinfo>`.</span></span> 
  
<span data-ttu-id="ef468-287">Используйте следующий код для реализации метода **GetAuthentication** в код приложения клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-287">Use the following code to implement the **GetAuthentication** method within the IM client application code.</span></span> 
  
```cs
public string GetAuthenticationInfo(string _version)
{
    // Define the version of Office that the IM client application supports.
    string supportedOfficeVersion = "15.0.0.0";
    // Do a simple check for equivalency.
    if (supportedOfficeVersion == _version)
    {
        // If the version of Office is supported, this method must 
        // return the string literal "<authenticationinfo>" exactly.
        return "<authenticationinfo>";
    }
    else
    {
        return null;
    }
}

```

<span data-ttu-id="ef468-288">Метод **GetInterface** передвигаются ссылки на классы коду вызова, в зависимости от того, что передается в качестве аргумента для параметра _интерфейса_ .</span><span class="sxs-lookup"><span data-stu-id="ef468-288">The **GetInterface** method shuttles references to classes to the calling code, depending on what is passed in as an argument for the  _interface_ parameter.</span></span> <span data-ttu-id="ef468-289">Когда приложение Office вызывает метод **GetInterface** , передается в одно из двух значений для параметра интерфейса: константа **oiInterfaceILyncClient** (1) или константа **oiInterfaceIAutomation** (2) из [ UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) перечисления.</span><span class="sxs-lookup"><span data-stu-id="ef468-289">When an Office application calls the **GetInterface** method, it passes in one of two values for the interface parameter: either the **oiInterfaceILyncClient** constant (1) or the **oiInterfaceIAutomation** constant (2) of the [UCCollaborationLib.OIInterface](http://msdn.microsoft.com/library/UCCollaborationLib.OIInterface) enumeration.</span></span> <span data-ttu-id="ef468-290">Если приложение Office передает **oiInterfaceILyncClient** константу, метод **GetInterface** возвращает ссылку на класс, реализующий интерфейс **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="ef468-290">If the Office application passes in the **oiInterfaceILyncClient** constant, the **GetInterface** method returns a reference to a class that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="ef468-291">Если приложение Office передает **oiInterfaceIAutomation** константу, метод **GetInterface** возвращает класс, реализующий интерфейс **IAutomation** .</span><span class="sxs-lookup"><span data-stu-id="ef468-291">If the Office application passes in the **oiInterfaceIAutomation** constant, the **GetInterface** method returns a class that implements the **IAutomation** interface.</span></span> 
  
<span data-ttu-id="ef468-292">Используйте следующий пример кода для реализации метода **GetInterface** в код приложения клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-292">Use the following code example to implement the **GetInterface** method within the IM client application code.</span></span> 
  
```cs
public object GetInterface(string _version, OIInterface _interface)
{
    // These objects implement the ILyncClient or IAutomation 
    // interfaces respectively. There is no restriction on what these
    // classes are named.
    IMClient imClient = new IMClient();
    IMClientAutomation imAutomation = new IMClientAutomation();
    // Return different object references depending on the value passed in
    // for the _interface parameter.
    switch (_interface)
    {
        // The calling code is asking for an object that inherits
        // from ILyncClient, so it returns such an object.
        case OIInterface.oiInterfaceILyncClient:
        {
            return imClient;
        }
        // The calling code is asking for an object that inherits
        // from IAutomation, so it returns such an object.
        case OIInterface.oiInterfaceIAutomation:
        {
            return imAutomation;
        }
        default:
        {
            throw new NotImplementedException();
        }
    }
}

```

<span data-ttu-id="ef468-293">Метод **GetSupportedFeatures** возвращает сведения о функции обмена мгновенными Сообщениями, которые поддерживает клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-293">The **GetSupportedFeatures** method returns information about the IM features that the IM client application supports.</span></span> <span data-ttu-id="ef468-294">Она принимает строку, для его единственный параметр _версии_.</span><span class="sxs-lookup"><span data-stu-id="ef468-294">It takes a string for its only parameter,  _version_.</span></span> <span data-ttu-id="ef468-295">Когда приложение Office вызывает метод **GetSupportFeatures** , метод возвращает значение из перечисления [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) .</span><span class="sxs-lookup"><span data-stu-id="ef468-295">When the Office application calls the **GetSupportFeatures** method, the method returns a value from the [UCCollaborationLib.OIFeature](http://msdn.microsoft.com/library/UCCollaborationLib.OIFeature) enumeration.</span></span> <span data-ttu-id="ef468-296">Возвращаемое значение указывает возможности клиент обмена мгновенными Сообщениями, где каждой возможности обмена мгновенными Сообщениями клиентского приложения указывается в приложение Office, добавив флаг значение.</span><span class="sxs-lookup"><span data-stu-id="ef468-296">The returned value specifies the capabilities of the IM client, where each capability of the IM client application is indicated to the Office application by adding a flag to the value.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="ef468-297">Приложения Office 2013 игнорировать следующие константы в перечислении **OIFeature** :</span><span class="sxs-lookup"><span data-stu-id="ef468-297">Office 2013 applications ignore the following constants in the **OIFeature** enumeration:</span></span> 
> - <span data-ttu-id="ef468-298">**oiFeaturePictures** (2)</span><span class="sxs-lookup"><span data-stu-id="ef468-298">**oiFeaturePictures** (2)</span></span> 
> - <span data-ttu-id="ef468-299">**oiFeatureFreeBusyIntegration**</span><span class="sxs-lookup"><span data-stu-id="ef468-299">**oiFeatureFreeBusyIntegration**</span></span>
> - <span data-ttu-id="ef468-300">**oiFeaturePhoneNormalization**</span><span class="sxs-lookup"><span data-stu-id="ef468-300">**oiFeaturePhoneNormalization**</span></span>
  
<span data-ttu-id="ef468-301">Используйте следующий пример кода для реализации метода **GetSupportFeatures** в код приложения клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-301">Use the following code example to implement the **GetSupportFeatures** method within the IM client application code.</span></span> 
  
```cs
public OIFeature GetSupportedFeatures(string _version)
{
    OIFeature supportedFeature1 = OIFeature.oiFeatureQuickContacts;
    OIFeature supportedFeature2 = OIFeature.oiFeatureFastSearch;
    return (supportedFeature1 | supportedFeature2);
}

```

### <a name="ilyncclient-interface"></a><span data-ttu-id="ef468-302">Интерфейс ILyncClient</span><span class="sxs-lookup"><span data-stu-id="ef468-302">ILyncClient interface</span></span>
<span data-ttu-id="ef468-303"><a name="off15_IMIntegration_ImplementRequired_ILyncClient"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-303"></span></span>

<span data-ttu-id="ef468-304">Интерфейс **ILyncClient** сопоставляет возможности обмена мгновенными Сообщениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-304">The **ILyncClient** interface maps to the capabilities of the IM client application itself.</span></span> <span data-ttu-id="ef468-305">Она предоставляет свойства, связанные с человека, который вошел в приложении (локальный пользователь, представленный в интерфейсе [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) ), состояние приложения, в списке контактов для локального пользователя и некоторые другие параметры.</span><span class="sxs-lookup"><span data-stu-id="ef468-305">It exposes properties that refer to the person who is signed into the application (the local user, represented by the [UCCollaborationLib.ISelf](http://msdn.microsoft.com/library/UCCollaborationLib.ISelf) interface), the state of the application, the list of contacts for the local user, and several other settings.</span></span> <span data-ttu-id="ef468-306">Когда она пытается подключиться к приложению клиент обмена мгновенными Сообщениями, приложение Office получает ссылку на объект, реализующий интерфейс **ILyncClient** .</span><span class="sxs-lookup"><span data-stu-id="ef468-306">When it's trying to connect to the IM client application, the Office application gets a reference to an object that implements the **ILyncClient** interface.</span></span> <span data-ttu-id="ef468-307">По этой ссылки Office может получить доступ практически возможности обмена мгновенными Сообщениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-307">From that reference, Office can access much of the functionality of the IM client application.</span></span> 
  
<span data-ttu-id="ef468-308">Кроме того класс, реализующий интерфейс **ILyncClient** также требуется реализовать интерфейс **_ILyncClientEvents** .</span><span class="sxs-lookup"><span data-stu-id="ef468-308">In addition, the class that implements the **ILyncClient** interface should also implement the **_ILyncClientEvents** interface.</span></span> <span data-ttu-id="ef468-309">Интерфейс **_ILyncClientEvents** предоставляет несколько событий, которые необходимы для отслеживания состояния клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-309">The **_ILyncClientEvents** interface exposes several of the events that are required for monitoring the state of the IM client application.</span></span> 
  
<span data-ttu-id="ef468-310">В таблице 3 показаны элементы, которые должны быть реализованы в классе, который наследует от **ILyncClient** и **_ILyncClientEvents**.</span><span class="sxs-lookup"><span data-stu-id="ef468-310">Table 3 shows the members that must be implemented in the class that inherits from **ILyncClient** and **_ILyncClientEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-311">Любой участник **ILyncClient** или ** \_ILyncClientEvents** интерфейс, не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-311">Any member of the **ILyncClient** or **\_ILyncClientEvents** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-312">Члены, которые являются существует, но не реализовано может вызывать **NotImplementedException** или **E\_NOTIMPL** ошибка.</span><span class="sxs-lookup"><span data-stu-id="ef468-312">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="ef468-313">Дополнительные сведения о **ILyncClient** и **_ILyncClientEvents** интерфейсы и их члены можно [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) и [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span><span class="sxs-lookup"><span data-stu-id="ef468-313">For more information about the **ILyncClient** and **_ILyncClientEvents** interfaces and their members, see [UCCollaborationLib.ILyncClient](http://msdn.microsoft.com/library/UCCollaborationLib.ILyncClient) and [UCCollaborationLib._ILyncClientEvents](http://msdn.microsoft.com/library/UCCollaborationLib._ILyncClientEvents).</span></span> 
  
<span data-ttu-id="ef468-314">**В таблице 3. Реализация интерфейсов ILyncClient и ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-314">**Table 3. Implementation of ILyncClient and ILyncClientEvents interfaces**</span></span>

|<span data-ttu-id="ef468-315">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="ef468-315">**Interface**</span></span>|<span data-ttu-id="ef468-316">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-316">**Member**</span></span>|<span data-ttu-id="ef468-317">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-317">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef468-318">**ILyncClient**</span><span class="sxs-lookup"><span data-stu-id="ef468-318">**ILyncClient**</span></span> <br/> |<span data-ttu-id="ef468-319">Свойство **ContactManager**</span><span class="sxs-lookup"><span data-stu-id="ef468-319">**ContactManager** property</span></span>  <br/> |<span data-ttu-id="ef468-320">Возвращает диспетчер группы контактов.</span><span class="sxs-lookup"><span data-stu-id="ef468-320">Gets the contact group manager.</span></span>  <br/> |
||<span data-ttu-id="ef468-321">Свойство **ConversationManager**</span><span class="sxs-lookup"><span data-stu-id="ef468-321">**ConversationManager** property</span></span>  <br/> |<span data-ttu-id="ef468-322">Возвращает диспетчер бесед.</span><span class="sxs-lookup"><span data-stu-id="ef468-322">Gets the conversations manager.</span></span>  <br/> |
||<span data-ttu-id="ef468-323">Свойство **SELF**</span><span class="sxs-lookup"><span data-stu-id="ef468-323">**Self** property</span></span>  <br/> |<span data-ttu-id="ef468-324">Получает объект **Self** .</span><span class="sxs-lookup"><span data-stu-id="ef468-324">Gets the **Self** object.</span></span>  <br/> |
||<span data-ttu-id="ef468-325">Метод **Вход**</span><span class="sxs-lookup"><span data-stu-id="ef468-325">**SignIn** method</span></span>  <br/> |<span data-ttu-id="ef468-326">Запускает обмена мгновенными Сообщениями клиентского приложения входа в процесс с определенным доступности.</span><span class="sxs-lookup"><span data-stu-id="ef468-326">Starts the IM client application sign-in process with a specific availability.</span></span>  <br/> |
||<span data-ttu-id="ef468-327">Свойство **состояний**</span><span class="sxs-lookup"><span data-stu-id="ef468-327">**State** property</span></span>  <br/> |<span data-ttu-id="ef468-328">Возвращает текущее состояние платформы.</span><span class="sxs-lookup"><span data-stu-id="ef468-328">Gets the current platform state.</span></span>  <br/> |
||<span data-ttu-id="ef468-329">Свойство **URI**</span><span class="sxs-lookup"><span data-stu-id="ef468-329">**Uri** property</span></span>  <br/> |<span data-ttu-id="ef468-330">Возвращает URI клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-330">Gets the URI of the IM client application.</span></span>  <br/> |
|<span data-ttu-id="ef468-331">**_ILyncClientEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-331">**_ILyncClientEvents**</span></span> <br/> |<span data-ttu-id="ef468-332">Событие **OnStateChanged**</span><span class="sxs-lookup"><span data-stu-id="ef468-332">**OnStateChanged** event</span></span>  <br/> |<span data-ttu-id="ef468-333">Возникает при изменении состояния приложения клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-333">Raised when the IM client application state changes.</span></span> <span data-ttu-id="ef468-334">Необходимо обрабатывать и получить свойство **eventData.NewState** .</span><span class="sxs-lookup"><span data-stu-id="ef468-334">You should handle this event and get the **eventData.NewState** property.</span></span> <span data-ttu-id="ef468-335">Событие все процессы, привязанного к экземпляру клиентского приложения обмена мгновенными Сообщениями, когда все подсистемы в приложении вызывает изменение состояния.</span><span class="sxs-lookup"><span data-stu-id="ef468-335">The event is raised for all processes bound to an instance of an IM client application when any subsystem in the application causes the state change.</span></span>  <br/> |
   
<span data-ttu-id="ef468-336">Во время инициализации Office обращается к свойству **ILyncClient.State** .</span><span class="sxs-lookup"><span data-stu-id="ef468-336">During the initialization process, Office accesses the **ILyncClient.State** property.</span></span> <span data-ttu-id="ef468-337">Это свойство должен возвращать значение из перечисления [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) .</span><span class="sxs-lookup"><span data-stu-id="ef468-337">This property needs to return a value from the [UCCollaborationLib.ClientState](http://msdn.microsoft.com/library/UCCollaborationLib.ClientState) enumeration.</span></span> 
  
```cs
private ClientState _clientState;
public ClientState State
{
    get
    {
        return this._clientState;
    }
}

```

<span data-ttu-id="ef468-338">Свойство **State** сохраняет текущее состояние клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-338">The **State** property stores the current status of the IM client application.</span></span> <span data-ttu-id="ef468-339">Необходимо установить и обновлено в течение всего сеанса обмена мгновенными Сообщениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-339">It must be set and updated throughout the IM client application session.</span></span> <span data-ttu-id="ef468-340">Когда обмен мгновенными Сообщениями клиентское приложение входит в, выходит или завершает работу, его следует установить свойство **состояний** .</span><span class="sxs-lookup"><span data-stu-id="ef468-340">When the IM client application signs in, signs out, or shuts down, it should set the **State** property.</span></span> <span data-ttu-id="ef468-341">Рекомендуется устанавливать это свойство в методы **ILyncClient.SignIn** и **ILyncClient.SignOut** , как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="ef468-341">It is best to set this property within the **ILyncClient.SignIn** and **ILyncClient.SignOut** methods, as the following example demonstrates.</span></span> 
  
```cs
// This field is of a type that implements the 
// IAsynchronousOperation interface.
private IMClientAsyncOperation _asyncOperation = new IMClientAsyncOperation();
// This field is of a type that implements the ISelf interface.
private IMClientSelf _self;
public IMClientAsyncOperation SignIn(string _userUri, string _domainAndUser, 
    string _password, object _IMClientCallback, object _state)
{
    ClientState _previousClientState = this._clientState;
    this._clientState = ClientState.ucClientStateSignedIn;
    // The IMClientStateChangedEventData class implements the 
    // IClientStateChangedEventData interface.
    IMClientStateChangedEventData eventData = 
        new IMClientStateChangedEventData(_previousClientState, 
        this._clientState);
    if (_userUri != null)
    {
        // During the sign-in process, create a new contact with
        // the contact information of the currently signed-in user.
        this._self = new IMClientSelf(IMContact.BuildContact(_userUri));
    }
    // Raise the _ILyncClientEvents.OnStateChanged event.
    OnStateChanged(this, eventData as UC.ClientStateChangedEventData);
    
    return this._asyncOperation;
    }
}

```

<span data-ttu-id="ef468-342">В следующем примере кода показано, как настроить прослушиватель событий, с помощью _ **ILyncClientEvents** и _ **IUCOfficeIntegrationEvents** интерфейсов.</span><span class="sxs-lookup"><span data-stu-id="ef468-342">The following code example demonstrates how to set up the event listener using the _ **ILyncClientEvents** and _ **IUCOfficeIntegrationEvents** interfaces.</span></span> 
  
```cs
using Microsoft.Office.Uc;
using System;
using System.Runtime.CompilerServices;
using System.Runtime.InteropServices;
namespace SampleImplementation
{
    // Note: UCOfficeIntegration inherits from both IUCOfficeIntegration and _IUCOfficeIntegrationEvents_Event
    [ClassInterface(ClassInterfaceType.None), Guid("13c41ef9-eb90-4e94-8a7c-1e9d686bc019"), ComVisible(true)]
    [ComSourceInterfaces(typeof(_IUCOfficeIntegrationEvents))]
    public class MyInstantMessengerOfficeIntegration : UCOfficeIntegration
    {
        #region IUCOfficeIntegration implementation
        public string GetAuthenticationInfo(string _version)
        {
            return "";
        }
        public object GetInterface(string _version, OIInterface _interface)
        {
            return null;
        }
        public OIFeature GetSupportedFeatures(string _version)
        {
            return OIFeature.oiFeatureAddOneNoteToConversation;
        }
        #endregion
        #region _IUCOfficeIntegrationEvents support
        // This event implements void _IUCOfficeIntegrationEvents.OnShuttingDown();
        public event _IUCOfficeIntegrationEvents_OnShuttingDownEventHandler OnShuttingDown;
        // This method is called by the IM application when it is beginning to shut down.
        // The method will raise the OnShuttingDown event which is translated by .NET COM interop layer
        // into a call to _IUCOfficeIntegrationEvents.OnShuttingDown.
        // This notifies Office applications that the IM application is going away.
        internal void RaiseOnShuttingDownEvent()
        {
            if (this.OnShuttingDown != null)
            {
                this.OnShuttingDown();
            }
        }
        #endregion
    }
    // Note: LyncClient inherits from both ILyncClient and _ILyncClientEvents_Event
    // You must implement LyncClient because the event handlers in _ILyncClientEvents expect you to pass a LyncClient interface.
    [ComVisible(true)]
    [ComSourceInterfaces(typeof(_ILyncClientEvents))]
    public class MyInstantMessengerOfficeIntegration2 :
        Client,
        Client2,
        LyncClient
    {
        #region Interfaces
        public LyncClientCapabilityTypes Capabilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConferenceScheduler ConferenceScheduler
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager ContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ConversationManager ConversationManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DelegatorClient[] DelegatorClients
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public DeviceManager DeviceManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public bool InSuppressedMode
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ContactManager PrivateContactManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public RoomManager RoomManager
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Self Self
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientSettings Settings
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public SignInConfiguration SignInConfiguration
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientState State
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ClientType Type
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public string Uri
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public Utilities Utilities
        {
            get
            {
                throw new NotImplementedException();
            }
        }
        public ApplicationRegistration CreateApplicationRegistration(string _appGuid, string _appName)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Initialize(string _clientName, string _version = "0", string _clientShortName = "0", string _clientNameAbbreviation = "0", string _clientLongName = "0", SupportedFeatures _supportedFeatures = SupportedFeatures.ucAllFeatures, [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation Shutdown([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignIn(string _userUri = "0", string _domainAndUsername = "0", string _password = "0", [IUnknownConstant] object _CommunicatorClientCallback = null, object _state = null)
        {
            throw new NotImplementedException();
        }
        public AsynchronousOperation SignOut([IUnknownConstant] object _CommunicatorClientCallback, object _state)
        {
            throw new NotImplementedException();
        }
        #endregion
        #region _ILyncClientEvents support
        public event _ILyncClientEvents_OnStateChangedEventHandler OnStateChanged;
        public event _ILyncClientEvents_OnNotificationReceivedEventHandler OnNotificationReceived;
        public event _ILyncClientEvents_OnCredentialRequestedEventHandler OnCredentialRequested;
        public event _ILyncClientEvents_OnSignInDelayedEventHandler OnSignInDelayed;
        public event _ILyncClientEvents_OnCapabilitiesChangedEventHandler OnCapabilitiesChanged;
        public event _ILyncClientEvents_OnDelegatorClientAddedEventHandler OnDelegatorClientAdded;
        public event _ILyncClientEvents_OnDelegatorClientRemovedEventHandler OnDelegatorClientRemoved;
        // Notifies Office apps that the IM client state (signed out, signing in, singed in, signing out, etc) has changed.
        internal void RaiseOnStateChangedEvent(ClientStateChangedEventData eventData)
        {
            if (this.OnStateChanged != null)
            {
                this.OnStateChanged(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a notification event from MAPI (e.g. autodiscover has finished)
        internal void RaiseOnNotificationReceivedEvent(LyncClientNotificationReceivedEventData eventData)
        {
            if (this.OnNotificationReceived != null)
            {
                this.OnNotificationReceived(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has received a request for credentials for some operation (e.g. sign in, web search)
        internal void RaiseOnCredentialRequestedEvent(CredentialRequestedEventData eventData)
        {
            if (this.OnCredentialRequested != null)
            {
                this.OnCredentialRequested(this, eventData);
            }
        }
        // Notifies Office apps that the IM client has been delayed from signing in and gives an estimated delay time.
        internal void RaiseOnSignInDelayedEvent(SignInDelayedEventData eventData)
        {
            if (this.OnSignInDelayed != null)
            {
                this.OnSignInDelayed(this, eventData);
            }
        }
        // Notifies Office apps that the capabilities of this IM client have changed.
        internal void RaiseOnCapabilitiesChangedEvent(PreferredCapabilitiesChangedEventData eventData)
        {
            if (this.OnCapabilitiesChanged != null)
            {
                this.OnCapabilitiesChanged(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been added to the IM client object.
        internal void RaiseOnDelegatorClientAdded(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientAdded != null)
            {
                this.OnDelegatorClientAdded(this, eventData);
            }
        }
        // Notifies Office apps that a DelegatorClient object has been removed from the IM client object.
        internal void RaiseOnDelegatorClientRemoved(DelegatorClientCollectionEventData eventData)
        {
            if (this.OnDelegatorClientRemoved != null)
            {
                this.OnDelegatorClientRemoved(this, eventData);
            }
        }
        #endregion
    }
}
```

### <a name="iautomation-interface"></a><span data-ttu-id="ef468-343">Интерфейс IAutomation</span><span class="sxs-lookup"><span data-stu-id="ef468-343">IAutomation interface</span></span>
<span data-ttu-id="ef468-344"><a name="off15_IMIntegration_ImplementRequired_IAutomation"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-344"></span></span>

<span data-ttu-id="ef468-345">Интерфейс **IAutomation** автоматизирует функции обмена мгновенными Сообщениями клиентского приложения.</span><span class="sxs-lookup"><span data-stu-id="ef468-345">The **IAutomation** interface automates features of the IM client application.</span></span> <span data-ttu-id="ef468-346">Его можно использовать для начало бесед, участвовать в конференциях и обеспечения расширяемости окно контекста.</span><span class="sxs-lookup"><span data-stu-id="ef468-346">It can be used to start conversations, join conferences, and provide extensibility window context.</span></span> 
  
<span data-ttu-id="ef468-347">В таблице 4 показаны элементы, которые должны быть реализованы в классе, который наследует от **IAutomation**.</span><span class="sxs-lookup"><span data-stu-id="ef468-347">Table 4 shows the members that must be implemented in the class that inherits from **IAutomation**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-348">Любой элемент в интерфейсе **IAutomation** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-348">Any member of the **IAutomation** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-349">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-349">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
> 
> <span data-ttu-id="ef468-350">Дополнительные сведения об интерфейсе **IAutomation** и его члены можно [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span><span class="sxs-lookup"><span data-stu-id="ef468-350">For more information about the **IAutomation** interface and its members, see [UCCollaborationLib.IAutomation](http://msdn.microsoft.com/library/UCCollaborationLib.IAutomation).</span></span> 
  
<span data-ttu-id="ef468-351">**В таблице 4. Реализация интерфейса IAutomation**</span><span class="sxs-lookup"><span data-stu-id="ef468-351">**Table 4. Implementation of IAutomation interface**</span></span>

|<span data-ttu-id="ef468-352">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-352">**Member**</span></span>|<span data-ttu-id="ef468-353">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-353">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-354">Метод **StartConversation**</span><span class="sxs-lookup"><span data-stu-id="ef468-354">**StartConversation** method</span></span>  <br/> |<span data-ttu-id="ef468-355">Запускает в беседе при помощи модальность указанного беседы.</span><span class="sxs-lookup"><span data-stu-id="ef468-355">Starts a conversation using the specified conversation modality.</span></span> <span data-ttu-id="ef468-356">Экземпляр **IConversationWindow** возвращается.</span><span class="sxs-lookup"><span data-stu-id="ef468-356">An instance of **IConversationWindow** is returned.</span></span>  <br/> |
   
## <a name="implementing-contact-presence-integration"></a><span data-ttu-id="ef468-357">Реализация интеграции контактных сведений о присутствии</span><span class="sxs-lookup"><span data-stu-id="ef468-357">Implementing contact presence integration</span></span>
<span data-ttu-id="ef468-358"><a name="off15_IMIntegration_ImplementIMFeatures"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-358"></span></span>

<span data-ttu-id="ef468-359">В дополнение к три необходимые интерфейсы, описанных ранее существует несколько интерфейсов, которые важны для включения функции контактных сведений о присутствии в Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-359">In addition to the three required interfaces discussed previously, there are several other interfaces that are important for enabling contact presence functionality in Office.</span></span> <span data-ttu-id="ef468-360">К ним относятся следующие:</span><span class="sxs-lookup"><span data-stu-id="ef468-360">These include the following:</span></span>
  
- <span data-ttu-id="ef468-361">Интерфейс [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) или **IContact2** .</span><span class="sxs-lookup"><span data-stu-id="ef468-361">The [IContact](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContact) or **IContact2** interface.</span></span> 
    
- <span data-ttu-id="ef468-362">Интерфейс [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) .</span><span class="sxs-lookup"><span data-stu-id="ef468-362">The [ISelf](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ISelf) interface.</span></span> 
    
- <span data-ttu-id="ef468-363">Интерфейсы [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) и [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) .</span><span class="sxs-lookup"><span data-stu-id="ef468-363">The [IContactManager](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) and [_IContactManagerEvents](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactManager) interfaces.</span></span> 
    
- <span data-ttu-id="ef468-364">Интерфейсы [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) и [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) .</span><span class="sxs-lookup"><span data-stu-id="ef468-364">The [IGroup](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) and [IGroupCollection](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IGroup) interfaces.</span></span> 
    
- <span data-ttu-id="ef468-365">Интерфейс [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) .</span><span class="sxs-lookup"><span data-stu-id="ef468-365">The [IContactSubscription](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactSubscription) interface.</span></span> 
    
- <span data-ttu-id="ef468-366">Интерфейс [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) .</span><span class="sxs-lookup"><span data-stu-id="ef468-366">The [IContactEndPoint](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_IContactEndPoint) interface.</span></span> 
    
- <span data-ttu-id="ef468-367">Интерфейс [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString)</span><span class="sxs-lookup"><span data-stu-id="ef468-367">The [ILocaleString](integrating-im-applications-with-office.md#off15_IMIntegration_ImplementRequired_ILocaleString) interface</span></span> 
    
### <a name="icontact-interface"></a><span data-ttu-id="ef468-368">Интерфейс IContact</span><span class="sxs-lookup"><span data-stu-id="ef468-368">IContact interface</span></span>
<span data-ttu-id="ef468-369"><a name="off15_IMIntegration_ImplementRequired_IContact"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-369"></span></span>

<span data-ttu-id="ef468-370">Интерфейс **IContact** представляет пользователь приложения клиент обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-370">The **IContact** interface represents an IM client application user.</span></span> <span data-ttu-id="ef468-371">Интерфейс предоставляет сведения о присутствии, доступные модальности, членство в группах и свойства тип контакта для пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-371">The interface exposes presence, available modalities, group membership, and contact type properties for a user.</span></span> <span data-ttu-id="ef468-372">Чтобы начать беседу с другим пользователем, необходимо предоставить экземпляр **IContact**этого пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-372">To start a conversation with another user, you must provide that user instance of **IContact**.</span></span>
  
<span data-ttu-id="ef468-373">В таблице 5 показаны элементы, которые должны быть реализованы в классе, который наследует от **IContact**.</span><span class="sxs-lookup"><span data-stu-id="ef468-373">Table 5 shows the members that must be implemented in the class that inherits from **IContact**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-374">Любой элемент в интерфейсе **IContact** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-374">Any member of the **IContact** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-375">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-375">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="ef468-376">Дополнительные сведения об интерфейсе **IContact** и его члены можно [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span><span class="sxs-lookup"><span data-stu-id="ef468-376">For more information about the **IContact** interface and its members, see [UCCollaborationLib.IContact](http://msdn.microsoft.com/library/UCCollaborationLib.IContact).</span></span> 
  
<span data-ttu-id="ef468-377">**В таблице 5. Реализация интерфейса IContact**</span><span class="sxs-lookup"><span data-stu-id="ef468-377">**Table 5. Implementation of the IContact interface**</span></span>

|<span data-ttu-id="ef468-378">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-378">**Member**</span></span>|<span data-ttu-id="ef468-379">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-379">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-380">Метод **CanStart**</span><span class="sxs-lookup"><span data-stu-id="ef468-380">**CanStart** method</span></span>  <br/> |<span data-ttu-id="ef468-381">Возвращает **значение true** , если заданного типа модальность может запускаться на контакт.</span><span class="sxs-lookup"><span data-stu-id="ef468-381">Returns **true** if a given type of modality can be started on the contact.</span></span>  <br/> |
|<span data-ttu-id="ef468-382">Метод **GetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="ef468-382">**GetContactInformation** method</span></span>  <br/> |<span data-ttu-id="ef468-383">Получает один элемент сведений о присутствии от публикации контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-383">Gets one presence item from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="ef468-384">Метод **BatchGetContactInformation**</span><span class="sxs-lookup"><span data-stu-id="ef468-384">**BatchGetContactInformation** method</span></span>  <br/> |<span data-ttu-id="ef468-385">Получает несколько элементов сведений о присутствии от публикации контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-385">Gets multiple presence items from a publishing contact.</span></span>  <br/> |
|<span data-ttu-id="ef468-386">Свойства **параметров**</span><span class="sxs-lookup"><span data-stu-id="ef468-386">**Settings** property</span></span>  <br/> |<span data-ttu-id="ef468-387">Получает коллекцию свойства контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-387">Gets a collection of contact properties.</span></span>  <br/> |
|<span data-ttu-id="ef468-388">Свойство **CustomGroups**</span><span class="sxs-lookup"><span data-stu-id="ef468-388">**CustomGroups** property</span></span>  <br/> |<span data-ttu-id="ef468-389">Получает коллекцию групп, которым принадлежит контакт.</span><span class="sxs-lookup"><span data-stu-id="ef468-389">Gets a collection of groups that the contact is a member of.</span></span>  <br/> |
   
<span data-ttu-id="ef468-390">Во время инициализации приложения Office вызывает метод **IContact.CanStart** для определения возможности обмена мгновенными Сообщениями для локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-390">During the initialization process, the Office application calls the **IContact.CanStart** method to determine the IM capabilities for the local user.</span></span> <span data-ttu-id="ef468-391">Метод **CanStart** принимает флаг из перечисления [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) в качестве аргумента для параметра_modalityTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="ef468-391">The **CanStart** method takes a flag from the [UCCollaborationLib.ModalityTypes](http://msdn.microsoft.com/library/UCCollaborationLib.ModalityTypes) enumeration as an argument for the  __modalityTypes_ parameter.</span></span> <span data-ttu-id="ef468-392">Если текущий пользователь могли взаимодействовать в запрошенные модальности (то есть, пользователь способен обмена мгновенными сообщениями, аудио- и видеоконференций обмена мгновенными сообщениями или общего доступа к приложениям), метод **CanStart** возвращает **значение true**.</span><span class="sxs-lookup"><span data-stu-id="ef468-392">If the current user can engage in the requested modality (that is, the user is capable of instant messaging, audio and video messaging, or application sharing), the **CanStart** method returns **true**.</span></span>
  
```cs
public bool CanStart(ModalityTypes _modalityTypes)
{
    // Define the capabilities of the current IM client application
    // user by using flags from the ModalityTypes enumeration.
    ModalityTypes userCapabilities = 
        ModalityTypes.ucModalityInstantMessage | 
        ModalityTypes.ucModalityAudioVideo | 
        ModalityTypes.ucModalityAppSharing;
    // Perform a simple test for equivalency.
    if (_modalityType == userCapabilities) 
    {
        return true;
    }
    else 
    {
        return false;
    }
}

```

<span data-ttu-id="ef468-393">Метод **GetContactInformation** получает сведения о контакте из объекта **IContact** .</span><span class="sxs-lookup"><span data-stu-id="ef468-393">The **GetContactInformation** method retrieves information about the contact from the **IContact** object.</span></span> <span data-ttu-id="ef468-394">Вызывающий код должен передать значение из перечисления [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) для параметра_contactInformationType_ _ указывает данные, которые нужно вернуть.</span><span class="sxs-lookup"><span data-stu-id="ef468-394">The calling code needs to pass in a value from the [UCCollaborationLib.ContactInformationType](http://msdn.microsoft.com/library/UCCollaborationLib.ContactInformationType) enumeration for the  __contactInformationType_ parameter, which indicates the data to be retrieved.</span></span> 
  
```cs
public object GetContactInformation(
    ContactInformationType _contactInformationType)
{
    // Determine the information to return from the contact's data based
    // on the value passed in for the _contactInformationType parameter.
    switch (_contactInformationType)
    {
        case ContactInformationType.ucPresenceEmailAddresses:
        {
            // Return the URI associated with the contact.
            string returnValue = this.Uri.ToLower().Replace("sip:", String.Empty);
            return returnValue;
        }
        case ContactInformationType.ucPresenceDisplayName:
        {
            // Return the display name associated with the contact.
            string returnValue = this._DisplayName;
            return returnValue;
        }
        default:
        {
            throw new NotImplementedException;
        }
        // Additional implementation details omitted.
    }
}
```

<span data-ttu-id="ef468-395">Как и **GetContactInformation**, метод **BatchGetContactInformation** получает несколько элементов сведений о присутствии о контакте из объекта **IContact** .</span><span class="sxs-lookup"><span data-stu-id="ef468-395">Similar to the **GetContactInformation**, the **BatchGetContactInformation** method retrieves multiple presence items about the contact from the **IContact** object.</span></span> <span data-ttu-id="ef468-396">Вызывающий код должен передать в массив значений из перечисления **ContactInformationType** для параметра_contactInformationTypes_ _.</span><span class="sxs-lookup"><span data-stu-id="ef468-396">The calling code needs to pass in an array of values from the **ContactInformationType** enumeration for the  __contactInformationTypes_ parameter.</span></span> <span data-ttu-id="ef468-397">Метод возвращает объект [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) , содержащий запрошенные данные.</span><span class="sxs-lookup"><span data-stu-id="ef468-397">The method returns an [UCCollaborationLib.IContactInformationDictionary](http://msdn.microsoft.com/library/UCCollaborationLib.IContactInformationDictionary) object that contains the requested data.</span></span> 
  
```cs
public IMClientContactInformationDictionary BatchGetContactInformation(
    ContactInformationType[] _contactInformationTypes)
{
    // The IMClientContactInformationDictionary class implements the
    // IContactInformationDictionary interface.
    IMClientContactInformationDictionary contactDictionary = 
        new IMClientContactInformationDictionary();
    foreach (ContactInformationType type in _contactInformationTypes)
    {
        // Call GetContactInformation for each type of contact 
        // information to retrieve. This code adds a new entry to
        // a Dictionary object exposed by the
        // ContactInformationDictionary property.
        contactDictionary.ContactInformationDictionary.Add(
            type, this.GetContactInformation(type));
    }
    return contactDictionary;
}
```

<span data-ttu-id="ef468-398">Свойство **IContact.Settings** возвращает объект **IContactSettingDictionary** , который содержит пользовательские свойства о контакте.</span><span class="sxs-lookup"><span data-stu-id="ef468-398">The **IContact.Settings** property returns an **IContactSettingDictionary** object that contains custom properties about the contact.</span></span> 
  
```cs
public IMClientContactSettingDictionary Settings
{
    get
    {
       // The IMClientContactSettingDictionary class implements
       // the IContactSettingDictionary interface.
       return new IMClientContactSettingDictionary();
    }
}
```

<span data-ttu-id="ef468-399">Свойство **IContact.CustomGroups** возвращает объект **IGroupCollection** , который включает в себя всех групп, членом которых является контактом.</span><span class="sxs-lookup"><span data-stu-id="ef468-399">The **IContact.CustomGroups** property returns an **IGroupCollection** object that includes all of the groups of which the contact is a member.</span></span> 
  
```cs
public IMClientGroupCollection CustomGroups
{
    get {
       // The IMClientGroupCollection class implements
       // the IGroupCollection interface.
        return new IMClientGroupCollection();
    }
}
```

### <a name="iself-interface"></a><span data-ttu-id="ef468-400">Интерфейс ISelf</span><span class="sxs-lookup"><span data-stu-id="ef468-400">ISelf interface</span></span>
<span data-ttu-id="ef468-401"><a name="off15_IMIntegration_ImplementRequired_ISelf"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-401"></span></span>

<span data-ttu-id="ef468-402">Во время инициализации приложения Office с помощью свойства **ILyncClient.Self** , который должен возвращать объект **ISelf** получает данные для текущего пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-402">During the initialization process, the Office application gets the data for the current user by accessing the **ILyncClient.Self** property, which must return an **ISelf** object.</span></span> <span data-ttu-id="ef468-403">Интерфейс **ISelf** представляет локального, выполнившего вход пользователя клиентского приложения обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-403">The **ISelf** interface represents the local, signed-in IM client application user.</span></span> 
  
<span data-ttu-id="ef468-404">В таблице 6 показаны элементы, которые должны быть реализованы в классе, который наследует от **ISelf**.</span><span class="sxs-lookup"><span data-stu-id="ef468-404">Table 6 shows the members that must be implemented in the class that inherits from **ISelf**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-405">Любой элемент в интерфейсе **ISelf** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-405">Any member of the **ISelf** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-406">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-406">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
  
<span data-ttu-id="ef468-407">**В таблице 6. Реализация интерфейса ISelf**</span><span class="sxs-lookup"><span data-stu-id="ef468-407">**Table 6. Implementation of the ISelf interface**</span></span>

|<span data-ttu-id="ef468-408">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-408">**Member**</span></span>|<span data-ttu-id="ef468-409">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-409">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-410">Свойство **контакта**</span><span class="sxs-lookup"><span data-stu-id="ef468-410">**Contact** property</span></span>  <br/> |<span data-ttu-id="ef468-411">Возвращает объект **IContact** , связанный с локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-411">Gets the **IContact** object associated with the local user.</span></span>  <br/> |
   
<span data-ttu-id="ef468-412">Сведения о присутствии, доступные модальности, членство в группах и свойства тип контакта для локального пользователя, предоставляемые с помощью свойства **ISelf.Contact** (который возвращает объект **IContact** ).</span><span class="sxs-lookup"><span data-stu-id="ef468-412">Presence, available modalities, group membership, and contact type properties for the local user are exposed through the **ISelf.Contact** property (which returns an **IContact** object).</span></span> <span data-ttu-id="ef468-413">Во время инициализации приложения Office обращается к свойству **ISelf.Contact** для получения ссылки на контактные данные для локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-413">During the initialization process, the Office application accesses the **ISelf.Contact** property to get a reference to the contact information for the local user.</span></span> 
  
<span data-ttu-id="ef468-414">Используйте следующий код для определения класса, наследуемого от **ISelf** интерфейс, который реализует свойства **контакта** .</span><span class="sxs-lookup"><span data-stu-id="ef468-414">Use the following code to define a class that inherits from the **ISelf** interface that implements the **Contact** property.</span></span> 
  
```cs
[ComVisible(true)]
public class IMClientSelf : ISelf
{
    // Declare a private field to store contact data for local user.
    private IMClientContact _contactData;
    // In the constructor for the ISelf object, the calling code 
    // must supply contact data.
    public IMClientSelf (IMClientContact _selfContactData)
    {
        this._contactData = _selfContactData;
    }
    // When accessed, the Contact property returns a reference
    // to the IContact object that represents the local user.
    public IMClientContact Contact
    {
        get
        {
            return this._contactData as IMClientContact;
        }
    }
    // Additional implementation details omitted.
}
```

### <a name="icontactmanager-and-icontactmanagerevents-interfaces"></a><span data-ttu-id="ef468-415">Интерфейсы IContactManager и _IContactManagerEvents</span><span class="sxs-lookup"><span data-stu-id="ef468-415">IContactManager and _IContactManagerEvents interfaces</span></span>
<span data-ttu-id="ef468-416"><a name="off15_IMIntegration_ImplementRequired_IContactManager"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-416"></span></span>

<span data-ttu-id="ef468-417">Объект **IContactManager** управляет контакты для локального пользователя, включая контактные данные локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-417">The **IContactManager** object manages the contacts for the local user, including the local user's own contact information.</span></span> <span data-ttu-id="ef468-418">Приложение Office использует объект **IContactManager** для доступа к объектам **IContact** , которые соответствуют контакты локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-418">The Office application uses an **IContactManager** object to access **IContact** objects that correspond to the local user's contacts.</span></span> 
  
<span data-ttu-id="ef468-419">В таблице 7 представлены элементы, которые должны быть реализованы в классе, который наследует от **IContactManager** и **_IContactManagerEvents**.</span><span class="sxs-lookup"><span data-stu-id="ef468-419">Table 7 shows the members that must be implemented in the class that inherits from **IContactManager** and **_IContactManagerEvents**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-420">Любой элемент в интерфейсе **IContactManager** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-420">Any member of the **IContactManager** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-421">Члены, которые являются существует, но не реализовано может вызывать **NotImplementedException** или **E\_NOTIMPL** ошибка.</span><span class="sxs-lookup"><span data-stu-id="ef468-421">Members that are present but not implemented can throw a **NotImplementedException** or **E\_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="ef468-422">Дополнительные сведения о **IContactManager** и **_IContactManagerEvents** интерфейсы и их члены можно [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) и [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span><span class="sxs-lookup"><span data-stu-id="ef468-422">For more information about the **IContactManager** and **_IContactManagerEvents** interfaces and their members, see [UCCollaborationLib.IContactManager](http://msdn.microsoft.com/library/UCCollaborationLib.IContactManager) and [UCCollaborationLib._IContactManagerEvents](http://msdn.microsoft.com/library/UCCollaborationLib._IContactManagerEvents).</span></span> 
  
<span data-ttu-id="ef468-423">**В таблице 7. Реализация интерфейсов IContactManager и _IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-423">**Table 7. Implementation of the IContactManager and _IContactManagerEvents interfaces**</span></span>

|<span data-ttu-id="ef468-424">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="ef468-424">**Interface**</span></span>|<span data-ttu-id="ef468-425">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-425">**Member**</span></span>|<span data-ttu-id="ef468-426">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-426">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef468-427">**IContactManager**</span><span class="sxs-lookup"><span data-stu-id="ef468-427">**IContactManager**</span></span> <br/> |<span data-ttu-id="ef468-428">Метод **GetContactByUri**</span><span class="sxs-lookup"><span data-stu-id="ef468-428">**GetContactByUri** method</span></span>  <br/> |<span data-ttu-id="ef468-429">Находит или создает новый экземпляр контакта с помощью контакта URI.</span><span class="sxs-lookup"><span data-stu-id="ef468-429">Finds or creates a new contact instance by using the contact URI.</span></span>  <br/> |
||<span data-ttu-id="ef468-430">Метод **CreateSubscription**</span><span class="sxs-lookup"><span data-stu-id="ef468-430">**CreateSubscription** method</span></span>  <br/> |<span data-ttu-id="ef468-431">Создает объект **ISubscription** , который может использоваться для пакетной обработки подписок или запросов.</span><span class="sxs-lookup"><span data-stu-id="ef468-431">Creates an **ISubscription** object that can be used for batching subscriptions or queries.</span></span>  <br/> |
||<span data-ttu-id="ef468-432">Метод **поиска**</span><span class="sxs-lookup"><span data-stu-id="ef468-432">**Lookup** method</span></span>  <br/> |<span data-ttu-id="ef468-433">Поиск контакта или группы рассылки.</span><span class="sxs-lookup"><span data-stu-id="ef468-433">Looks up a contact or distribution group.</span></span>  <br/> |
|<span data-ttu-id="ef468-434">**_IContactManagerEvents**</span><span class="sxs-lookup"><span data-stu-id="ef468-434">**_IContactManagerEvents**</span></span> <br/> |<span data-ttu-id="ef468-435">Событие **OnGroupAdded**</span><span class="sxs-lookup"><span data-stu-id="ef468-435">**OnGroupAdded** event</span></span>  <br/> |<span data-ttu-id="ef468-436">Возникает при добавлении группы в семейство сайтов группы.</span><span class="sxs-lookup"><span data-stu-id="ef468-436">Raised when a group is added to a group collection.</span></span> <span data-ttu-id="ef468-437">Коллекции обновленные группы можно получить из свойства **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="ef468-437">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="ef468-438">Событие **OnGroupRemoved**</span><span class="sxs-lookup"><span data-stu-id="ef468-438">**OnGroupRemoved** event</span></span>  <br/> |<span data-ttu-id="ef468-439">Возникает при удалении группы из коллекции группы.</span><span class="sxs-lookup"><span data-stu-id="ef468-439">Raised when a group is removed from a group collection.</span></span> <span data-ttu-id="ef468-440">Коллекции обновленные группы можно получить из свойства **IContactManager.Groups** .</span><span class="sxs-lookup"><span data-stu-id="ef468-440">The updated group collection can be obtained from the **IContactManager.Groups** property.</span></span>  <br/> |
||<span data-ttu-id="ef468-441">Событие **OnSearchProviderStateChanged**</span><span class="sxs-lookup"><span data-stu-id="ef468-441">**OnSearchProviderStateChanged** event</span></span>  <br/> |<span data-ttu-id="ef468-442">Возникает при изменении состояния службы поиска.</span><span class="sxs-lookup"><span data-stu-id="ef468-442">Raised when a search provider's status changes.</span></span>  <br/> |
   
<span data-ttu-id="ef468-443">Office вызывает **IContactManager.GetContactByUri** для получения сведений о присутствии контакта с помощью SIP-адрес контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-443">Office calls **IContactManager.GetContactByUri** to get a contact's presence information, by using the SIP address of the contact.</span></span> <span data-ttu-id="ef468-444">Когда контакт, настроенный для SIP-адрес в Active Directory, Office определяет этот адрес контакта и вызовы **GetContactByUri**, передав SIP-адрес контакта в для параметра_contactUri_ _.</span><span class="sxs-lookup"><span data-stu-id="ef468-444">When a contact is configured for an SIP address in the Active Directory, Office determines this address for a contact and calls **GetContactByUri**, passing the SIP address of the contact in for the  __contactUri_ parameter.</span></span> 
  
<span data-ttu-id="ef468-445">Когда Office не может определить адрес SIP контакта, он вызывает метод **IContactManager.Lookup** для поиска SIP с помощью службы обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-445">When Office cannot determine the SIP address for the contact, it calls the **IContactManager.Lookup** method to find the SIP by using the IM service.</span></span> <span data-ttu-id="ef468-446">Здесь Office передает в наиболее данных, его можно найти для контакта (например, просто адрес электронной почты контакта).</span><span class="sxs-lookup"><span data-stu-id="ef468-446">Here Office passes in the best data that it can find for the contact (for example, just the email address for the contact).</span></span> <span data-ttu-id="ef468-447">Метод **поиска** асинхронно возвращает объект **AsynchronousOperation** .</span><span class="sxs-lookup"><span data-stu-id="ef468-447">The **Lookup** method asynchronously returns an **AsynchronousOperation** object.</span></span> <span data-ttu-id="ef468-448">Когда он вызывает функцию обратного вызова, метод **поиска** должна вернуть успешное или неудачное выполнение операции в дополнение к URI контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-448">When it invokes the callback, the **Lookup** method should return the success or failure of the operation in addition to the URI of the contact.</span></span> 
  
```cs
public IMClientContact GetContactByUri(string _contactUri)
{
    // Declare a Contact variable to contain information about the contact.
    IMClientContact tempContact = null;
    // The _groupCollections field is an IGroupCollection object. Iterate 
    // over each group in collection to see if the 
    // contact is a part of the group.
    foreach (IMClientGroup group in this._groupCollections)
    {
       if (group.TryGetContact(_contactUri, out tempContact))
       {
           break;
       }
    }
    // Check to see that the URI returned a valid contact. If it
    // did not, create a new contact.
    if (tempContact == null)
    {
        tempContact = IMClientContact.BuildContact(_contactUri);
    }
    // Return the contact to the calling code.
    return tempContact;
}
```

<span data-ttu-id="ef468-449">Подписаться на изменения сведений о присутствии для отдельного контакта требуются приложения Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-449">The Office application needs to subscribe to presence changes for an individual contact.</span></span> <span data-ttu-id="ef468-450">Таким образом, когда состояние присутствия контакта изменяется, обмен мгновенными Сообщениями сервера оповещений клиентское приложение обмена мгновенными Сообщениями, тем самым предупреждения приложения Office.</span><span class="sxs-lookup"><span data-stu-id="ef468-450">Thus, when a contact's presence status changes, the IM server alerts the IM client application—thereby alerting the Office application.</span></span> <span data-ttu-id="ef468-451">Для этого приложения Office вызывает метод **IContactManager.CreateSubscription** для создания нового объекта **IContactSubscription** для этого запроса.</span><span class="sxs-lookup"><span data-stu-id="ef468-451">To do this, the Office application calls the **IContactManager.CreateSubscription** method to create a new **IContactSubscription** object for this request.</span></span> 
  
```cs
// Declare a private field to contain an IContactSubscription object.
private IMClientContactSubscription _contactSubscription;
// Return the IContactSubscription object associated 
// with the IContactManager object.
public IMClientContactSubscription CreateSubscription()
{
    return this._contactSubscription;
}
```

### <a name="igroup-and-igroupcollection-interfaces"></a><span data-ttu-id="ef468-452">Интерфейсы IGroup и IGroupCollection</span><span class="sxs-lookup"><span data-stu-id="ef468-452">IGroup and IGroupCollection interfaces</span></span>
<span data-ttu-id="ef468-453"><a name="off15_IMIntegration_ImplementRequired_IGroup"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-453"></span></span>

<span data-ttu-id="ef468-454">Объект **IGroup** представляет набор контактов с помощью дополнительных свойств для идентификации коллекции контакта по имени общую группу.</span><span class="sxs-lookup"><span data-stu-id="ef468-454">The **IGroup** object represents a collection of contacts with additional properties for identifying the contact collection by a collective group name.</span></span> <span data-ttu-id="ef468-455">Объект **IGroupCollection** представляет коллекцию объектов **IGroup** , определенные в локальных пользователей и клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-455">An **IGroupCollection** object represents a collection of **IGroup** objects defined by a local user and the IM client application.</span></span> <span data-ttu-id="ef468-456">Приложения Office с помощью объектов **IGroupCollection** и **IGroup** доступ к контакты локального пользователя.</span><span class="sxs-lookup"><span data-stu-id="ef468-456">The Office application uses the **IGroupCollection** and **IGroup** objects to access the local user's contacts.</span></span> 
  
<span data-ttu-id="ef468-457">В таблице 9 показаны элементы, которые должны быть реализованы в классы, наследующие от **IGroup** и **IGroupCollection** в следующей таблице.</span><span class="sxs-lookup"><span data-stu-id="ef468-457">Table 9 shows the members that must be implemented in the classes that inherit from **IGroup** and **IGroupCollection** in the following table.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="ef468-458">Любой элемент в интерфейсе **IGroup** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-458">Any member of the **IGroup** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-459">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-459">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span> 
>
> <span data-ttu-id="ef468-460">Дополнительные сведения о **IGroup** и **IGroupCollection** интерфейсов и их члены можно [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) и [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span><span class="sxs-lookup"><span data-stu-id="ef468-460">For more information about the **IGroup** and **IGroupCollection** interfaces and their members, see [UCCollaborationLib.IGroup](http://msdn.microsoft.com/library/UCCollaborationLib.IGroup) and [UCCollaborationLib.IGroupCollection](http://msdn.microsoft.com/library/UCCollaborationLib.IGroupCollection).</span></span> 
  
<span data-ttu-id="ef468-461">**В таблице 9. Реализация интерфейсов IGroup и IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="ef468-461">**Table 9. Implementation of the IGroup and IGroupCollection interfaces**</span></span>

|<span data-ttu-id="ef468-462">**Интерфейс**</span><span class="sxs-lookup"><span data-stu-id="ef468-462">**Interface**</span></span>|<span data-ttu-id="ef468-463">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-463">**Member**</span></span>|<span data-ttu-id="ef468-464">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-464">**Description**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="ef468-465">**IGroupCollection**</span><span class="sxs-lookup"><span data-stu-id="ef468-465">**IGroupCollection**</span></span> <br/> |<span data-ttu-id="ef468-466">Свойство **Count**</span><span class="sxs-lookup"><span data-stu-id="ef468-466">**Count** property</span></span>  <br/> |<span data-ttu-id="ef468-467">Возвращает число объектов **IGroup** в коллекции</span><span class="sxs-lookup"><span data-stu-id="ef468-467">Returns the count of **IGroup** objects in the collection</span></span>  <br/> |
||<span data-ttu-id="ef468-468">Свойство **Item**</span><span class="sxs-lookup"><span data-stu-id="ef468-468">**Item** property</span></span>  <br/> |<span data-ttu-id="ef468-469">Возвращает объект **IGroup** по указанному индексу в коллекции.</span><span class="sxs-lookup"><span data-stu-id="ef468-469">Returns the **IGroup** object at the specified index in the collection.</span></span>  <br/> |
|<span data-ttu-id="ef468-470">**IGroup**</span><span class="sxs-lookup"><span data-stu-id="ef468-470">**IGroup**</span></span> <br/> |<span data-ttu-id="ef468-471">Свойство **ID**</span><span class="sxs-lookup"><span data-stu-id="ef468-471">**Id** property</span></span>  <br/> |<span data-ttu-id="ef468-472">Возвращает идентификатор группы.</span><span class="sxs-lookup"><span data-stu-id="ef468-472">Returns the ID of the group.</span></span>  <br/> |
   
<span data-ttu-id="ef468-473">Когда приложение Office возвращает сведения для локального пользователя, он обращается к членство в группах для контакта (локального пользователя), вызвав свойство **IContact.CustomGroups** , которое возвращает объект **IGroupCollection** .</span><span class="sxs-lookup"><span data-stu-id="ef468-473">When the Office application gets the information for the local user, it accesses the group memberships of the contact (local user) by calling the **IContact.CustomGroups** property, which returns an **IGroupCollection** object.</span></span> <span data-ttu-id="ef468-474">**IGroupCollection** должен содержать массив (или **списка**) **IGroup** объектов.</span><span class="sxs-lookup"><span data-stu-id="ef468-474">The **IGroupCollection** must contain an array (or **List**) of **IGroup** objects.</span></span> <span data-ttu-id="ef468-475">Класс, производный от **IGroupCollection** должен предоставлять свойство **Count** , которое возвращает количество элементов в коллекции и метод проверки компонента индексирования **this(int)**, которое возвращает объект **IGroup** из коллекции.</span><span class="sxs-lookup"><span data-stu-id="ef468-475">The class that derives from **IGroupCollection** must expose a **Count** property, which returns the number of items in the collection, and an indexer method, **this(int)**, which returns an **IGroup** object from the collection.</span></span> 
  
### <a name="icontactsubscription-interface"></a><span data-ttu-id="ef468-476">Интерфейс IContactSubscription</span><span class="sxs-lookup"><span data-stu-id="ef468-476">IContactSubscription interface</span></span>
<span data-ttu-id="ef468-477"><a name="off15_IMIntegration_ImplementRequired_IContactSubscription"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-477"></span></span>

<span data-ttu-id="ef468-478">Интерфейс **IContactSubscription** позволяет выбирать контакты для получения сведений о присутствии обновлять сведения о и типов сведений о присутствии, которые активируют уведомление.</span><span class="sxs-lookup"><span data-stu-id="ef468-478">The **IContactSubscription** interface allows you to specify the contacts to receive presence information updates for and the types of presence information that trigger a notification.</span></span> <span data-ttu-id="ef468-479">Приложения Office используйте объект **IContactSubscription** для регистрации изменений в состояние присутствия контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-479">Office applications use an **IContactSubscription** object to register changes to contact's presence status.</span></span> 
  
<span data-ttu-id="ef468-480">В таблице 10 показаны элементы, которые должны быть реализованы в классы, наследующие от **IContactSubscription**.</span><span class="sxs-lookup"><span data-stu-id="ef468-480">Table 10 shows the members that must be implemented in the classes that inherit from **IContactSubscription**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-481">Любой элемент в интерфейсе **IContactSubscription** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-481">Any member of the **IContactSubscription** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-482">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-482">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="ef468-483">Дополнительные сведения об интерфейсе **IContactSubscription** и его члены можно [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span><span class="sxs-lookup"><span data-stu-id="ef468-483">For more information about the **IContactSubscription** interface and its members, see [UCCollaborationLib.IContactSubscription](http://msdn.microsoft.com/library/UCCollaborationLib.IContactSubscription).</span></span> 
  
<span data-ttu-id="ef468-484">**В таблице 10. Реализация интерфейса IContactSubscription**</span><span class="sxs-lookup"><span data-stu-id="ef468-484">**Table 10. Implementation of the IContactSubscription interface**</span></span>

|<span data-ttu-id="ef468-485">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-485">**Member**</span></span>|<span data-ttu-id="ef468-486">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-486">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-487">Метод **AddContact**</span><span class="sxs-lookup"><span data-stu-id="ef468-487">**AddContact** method</span></span>  <br/> |<span data-ttu-id="ef468-488">Добавляет объект подписки контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-488">Adds a contact to the subscription object.</span></span>  <br/> |
|<span data-ttu-id="ef468-489">**Подписки на** метод</span><span class="sxs-lookup"><span data-stu-id="ef468-489">**Subscribe** method</span></span>  <br/> |<span data-ttu-id="ef468-490">Эта статья поможет клиентское приложение обмена мгновенными Сообщениями для отслеживания присутствия контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-490">Helps the IM client application to monitor presence for a contact.</span></span>  <br/> |
   
<span data-ttu-id="ef468-491">Интерфейс **IContactSubscription** должен содержать ссылки на все объекты **IContact** , оно отслеживает, с помощью массив или **список**.</span><span class="sxs-lookup"><span data-stu-id="ef468-491">The **IContactSubscription** interface must contain a reference to all the **IContact** objects that it monitors, using an array or a **List**.</span></span> <span data-ttu-id="ef468-492">Метод **IContactSubscription.AddContact** добавляет объект **IContact** для для структуры данных объекта **IContactSubscription** , тем самым Добавление нового контакта для наблюдения за изменения сведений о присутствии.</span><span class="sxs-lookup"><span data-stu-id="ef468-492">The **IContactSubscription.AddContact** method adds an **IContact** object for the to the underlying data structure of the **IContactSubscription** object, thereby adding a new contact to monitor for presence changes.</span></span> 
  
```cs
// Store references to all of the IContact objects to subscribe to.
private List<IMClientContact> _subscribedContacts;
// Add a new IContact object to the collection of contacts.
public void AddContact(IMClientContact _contact)
{
    this._subscribedContacts.Add(_contact);
}
```

<span data-ttu-id="ef468-493">Метод **IContactSubscription.Subscribe** позволяет клиентского приложения обмена мгновенными Сообщениями для доступа к наблюдатели присутствия контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-493">The **IContactSubscription.Subscribe** method allows an IM client application to access presence observers for the contact.</span></span> <span data-ttu-id="ef468-494">Его можно использовать стратегию опроса для получения сведений о присутствии с сервера для контактов, которые подписана клиентское приложение обмена мгновенными Сообщениями.</span><span class="sxs-lookup"><span data-stu-id="ef468-494">It can use a polling strategy to get the presence from the server for the contacts for that the IM client application has subscribed to.</span></span> <span data-ttu-id="ef468-495">Метод **подписки на** полезно в тех случаях, когда запрашиваются сведения о присутствии для пользователя не из списка контактов пользователя (например, от большего публичная сеть).</span><span class="sxs-lookup"><span data-stu-id="ef468-495">The **Subscribe** method is helpful in situations where presence is requested for someone outside of a user's contact list (for example, from a larger public network).</span></span> 
  
### <a name="icontactendpoint-interface"></a><span data-ttu-id="ef468-496">Интерфейс IContactEndPoint</span><span class="sxs-lookup"><span data-stu-id="ef468-496">IContactEndPoint interface</span></span>
<span data-ttu-id="ef468-497"><a name="off15_IMIntegration_ImplementRequired_IContactEndPoint"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-497"></span></span>

<span data-ttu-id="ef468-498">**IContactEndPoint** представляет телефонный номер из коллекции контакта телефонных номеров.</span><span class="sxs-lookup"><span data-stu-id="ef468-498">The **IContactEndPoint** represents a telephone number from a contact's collection of telephone numbers.</span></span> 
  
<span data-ttu-id="ef468-499">В таблице 11 показаны элементы, которые должны быть реализованы в классы, наследующие от **IContactEndPoint**.</span><span class="sxs-lookup"><span data-stu-id="ef468-499">Table 11 shows the members that must be implemented in the classes that inherit from **IContactEndPoint**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-500">Любой элемент в интерфейсе **IContactEndPoint** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-500">Any member of the **IContactEndPoint** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-501">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-501">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="ef468-502">Дополнительные сведения об интерфейсе **IContactEndPoint** и его члены можно [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span><span class="sxs-lookup"><span data-stu-id="ef468-502">For more information about the **IContactEndPoint** interface and its members, see [UCCollaborationLib.IContactEndpoint](http://msdn.microsoft.com/library/UCCollaborationLib.IContactEndpoint).</span></span> 
  
<span data-ttu-id="ef468-503">**В таблице 11. Реализация интерфейса IContactEndPoint**</span><span class="sxs-lookup"><span data-stu-id="ef468-503">**Table 11. Implementation of the IContactEndPoint interface**</span></span>

|<span data-ttu-id="ef468-504">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-504">**Member**</span></span>|<span data-ttu-id="ef468-505">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-505">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-506">Свойство **DisplayName**</span><span class="sxs-lookup"><span data-stu-id="ef468-506">**DisplayName** property</span></span>  <br/> |<span data-ttu-id="ef468-507">Получает строку, отображение.</span><span class="sxs-lookup"><span data-stu-id="ef468-507">Gets the display string.</span></span>  <br/> |
|<span data-ttu-id="ef468-508">Свойство **Type**</span><span class="sxs-lookup"><span data-stu-id="ef468-508">**Type** property</span></span>  <br/> |<span data-ttu-id="ef468-509">Получает тип контакта конечной точки</span><span class="sxs-lookup"><span data-stu-id="ef468-509">Gets the contact endpoint type</span></span>  <br/> |
|<span data-ttu-id="ef468-510">Свойство **URI**</span><span class="sxs-lookup"><span data-stu-id="ef468-510">**Uri** property</span></span>  <br/> |<span data-ttu-id="ef468-511">Получает контакт URI.</span><span class="sxs-lookup"><span data-stu-id="ef468-511">Gets the contact URI.</span></span>  <br/> |
   
### <a name="ilocalestring-interface"></a><span data-ttu-id="ef468-512">Интерфейс ILocaleString</span><span class="sxs-lookup"><span data-stu-id="ef468-512">ILocaleString interface</span></span>
<span data-ttu-id="ef468-513"><a name="off15_IMIntegration_ImplementRequired_ILocaleString"> </a></span><span class="sxs-lookup"><span data-stu-id="ef468-513"></span></span>

<span data-ttu-id="ef468-514">**ILocaleString** — это структура локализованные строки, которая содержит локализованные строковые и код языка для локализации.</span><span class="sxs-lookup"><span data-stu-id="ef468-514">The **ILocaleString** is a localized string structure that contains both a localized string and the locale ID of the localization.</span></span> <span data-ttu-id="ef468-515">Интерфейс **ILocaleString** используется для форматирования строку настраиваемой состояние в карточке контакта.</span><span class="sxs-lookup"><span data-stu-id="ef468-515">The **ILocaleString** interface is used to format the custom status string on the contact card.</span></span> 
  
<span data-ttu-id="ef468-516">В таблице 12 показаны элементы, которые должны быть реализованы в классы, наследующие от **ILocaleString**.</span><span class="sxs-lookup"><span data-stu-id="ef468-516">Table 12 shows the members that must be implemented in the classes that inherit from **ILocaleString**.</span></span>
  
> [!NOTE]
> <span data-ttu-id="ef468-517">Любой элемент в интерфейсе **ILocaleString** , не указанные в таблице, должно быть установлено, но не обязательно должна быть реализована.</span><span class="sxs-lookup"><span data-stu-id="ef468-517">Any member of the **ILocaleString** interface not listed in the table must be present but does not need to be implemented.</span></span> <span data-ttu-id="ef468-518">Члены, которые являются существует, но не реализовано может вызвать ошибку **NotImplementedException** или **E_NOTIMPL** .</span><span class="sxs-lookup"><span data-stu-id="ef468-518">Members that are present but not implemented can throw a **NotImplementedException** or **E_NOTIMPL** error.</span></span>
>
> <span data-ttu-id="ef468-519">Дополнительные сведения об интерфейсе **ILocalString** и его члены можно [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span><span class="sxs-lookup"><span data-stu-id="ef468-519">For more information about the **ILocalString** interface and its members, see [UCCollaborationLib.ILocaleString](http://msdn.microsoft.com/library/UCCollaborationLib.ILocaleString).</span></span> 
  
<span data-ttu-id="ef468-520">**В таблице 12. Реализация интерфейса ILocaleString**</span><span class="sxs-lookup"><span data-stu-id="ef468-520">**Table 12. Implementation of the ILocaleString interface**</span></span>

|<span data-ttu-id="ef468-521">**Элемент**</span><span class="sxs-lookup"><span data-stu-id="ef468-521">**Member**</span></span>|<span data-ttu-id="ef468-522">**Описание**</span><span class="sxs-lookup"><span data-stu-id="ef468-522">**Description**</span></span>|
|:-----|:-----|
|<span data-ttu-id="ef468-523">Свойство **LocaleId**</span><span class="sxs-lookup"><span data-stu-id="ef468-523">**LocaleId** property</span></span>  <br/> |<span data-ttu-id="ef468-524">Получает идентификатор языка.</span><span class="sxs-lookup"><span data-stu-id="ef468-524">Gets the locale ID.</span></span>  <br/> |
|<span data-ttu-id="ef468-525">Свойство **value**</span><span class="sxs-lookup"><span data-stu-id="ef468-525">**Value** property</span></span>  <br/> |<span data-ttu-id="ef468-526">Получает строку.</span><span class="sxs-lookup"><span data-stu-id="ef468-526">Gets the string.</span></span>  <br/> |
   
## <a name="see-also"></a><span data-ttu-id="ef468-527">См. также</span><span class="sxs-lookup"><span data-stu-id="ef468-527">See also</span></span>

- <span data-ttu-id="ef468-528">Пространство имен [UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib)</span><span class="sxs-lookup"><span data-stu-id="ef468-528">[UCCollaborationLib](http://msdn.microsoft.com/library/UCCollaborationLib) namespace</span></span> 
    

