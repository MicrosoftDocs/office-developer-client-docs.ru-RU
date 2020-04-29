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
# <a name="transport-provider-sample"></a><span data-ttu-id="b27a2-103">Пример поставщика транспорта</span><span class="sxs-lookup"><span data-stu-id="b27a2-103">Transport Provider Sample</span></span>

  
  
<span data-ttu-id="b27a2-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="b27a2-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="b27a2-105">В этом примере используются файлы и каталоги для передачи и получения сообщений.</span><span class="sxs-lookup"><span data-stu-id="b27a2-105">This sample uses files and directories to transmit and receive messages.</span></span> <span data-ttu-id="b27a2-106">Он реализует и регистрирует очень простой препроцессор, который добавляет строку текста для каждого исходящего сообщения.</span><span class="sxs-lookup"><span data-stu-id="b27a2-106">It implements and registers a very simple preprocessor that appends a line of text to each outbound message.</span></span> <span data-ttu-id="b27a2-107">В этом примере показано, как разделить содержимое сообщения между форматами TNEF и Text, не зависящим от транспорта.</span><span class="sxs-lookup"><span data-stu-id="b27a2-107">The sample illustrates how to split message content between Transport Neutral Encapsulation Format (TNEF) and text.</span></span> <span data-ttu-id="b27a2-108">Кроме того, поддерживаются все параметры конфигурации (страницы свойств, мастера и программная конфигурация) и параметры сообщений.</span><span class="sxs-lookup"><span data-stu-id="b27a2-108">It also supports all configuration options (property sheets, wizards, and programmatic configuration) and message options.</span></span> <span data-ttu-id="b27a2-109">Он не поддерживает удаленные транспортные интерфейсы.</span><span class="sxs-lookup"><span data-stu-id="b27a2-109">It does not support the remote transport interfaces.</span></span> 
  
