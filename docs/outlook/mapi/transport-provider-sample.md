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
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25401407"
---
# <a name="transport-provider-sample"></a><span data-ttu-id="b88cb-103">Пример поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="b88cb-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="b88cb-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b88cb-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b88cb-105">В этом примере использует каталоги и файлы для передачи и получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="b88cb-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="b88cb-106">Он реализует и регистрирует очень простым препроцессор, который добавляет строку текста для всех исходящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b88cb-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="b88cb-107">Пример схемы иллюстрирует способ разделения содержимого сообщения между транспорта Neutral Encapsulation формата TNEF и текст.</span><span class="sxs-lookup"><span data-stu-id="b88cb-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="b88cb-108">Он также поддерживает все параметры конфигурации (страницы свойств, мастеры и программной конфигурации) и параметры сообщения.</span><span class="sxs-lookup"><span data-stu-id="b88cb-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="b88cb-109">Он не поддерживает интерфейсы удаленных транспорта.</span><span class="sxs-lookup"><span data-stu-id="b88cb-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="b88cb-110">В этом примере можно загрузить из [Примеры кода Outlook системы обмена сообщениями API (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740).</span><span class="sxs-lookup"><span data-stu-id="b88cb-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b88cb-111">Исполняемый файл:</span><span class="sxs-lookup"><span data-stu-id="b88cb-111">Executable:</span></span>  <br/> |<span data-ttu-id="b88cb-112">mrxp32.dll</span><span class="sxs-lookup"><span data-stu-id="b88cb-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="b88cb-113">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="b88cb-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="b88cb-114">SampleTransportProvider\MRXP</span><span class="sxs-lookup"><span data-stu-id="b88cb-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="b88cb-115">Язык:</span><span class="sxs-lookup"><span data-stu-id="b88cb-115">Language:</span></span>  <br/> |<span data-ttu-id="b88cb-116">C++</span><span class="sxs-lookup"><span data-stu-id="b88cb-116">C++</span></span>  <br/> |
|<span data-ttu-id="b88cb-117">Платформы:</span><span class="sxs-lookup"><span data-stu-id="b88cb-117">Platforms:</span></span>  <br/> |<span data-ttu-id="b88cb-118">Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1</span><span class="sxs-lookup"><span data-stu-id="b88cb-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="b88cb-119">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="b88cb-119">Supported Features</span></span>

<span data-ttu-id="b88cb-120">В этом примере не поддерживают следующие возможности:</span><span class="sxs-lookup"><span data-stu-id="b88cb-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="b88cb-121">Основные функции, например, отправка, получение и опроса для новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="b88cb-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="b88cb-122">Интерактивные и программный конфигурации.</span><span class="sxs-lookup"><span data-stu-id="b88cb-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="b88cb-123">Интерфейс **IMAPIStatus** , за исключением параметра свойства.</span><span class="sxs-lookup"><span data-stu-id="b88cb-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="b88cb-124">Дополнительные сведения можно [IMAPIStatus: IMAPIProp](imapistatusimapiprop.md) интерфейса.</span><span class="sxs-lookup"><span data-stu-id="b88cb-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="b88cb-125">Потокобезопасность.</span><span class="sxs-lookup"><span data-stu-id="b88cb-125">Thread safety.</span></span>
    
- <span data-ttu-id="b88cb-126">Ведение журнала событий в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b88cb-126">Event logging to a text file.</span></span> <span data-ttu-id="b88cb-127">Файл автоматически ограничено до указанного размера.</span><span class="sxs-lookup"><span data-stu-id="b88cb-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="b88cb-128">Все сеансы транспорта использовать тот же файл.</span><span class="sxs-lookup"><span data-stu-id="b88cb-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="b88cb-129">Неподдерживаемые возможности</span><span class="sxs-lookup"><span data-stu-id="b88cb-129">Unsupported Features</span></span>

