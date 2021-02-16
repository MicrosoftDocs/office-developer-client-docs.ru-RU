---
title: Пример поставщика транспорта
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: ec6eb6c0-bfe3-4989-9071-89a14c0e7bdd
description: 'Дата последнего изменения: 9 марта 2015 г.'
ms.openlocfilehash: def51a752abcb79a35980ed12eb73011c26d2597
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32356590"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="826b5-103">Пример поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="826b5-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="826b5-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="826b5-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="826b5-105">В этом примере для передачи и получения сообщений используются файлы и каталоги.</span><span class="sxs-lookup"><span data-stu-id="826b5-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="826b5-106">Он реализует и регистрирует очень простой препроцессор, который примесит строку текста к каждому исходячему сообщению.</span><span class="sxs-lookup"><span data-stu-id="826b5-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="826b5-107">В примере показано, как разделить содержимое сообщения между форматом TNEF и текстом.</span><span class="sxs-lookup"><span data-stu-id="826b5-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="826b5-108">Он также поддерживает все параметры конфигурации (листы свойств, мастера и программную конфигурацию) и параметры сообщений.</span><span class="sxs-lookup"><span data-stu-id="826b5-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="826b5-109">Он не поддерживает интерфейсы удаленного транспорта.</span><span class="sxs-lookup"><span data-stu-id="826b5-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="826b5-110">Вы можете скачать этот пример из примеров кода для API сообщений [Outlook (MAPI).](https://go.microsoft.com/fwlink/?LinkId=129740)</span><span class="sxs-lookup"><span data-stu-id="826b5-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="826b5-111">Исполняемый исполня</span><span class="sxs-lookup"><span data-stu-id="826b5-111">Executable:</span></span>  <br/> |<span data-ttu-id="826b5-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="826b5-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="826b5-113">Каталог с исходным кодом:</span><span class="sxs-lookup"><span data-stu-id="826b5-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="826b5-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="826b5-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="826b5-115">Язык:</span><span class="sxs-lookup"><span data-stu-id="826b5-115">Language:</span></span>  <br/> |<span data-ttu-id="826b5-116">C++</span><span class="sxs-lookup"><span data-stu-id="826b5-116">C++</span></span>  <br/> |
|<span data-ttu-id="826b5-117">Платформы:</span><span class="sxs-lookup"><span data-stu-id="826b5-117">Platforms:</span></span>  <br/> |<span data-ttu-id="826b5-118">Visual Studio 2008 для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 (SP2) и Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="826b5-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="826b5-119">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="826b5-119">Supported Features</span></span>

<span data-ttu-id="826b5-120">В этом примере поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="826b5-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="826b5-121">Основные функции, такие как отправка, получение и опрос новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="826b5-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="826b5-122">Интерактивная и программная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="826b5-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="826b5-123">Интерфейс **IMAPIStatus,** за исключением параметра свойства.</span><span class="sxs-lookup"><span data-stu-id="826b5-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="826b5-124">Дополнительные сведения см. в [интерфейсе IMAPIStatus : IMAPIProp.](imapistatusimapiprop.md)</span><span class="sxs-lookup"><span data-stu-id="826b5-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="826b5-125">Потокобезопасности.</span><span class="sxs-lookup"><span data-stu-id="826b5-125">Thread safety.</span></span>
    
- <span data-ttu-id="826b5-126">Ведение журнала событий в текстовом файле.</span><span class="sxs-lookup"><span data-stu-id="826b5-126">Event logging to a text file.</span></span> <span data-ttu-id="826b5-127">Файл автоматически ограничивается указанным размером.</span><span class="sxs-lookup"><span data-stu-id="826b5-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="826b5-128">Все сеансы транспорта используют один и тот же файл.</span><span class="sxs-lookup"><span data-stu-id="826b5-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="826b5-129">Неподтверченные функции</span><span class="sxs-lookup"><span data-stu-id="826b5-129">Unsupported Features</span></span>