<span data-ttu-id="b27a2-110">Этот пример можно скачать из [примеров кода для API обмена сообщениями Outlook (MAPI)](https://go.microsoft.com/fwlink/?LinkId=129740).</span><span class="sxs-lookup"><span data-stu-id="b27a2-110">You can download this sample from [Outlook Messaging API (MAPI) Code Samples](https://go.microsoft.com/fwlink/?LinkId=129740).</span></span>
  
|||
|:-----|:-----|
|<span data-ttu-id="b27a2-111">Выполним</span><span class="sxs-lookup"><span data-stu-id="b27a2-111">Executable:</span></span>  <br/> |<span data-ttu-id="b27a2-112">mrxp32. dll</span><span class="sxs-lookup"><span data-stu-id="b27a2-112">mrxp32.dll</span></span>  <br/> |
|<span data-ttu-id="b27a2-113">Каталог исходного кода:</span><span class="sxs-lookup"><span data-stu-id="b27a2-113">Source code directory:</span></span>  <br/> |<span data-ttu-id="b27a2-114">самплетранспортпровидер\мрксп</span><span class="sxs-lookup"><span data-stu-id="b27a2-114">SampleTransportProvider\MRXP</span></span>  <br/> |
|<span data-ttu-id="b27a2-115">Языки</span><span class="sxs-lookup"><span data-stu-id="b27a2-115">Language:</span></span>  <br/> |<span data-ttu-id="b27a2-116">Языка</span><span class="sxs-lookup"><span data-stu-id="b27a2-116">C++</span></span>  <br/> |
|<span data-ttu-id="b27a2-117">Embedded</span><span class="sxs-lookup"><span data-stu-id="b27a2-117">Platforms:</span></span>  <br/> |<span data-ttu-id="b27a2-118">Visual Studio 2008 для компиляции для Windows Vista, Windows Server 2008, Windows XP с пакетом обновления 2 и Windows Server 2003 с пакетом обновления 1 (SP1)</span><span class="sxs-lookup"><span data-stu-id="b27a2-118">Visual Studio 2008 to compile for Windows Vista, Windows Server 2008, Windows XP SP2, and Windows Server 2003 SP1</span></span>  <br/> |
   
## <a name="supported-features"></a><span data-ttu-id="b27a2-119">Поддерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="b27a2-119">Supported Features</span></span>

<span data-ttu-id="b27a2-120">В этом примере поддерживаются следующие функции:</span><span class="sxs-lookup"><span data-stu-id="b27a2-120">This sample supports the following features:</span></span>
  
- <span data-ttu-id="b27a2-121">Основные функции, такие как отправка, получение и опрос новых сообщений.</span><span class="sxs-lookup"><span data-stu-id="b27a2-121">Basic features such as sending, receiving, and polling for new messages.</span></span>
    
- <span data-ttu-id="b27a2-122">Интерактивная и программная конфигурация.</span><span class="sxs-lookup"><span data-stu-id="b27a2-122">Interactive and programmatic configuration.</span></span>
    
- <span data-ttu-id="b27a2-123">Интерфейс **имапистатус** , за исключением параметра свойства.</span><span class="sxs-lookup"><span data-stu-id="b27a2-123">The **IMAPIStatus** interface, except for property setting.</span></span> <span data-ttu-id="b27a2-124">Дополнительные сведения см. в интерфейсе [имапистатус: IMAPIProp](imapistatusimapiprop.md) .</span><span class="sxs-lookup"><span data-stu-id="b27a2-124">For more information, see the [IMAPIStatus : IMAPIProp](imapistatusimapiprop.md) interface.</span></span> 
    
- <span data-ttu-id="b27a2-125">Безопасность потоков.</span><span class="sxs-lookup"><span data-stu-id="b27a2-125">Thread safety.</span></span>
    
- <span data-ttu-id="b27a2-126">Ведение журнала событий в текстовый файл.</span><span class="sxs-lookup"><span data-stu-id="b27a2-126">Event logging to a text file.</span></span> <span data-ttu-id="b27a2-127">Размер файла автоматически ограничен указанным.</span><span class="sxs-lookup"><span data-stu-id="b27a2-127">The file is automatically limited to a specified size.</span></span> <span data-ttu-id="b27a2-128">Все сеансы транспорта используют один и тот же файл.</span><span class="sxs-lookup"><span data-stu-id="b27a2-128">All transport sessions use the same file.</span></span>
    
## <a name="unsupported-features"></a><span data-ttu-id="b27a2-129">Неподдерживаемые функции</span><span class="sxs-lookup"><span data-stu-id="b27a2-129">Unsupported Features</span></span>

<span data-ttu-id="b27a2-130">В этом примере не поддерживается асинхронное обнаружение входящих сообщений.</span><span class="sxs-lookup"><span data-stu-id="b27a2-130">This sample does not support asynchronous detection of incoming messages.</span></span>
  
 <span data-ttu-id="b27a2-131">**Установка образца поставщика транспорта**</span><span class="sxs-lookup"><span data-stu-id="b27a2-131">**To install the Sample Transport Provider**</span></span>
  
1. <span data-ttu-id="b27a2-132">Чтобы скачать образец поставщика транспорта, ознакомьтесь со статьей [скачивание образцов Outlook MAPI](downloading-the-outlook-mapi-samples.md).</span><span class="sxs-lookup"><span data-stu-id="b27a2-132">To download the Sample Transport Provider, see [Downloading the Outlook MAPI Samples](downloading-the-outlook-mapi-samples.md).</span></span>
    
2. <span data-ttu-id="b27a2-133">Откройте папку, в которую были сохранены примеры Outlook MAPI.</span><span class="sxs-lookup"><span data-stu-id="b27a2-133">Locate the folder where you saved the Outlook MAPI samples.</span></span> <span data-ttu-id="b27a2-134">Щелкните правой кнопкой мыши папку Zip **\<аутлукмаписамплес-\> Version Number** и выберите **извлечь все**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-134">Right-click the **OutlookMAPISamples-\<version number\>** zip folder and click **Extract All**.</span></span>
    
3. <span data-ttu-id="b27a2-135">Нажмите кнопку **Обзор**, выберите расположение, в котором нужно сохранить пример, и нажмите кнопку **извлечь**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-135">Click **Browse**, select the location where you want to save the sample, and click **Extract**.</span></span>
    
4. <span data-ttu-id="b27a2-136">Запустите Visual Studio 2008.</span><span class="sxs-lookup"><span data-stu-id="b27a2-136">Run Visual Studio 2008.</span></span>
    
5. <span data-ttu-id="b27a2-137">В Visual Studio 2008 откройте меню **файл**, выберите пункт **Открыть**, а затем выберите **проект/решение**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-137">In Visual Studio 2008, click **File**, select **Open**, and then click **Project/Solution**.</span></span>
    
6. <span data-ttu-id="b27a2-138">Перейдите к папке, в которой сохранен пример, выберите **mrxp32. vcproj**, а затем нажмите кнопку **Открыть**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-138">Browse to the location where you saved the sample, click **mrxp32.vcproj**, and then click **Open**.</span></span>
    
7. <span data-ttu-id="b27a2-139">В меню **Построение** выберите пункт **Диспетчер конфигураций**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-139">On the **Build** menu, click **Configuration Manager**.</span></span>
    
8. <span data-ttu-id="b27a2-140">В диалоговом окне **Диспетчер конфигураций** перейдите к строке **mrxp32** , а затем в столбце **Конфигурация** выберите **выпуск**и нажмите кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-140">In the **Configuration Manager** dialog box, go to the **mrxp32** row, and in the **Configuration** column select **Release**, and then click **Close**.</span></span>
    
9. <span data-ttu-id="b27a2-141">On the **Build** menu, click **Build Solution**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-141">On the **Build** menu, click **Build Solution**.</span></span>
    
10. <span data-ttu-id="b27a2-142">В диалоговом окне **сохранить файл как** нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-142">In the **Save File As** dialog box, click **Save**.</span></span>
    
11. <span data-ttu-id="b27a2-143">В папке, в которой сохранен пример, щелкните правой кнопкой мыши пакетный файл установки и выберите команду **Запуск от имени администратора**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-143">In the folder where you saved the sample, right-click the installation batch file and click **Run as administrator**.</span></span>
    
12. <span data-ttu-id="b27a2-144">В диалоговом окне **Контроль учетных записей пользователей** нажмите кнопку **Продолжить**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-144">In the **User Account Control** dialog box, click **Continue**.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b27a2-145">**install. bat** копирует библиотеку DLL в папку установки Microsoft Office по умолчанию, C:\Program Files\Microsoft Office\Office12\.</span><span class="sxs-lookup"><span data-stu-id="b27a2-145">**install.bat** copies the .dll to the default Microsoft Office installation folder, C:\Program Files\Microsoft Office\Office12\.</span></span> <span data-ttu-id="b27a2-146">Если вы установили продукты Office в другом расположении, щелкните правой кнопкой мыши **install. bat** и выберите команду **изменить**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-146">If you have installed Office products in a different location, right-click **install.bat** and click **Edit**.</span></span> <span data-ttu-id="b27a2-147">Файл откроется в блокноте.</span><span class="sxs-lookup"><span data-stu-id="b27a2-147">The file opens in Notepad.</span></span> <span data-ttu-id="b27a2-148">Замените путь установки по умолчанию на путь установки, используемый на вашем компьютере.</span><span class="sxs-lookup"><span data-stu-id="b27a2-148">Replace the default installation path with the installation path used on your computer.</span></span> 
  
 <span data-ttu-id="b27a2-149">**Настройка поставщика транспорта в Outlook**</span><span class="sxs-lookup"><span data-stu-id="b27a2-149">**To set up the Transport Provider in Outlook**</span></span>
  
1. <span data-ttu-id="b27a2-150">В меню **Сервис** Outlook выберите пункт **Параметры учетной записи**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-150">On the **Tools** menu of Outlook, click **Account Settings**.</span></span>
    
2. <span data-ttu-id="b27a2-151">В диалоговом окне **Параметры учетной записи** на вкладке **Электронная почта** нажмите кнопку **создать**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-151">In the **Account Settings** dialog box, on the **Email** tab, click **New**.</span></span>
    
3. <span data-ttu-id="b27a2-152">В разделе **Выбор службы электронной почты** нажмите кнопку **другой**, выберите пункт **мрксп Sample Transport (транспорт**), а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-152">Under **Choose Email Service** click **Other**, select **MRXP Sample Transport**, and then click **Next**.</span></span>
    
4. <span data-ttu-id="b27a2-153">В диалоговом окне **Конфигурация транспорта мрксп** введите **Отображаемое имя пользователя**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-153">In the **MRXP Transport Configuration** dialog box type a **User Display Name**.</span></span>
    
5. <span data-ttu-id="b27a2-154">В разделе **путь к папке "Входящие" (UNC-общая папка)** введите путь к папке.</span><span class="sxs-lookup"><span data-stu-id="b27a2-154">Under **Path to Inbox (UNC Share)** enter a folder path.</span></span> <span data-ttu-id="b27a2-155">Это также может быть путь к локальной папке.</span><span class="sxs-lookup"><span data-stu-id="b27a2-155">This can also be a path to a local folder.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="b27a2-156">Этот путь должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b27a2-156">This path must exist.</span></span> 
  
6. <span data-ttu-id="b27a2-157">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-157">Click **OK**.</span></span>
    
7. <span data-ttu-id="b27a2-158">В диалоговом окне **Добавление учетной записи электронной почты** нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-158">In the **Add Email Account** dialog box click **OK**.</span></span> <span data-ttu-id="b27a2-159">Нажмите кнопку **Готово** , а затем кнопку **Закрыть**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-159">Click **Finish** and then click **Close**.</span></span>
    
8. <span data-ttu-id="b27a2-160">Чтобы начать работу с учетной записью МРКСП, закройте и перезапустите Outlook.</span><span class="sxs-lookup"><span data-stu-id="b27a2-160">To start using the MRXP account, exit and restart Outlook.</span></span>
    
 <span data-ttu-id="b27a2-161">**Использование образца поставщика транспорта для отправки сообщения в Outlook**</span><span class="sxs-lookup"><span data-stu-id="b27a2-161">**To use the Transport Provider Sample to send a message in Outlook**</span></span>
  
1. <span data-ttu-id="b27a2-162">В меню **файл** выберите команду **создать**, а затем — **сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-162">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b27a2-163">В поле **Кому** введите имя получателя в формате **[мрксп\<\>: адрес]**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-163">In the **To** box type the name of the recipient using the format **[MRXP:\<ADDRESS\>]**.</span></span> <span data-ttu-id="b27a2-164">Адрес — это UNC-путь к папке "Входящие" или путь к локальной папке получателя.</span><span class="sxs-lookup"><span data-stu-id="b27a2-164">The address is the UNC share or local folder path to the recipient's inbox.</span></span>
    
    > [!NOTE]
    > <span data-ttu-id="b27a2-165">Если в адресе есть двоеточия или обратные косые черты, необходимо вставить обратную косую черту перед каждым двоеточием или обратной косой чертой.</span><span class="sxs-lookup"><span data-stu-id="b27a2-165">If there are colons or backslashes in the address, you must insert a backslash before each colon or backslash.</span></span> <span data-ttu-id="b27a2-166">Например, чтобы отправить почту [МРКСП: C: \Маил\мидир], необходимо ввести `[MRXP:C\:\\Mail\\myDir]`.</span><span class="sxs-lookup"><span data-stu-id="b27a2-166">For example, to send mail to [MRXP:C:\Mail\myDir] you must type  `[MRXP:C\:\\Mail\\myDir]`.</span></span> 
  
    > [!IMPORTANT]
    > <span data-ttu-id="b27a2-167">Адрес получателя должен существовать.</span><span class="sxs-lookup"><span data-stu-id="b27a2-167">The recipient address must exist.</span></span> 
  
3. <span data-ttu-id="b27a2-168">Выберите **учетная запись** , а затем щелкните **мрксп образец транспорта**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-168">Click **Account** and then click **MRXP Sample Transport**.</span></span>
    
4. <span data-ttu-id="b27a2-169">Введите сообщение и нажмите кнопку **Отправить**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-169">Type your message and click **Send**.</span></span> <span data-ttu-id="b27a2-170">Сообщение отправляется с помощью поставщика транспорта МРКСП.</span><span class="sxs-lookup"><span data-stu-id="b27a2-170">The message is sent using the MRXP transport provider.</span></span>
    
 <span data-ttu-id="b27a2-171">**Использование образца поставщика транспорта для получения сообщения в Outlook**</span><span class="sxs-lookup"><span data-stu-id="b27a2-171">**To use the Transport Provider Sample to receive a message in Outlook**</span></span>
  
1. <span data-ttu-id="b27a2-172">В меню **файл** выберите команду **создать**, а затем — **сообщение электронной почты**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-172">On the **File** menu, click **New**, and then click **Mail Message**.</span></span>
    
2. <span data-ttu-id="b27a2-173">Введите текст сообщения.</span><span class="sxs-lookup"><span data-stu-id="b27a2-173">Type your message.</span></span>
    
3. <span data-ttu-id="b27a2-174">Нажмите кнопку **Microsoft Office**, выберите **Сохранить как**, а затем нажмите кнопку **Сохранить как** , чтобы сохранить файл в папке "Входящие", указанной во время установки.</span><span class="sxs-lookup"><span data-stu-id="b27a2-174">Click the **Microsoft Office Button**, click **Save As**, and then click **Save As** to save the file to the inbox folder you specified during setup.</span></span> 
    
4. <span data-ttu-id="b27a2-175">В диалоговом окне **Сохранить как** перейдите к общему ресурсу UNC или локальной папке, настроенным в качестве папки "Входящие".</span><span class="sxs-lookup"><span data-stu-id="b27a2-175">In the **Save As** dialog box, browse to the UNC share or local folder that you set as your inbox.</span></span> 
    
5. <span data-ttu-id="b27a2-176">В раскрывающемся списке **Тип файла** выберите **Формат сообщений Outlook**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-176">In the **Save as type** drop down, click **Outlook Message Format**.</span></span>
    
6. <span data-ttu-id="b27a2-177">Введите имя файла и нажмите кнопку **сохранить**.</span><span class="sxs-lookup"><span data-stu-id="b27a2-177">Type a name for the file and click **Save**.</span></span>
    
7. <span data-ttu-id="b27a2-178">Файл будет сохранен в общей папке.</span><span class="sxs-lookup"><span data-stu-id="b27a2-178">The file is saved to the shared folder.</span></span> <span data-ttu-id="b27a2-179">Поставщик транспорта МРКСП доставляет сообщение в папку "Входящие" в Outlook.</span><span class="sxs-lookup"><span data-stu-id="b27a2-179">The MRXP transport provider delivers the message to your Inbox in Outlook.</span></span>
    