<span data-ttu-id="b88cb-130">В этом примере не поддерживает асинхронные обнаружения входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b88cb-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="b88cb-131">**Установка примера поставщика транспорта**</span><span class="sxs-lookup"><span data-stu-id="b88cb-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="b88cb-132">Чтобы загрузить пример поставщика транспорта, обратитесь к разделу [Загрузка примеров Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b88cb-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="b88cb-133">Найдите папку, в которой вы сохранили примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="b88cb-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="b88cb-134">Щелкните правой кнопкой мыши \*\*OutlookMAPISamples -\<номер версии\> \*\* ZIP-папку и выберите команду **Извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="b88cb-135">Нажмите кнопку **Обзор**, выберите расположение, где требуется сохранить образца и нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="b88cb-136">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b88cb-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="b88cb-137">В Visual Studio 2008 откройте меню **файл**, выберите команду **Открыть**и щелкните **Проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="b88cb-138">Перейдите к папке, в которой вы сохранили примера **mrxp32.vcproj**и нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="b88cb-139">В меню **Построение** выберите пункт **Диспетчер конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="b88cb-140">В диалоговом окне **Диспетчер конфигураций** переход на строку **mrxp32** и выберите в столбце **конфигурации** **выпуска**и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="b88cb-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="b88cb-142">В диалоговом окне **Сохранение файла** нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="b88cb-143">В папке, где был сохранен примера щелкните правой кнопкой мыши файл пакета установки и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="b88cb-144">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b88cb-145">**Install.bat** копирует DLL-файл в папке установки Microsoft Office по умолчанию C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="b88cb-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="b88cb-146">Если вы установили продукты Office в другом месте, щелкните правой кнопкой мыши **install.bat** и нажмите кнопку **Изменить**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="b88cb-147">Файл открывается в "Блокнот".</span><span class="sxs-lookup"><span data-stu-id="b88cb-147">The file opens in Notepad.</span></span> <span data-ttu-id="b88cb-148">Замените путь установки по умолчанию путь установки, используемые на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="b88cb-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="b88cb-149">**Чтобы настроить поставщика транспорта в Outlook**</span><span class="sxs-lookup"><span data-stu-id="b88cb-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="b88cb-150">В меню **Сервис** Outlook выберите **Настройка учетных записей**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="b88cb-151">В диалоговом окне **Настройка учетных записей** на вкладке **электронной почты** нажмите кнопку **Создать**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="b88cb-152">В разделе **Выбор службы электронной почты** нажмите кнопку **другие**, выберите **MRXP пример транспорта**и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="b88cb-153">В диалоговом окне **Конфигурация транспорта MRXP** введите **Отображаемое имя пользователя**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="b88cb-154">В поле **путь к папке "Входящие" (общий Сетевой ресурс)** введите путь к папке.</span><span class="sxs-lookup"><span data-stu-id="b88cb-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="b88cb-155">Это также может быть пути в локальную папку.</span><span class="sxs-lookup"><span data-stu-id="b88cb-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="b88cb-156">Этот путь должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b88cb-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="b88cb-157">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="b88cb-158">В диалоговом окне **Добавление учетной записи электронной почты** нажмите **кнопку ОК**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="b88cb-159">Нажмите кнопку **Готово** , а затем нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="b88cb-160">Чтобы начать работу с использованием учетной записи MRXP, закройте и перезапустите Outlook.</span><span class="sxs-lookup"><span data-stu-id="b88cb-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="b88cb-161">**Чтобы отправить сообщение в Outlook при использовании примера поставщика транспорта**</span><span class="sxs-lookup"><span data-stu-id="b88cb-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="b88cb-162">В меню **файл** выберите **Создать**и нажмите кнопку **Сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b88cb-163">В **поле** введите имя получателя, в формате **[MRXP:\<адрес\>]**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="b88cb-164">Адрес — это общий Сетевой ресурс или локальный путь к папке "Входящие" получателя.</span><span class="sxs-lookup"><span data-stu-id="b88cb-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b88cb-165">В случае с запятыми или обратной косой черты в поле адрес, необходимо вставить обратную косую черту перед каждого двоеточие или обратная косая черта.</span><span class="sxs-lookup"><span data-stu-id="b88cb-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="b88cb-166">Например, для отправки почты в [MRXP:C:\Mail\myDir] необходимо будет ввести `[MRXP:C\:\\Mail\\myDir]`.</span><span class="sxs-lookup"><span data-stu-id="b88cb-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="b88cb-167">Должны существовать в адресе получателя.</span><span class="sxs-lookup"><span data-stu-id="b88cb-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="b88cb-168">Выберите **учетную запись** и нажмите кнопку **MRXP пример транспорта**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="b88cb-169">Введите сообщение и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-169">Type your message and click **Send**.</span></span> <span data-ttu-id="b88cb-170">Сообщение отправлено с использованием поставщика транспорта MRXP.</span><span class="sxs-lookup"><span data-stu-id="b88cb-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="b88cb-171">**Использование примера поставщика транспорта для получения сообщений в Outlook**</span><span class="sxs-lookup"><span data-stu-id="b88cb-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="b88cb-172">В меню **файл** выберите **Создать**и нажмите кнопку **Сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b88cb-173">Введите сообщение.</span><span class="sxs-lookup"><span data-stu-id="b88cb-173">Type your message.</span></span>
    
3. <span data-ttu-id="b88cb-174">Нажмите **Кнопку Microsoft Office**, выберите команду **Сохранить как**и нажмите кнопку **Сохранить как** для сохранения файла в папке "Входящие", которые были заданы во время установки.</span><span class="sxs-lookup"><span data-stu-id="b88cb-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="b88cb-175">В диалоговом окне **Сохранить как** перейдите к общий Сетевой ресурс или локальную папку, который необходимо задать в качестве папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="b88cb-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="b88cb-176">В раскрывающемся списке **Тип файла** нажмите кнопку **Формат сообщения Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="b88cb-177">Введите имя для файла и нажмите кнопку **Сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b88cb-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="b88cb-178">Файл сохраняется в общую папку.</span><span class="sxs-lookup"><span data-stu-id="b88cb-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="b88cb-179">Поставщика транспорта MRXP доставляет сообщение в папку "Входящие" в Outlook.</span><span class="sxs-lookup"><span data-stu-id="b88cb-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