<span data-ttu-id="826b5-130">Этот пример не поддерживает асинхронное обнаружение входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="826b5-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="826b5-131">**Установка примера поставщика транспорта**</span><span class="sxs-lookup"><span data-stu-id="826b5-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="826b5-132">Чтобы скачать пример поставщика транспорта, скачайте примеры [MAPI для Outlook.](downloading-the-outlook-mapi-samples.md)</span><span class="sxs-lookup"><span data-stu-id="826b5-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="826b5-133">Найдите папку, в которой сохранены примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="826b5-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="826b5-134">Щелкните правой кнопкой **мыши ZIP-папку OutlookMAPISamples версии \< \>** и выберите **"Извлечь все".**</span><span class="sxs-lookup"><span data-stu-id="826b5-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="826b5-135">Нажмите **кнопку**"Обзор", выберите расположение, в котором вы хотите сохранить пример, и нажмите кнопку **"Извлечь".**</span><span class="sxs-lookup"><span data-stu-id="826b5-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="826b5-136">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="826b5-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="826b5-137">В Visual Studio 2008 выберите **"Файл",** **"Открыть"** и **"Проект/решение".**</span><span class="sxs-lookup"><span data-stu-id="826b5-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="826b5-138">Перейдите в расположение, в котором сохранен пример, **щелкните mrxp32.vcproj** и нажмите кнопку **"Открыть".**</span><span class="sxs-lookup"><span data-stu-id="826b5-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="826b5-139">В меню **"Построение"** выберите **Configuration Manager.**</span><span class="sxs-lookup"><span data-stu-id="826b5-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="826b5-140">В **диалоговом окне Configuration Manager** перейдите к строке  **mrxp32** и в столбце "Конфигурация" выберите "Выпуск" **и** нажмите кнопку **"Закрыть".**</span><span class="sxs-lookup"><span data-stu-id="826b5-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="826b5-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="826b5-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="826b5-142">В **диалоговом окне** "Сохранить файл как" нажмите кнопку **"Сохранить".**</span><span class="sxs-lookup"><span data-stu-id="826b5-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="826b5-143">В папке, в которой сохранен пример, щелкните правой кнопкой мыши пакетный файл установки и выберите "Запуск **от прав администратора".**</span><span class="sxs-lookup"><span data-stu-id="826b5-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="826b5-144">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="826b5-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="826b5-145">**install.bat** DLL-файл копируется в папку установки Microsoft Office по умолчанию C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="826b5-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="826b5-146">Если продукты Office установлены в другом расположении, щелкните правой кнопкой мышиinstall.bat **и** выберите **"Изменить".**</span><span class="sxs-lookup"><span data-stu-id="826b5-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="826b5-147">Файл откроется в Блокноте.</span><span class="sxs-lookup"><span data-stu-id="826b5-147">The file opens in Notepad.</span></span> <span data-ttu-id="826b5-148">Замените путь установки по умолчанию на путь установки, используемый на компьютере.</span><span class="sxs-lookup"><span data-stu-id="826b5-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="826b5-149">**Настройка поставщика транспорта в Outlook**</span><span class="sxs-lookup"><span data-stu-id="826b5-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="826b5-150">В меню **"Инструменты"** Outlook щелкните **"Параметры учетной записи".**</span><span class="sxs-lookup"><span data-stu-id="826b5-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="826b5-151">В **диалоговом окне** "Параметры учетной записи" на вкладке **"Электронная** почта" нажмите кнопку **"Создать".**</span><span class="sxs-lookup"><span data-stu-id="826b5-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="826b5-152">В **области "Выбор службы электронной почты"** щелкните **"Другой",** выберите пример транспорта **MRXP** и нажмите кнопку **"Далее".**</span><span class="sxs-lookup"><span data-stu-id="826b5-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="826b5-153">В диалоговом окне "Конфигурация транспорта **MRXP"** введите **отображаемого имени пользователя.**</span><span class="sxs-lookup"><span data-stu-id="826b5-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="826b5-154">В **папке "Путь к папке "Входящие" (UNC-папка)** введите путь к папке.</span><span class="sxs-lookup"><span data-stu-id="826b5-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="826b5-155">Это также может быть путь к локальной папке.</span><span class="sxs-lookup"><span data-stu-id="826b5-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="826b5-156">Этот путь должен существовать.</span><span class="sxs-lookup"><span data-stu-id="826b5-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="826b5-157">Нажмите **ОК**.</span><span class="sxs-lookup"><span data-stu-id="826b5-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="826b5-158">В **диалоговом окне "Добавление учетной записи** электронной почты" нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="826b5-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="826b5-159">Нажмите **кнопку "Готово",** а затем **нажмите кнопку "Закрыть".**</span><span class="sxs-lookup"><span data-stu-id="826b5-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="826b5-160">Чтобы начать использовать учетную запись MRXP, выйдите из Outlook и перезапустите его.</span><span class="sxs-lookup"><span data-stu-id="826b5-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="826b5-161">**Использование примера поставщика транспорта для отправки сообщения в Outlook**</span><span class="sxs-lookup"><span data-stu-id="826b5-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="826b5-162">В меню **"Файл"** щелкните **"Новый"** и выберите пункт **"Сообщение почты".**</span><span class="sxs-lookup"><span data-stu-id="826b5-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="826b5-163">В поле **"К"** введите имя получателя в **формате [MRXP: \< ADDRESS \> ]**.</span><span class="sxs-lookup"><span data-stu-id="826b5-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="826b5-164">Адрес — это UNC-папка или путь к локальной папке в папку "Входящие" получателя.</span><span class="sxs-lookup"><span data-stu-id="826b5-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="826b5-165">Если в адресе имеются двоеточия или задние кавычка, необходимо вставить накладную перед каждой двоеточием или задней.</span><span class="sxs-lookup"><span data-stu-id="826b5-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="826b5-166">Например, чтобы отправить почту [MRXP:C:\Mail\myDir], необходимо ввести  `[MRXP:C\:\\Mail\\myDir]` .</span><span class="sxs-lookup"><span data-stu-id="826b5-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="826b5-167">Адрес получателя должен существовать.</span><span class="sxs-lookup"><span data-stu-id="826b5-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="826b5-168">Щелкните **"Учетная** запись" и выберите пример транспорта **MRXP.**</span><span class="sxs-lookup"><span data-stu-id="826b5-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="826b5-169">Введите сообщение и нажмите кнопку **"Отправить".**</span><span class="sxs-lookup"><span data-stu-id="826b5-169">Type your message and click **Send**.</span></span> <span data-ttu-id="826b5-170">Сообщение отправляется с помощью поставщика транспорта MRXP.</span><span class="sxs-lookup"><span data-stu-id="826b5-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="826b5-171">**Использование примера поставщика транспорта для получения сообщения в Outlook**</span><span class="sxs-lookup"><span data-stu-id="826b5-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="826b5-172">В меню **"Файл"** щелкните **"Новый"** и выберите пункт **"Сообщение почты".**</span><span class="sxs-lookup"><span data-stu-id="826b5-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="826b5-173">Введите сообщение.</span><span class="sxs-lookup"><span data-stu-id="826b5-173">Type your message.</span></span>
    
3. <span data-ttu-id="826b5-174">Нажмите **кнопку Microsoft Office,** нажмите кнопку "Сохранить  как", а затем нажмите кнопку "Сохранить как", чтобы сохранить файл в папку "Входящие", указанную во время установки.</span><span class="sxs-lookup"><span data-stu-id="826b5-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="826b5-175">В **диалоговом окне** "Сохранить как" перейдите к UNC-папке или локальной папке, которая настроена в качестве папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="826b5-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="826b5-176">In the **Save as type** drop down, click Outlook Message **Format**.</span><span class="sxs-lookup"><span data-stu-id="826b5-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="826b5-177">Введите имя файла и нажмите кнопку **"Сохранить".**</span><span class="sxs-lookup"><span data-stu-id="826b5-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="826b5-178">Файл сохранен в общую папку.</span><span class="sxs-lookup"><span data-stu-id="826b5-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="826b5-179">Поставщик транспорта MRXP доставляет сообщение в вашу входящие в Outlook.</span><span class="sxs-lookup"><span data-stu-id="826b5-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

