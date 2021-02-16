---
title: Установка примеров, используемых в этом разделе
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
api_type:
- COM
ms.assetid: 810f54bf-5b78-46b8-a617-4f61ff816400
description: 'Дата последнего изменения: 23 июля 2011 г.'
ms.openlocfilehash: 288ece7a26fb89fa240339da681f163909124823
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32345551"
---
# <a name="install-the-samples-used-in-this-section"></a><span data-ttu-id="69505-103">Установка примеров, используемых в этом разделе</span><span class="sxs-lookup"><span data-stu-id="69505-103">Install the samples used in this section</span></span>

<span data-ttu-id="69505-104">**Относится к**: Outlook 2013 | Outlook 2016</span><span class="sxs-lookup"><span data-stu-id="69505-104">**Applies to**: Outlook 2013 | Outlook 2016</span></span> 
  
<span data-ttu-id="69505-105">Чтобы установить приложение MFCMAPI и проект CreateOutlookItemsAddin для просмотра и запуска примера кода, на который ссылается раздел в разделе "Создание элементов Outlook с помощью [MAPI",](creating-outlook-items-by-using-mapi.md) выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69505-105">To install the MFCMAPI application and CreateOutlookItemsAddin project to view and run the sample code referenced by the topics in the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section, follow these steps.</span></span> 

<span data-ttu-id="69505-106">Чтобы скачать и установить примеры, используемые в разделе "Использование MAPI для создания элементов Outlook", выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="69505-106">To download and install the examples used in the "Using MAPI to create Outlook items" section, follow these steps.</span></span>

### <a name="to-download-and-install-the-mfcmapi-application-and-open-createoutlookitemsaddin-project"></a><span data-ttu-id="69505-107">Загрузка и установка приложения MFCMAPI и открытие проекта CreateOutlookItemsAddin</span><span class="sxs-lookup"><span data-stu-id="69505-107">To download and install the MFCMAPI application and open CreateOutlookItemsAddin project</span></span>

1. <span data-ttu-id="69505-108">Скачайте текущую версию [исполняемого MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) в папку в системе.</span><span class="sxs-lookup"><span data-stu-id="69505-108">Download the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) executable to a folder on your system.</span></span> 
    
2. <span data-ttu-id="69505-109">Извлекать MFCMapi.exe в MFCMapi.exe.</span><span class="sxs-lookup"><span data-stu-id="69505-109">Extract the MFCMapi.exe file in MFCMapi.exe.</span></span> <span data-ttu-id="69505-110">_zip_ версии в пустую папку на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="69505-110">_version_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="69505-111">Скачайте текущую версию проекта [CreateOutlookItemsAddin.](https://go.microsoft.com/fwlink/?LinkID=127828)</span><span class="sxs-lookup"><span data-stu-id="69505-111">Download the current version of the [CreateOutlookItemsAddin](https://go.microsoft.com/fwlink/?LinkID=127828) project.</span></span> 
    
4. <span data-ttu-id="69505-112">Извлекаете все файлы из CreateOutlookItemsAddin.zip в папку, в которой вы извлекли MFCMapi.exe на шаге 2.</span><span class="sxs-lookup"><span data-stu-id="69505-112">Extract all the files in the CreateOutlookItemsAddin.zip file to the folder where you extracted the MFCMapi.exe file in Step 2.</span></span>
    
5. <span data-ttu-id="69505-113">Скопируйте MFCMapi.exe из папки, используемой на шаге 2, в каталог сборки для проекта CreateOutlookItemsAddin (\CreateOutlookItemsAddin\Debug).</span><span class="sxs-lookup"><span data-stu-id="69505-113">Copy MFCMapi.exe from the folder used in Step 2 to the build directory for the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\Debug).</span></span>
    
6. <span data-ttu-id="69505-114">Откройте проект CreateOutlookItemsAddin (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) в Visual Studio, чтобы изучить исходный код.</span><span class="sxs-lookup"><span data-stu-id="69505-114">Open the CreateOutlookItemsAddin project (\CreateOutlookItemsAddin\CreateOutlookItemsAddin.vcproj) in Visual Studio to examine the source code.</span></span> <span data-ttu-id="69505-115">Чтобы определить, какие исходные файлы необходимо открыть, обратитесь к темам раздела "Создание элементов Outlook с помощью [MAPI".](creating-outlook-items-by-using-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="69505-115">Refer to the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section to determine which source files to open.</span></span> 
    
## <a name="run-mfcmapi-and-the-createoutlookitemsaddin-project"></a><span data-ttu-id="69505-116">Запуск MFCMAPI и проекта CreateOutlookItemsAddin</span><span class="sxs-lookup"><span data-stu-id="69505-116">Run MFCMAPI and the CreateOutlookItemsAddin project</span></span>

<span data-ttu-id="69505-117">В следующих шагах предполагается, что вы загрузили и установили текущую версию исполняемого MFCMAPI и проекта CreateOutlookItemsAddin, как описано в предыдущей процедуре.</span><span class="sxs-lookup"><span data-stu-id="69505-117">The following steps assume that you have downloaded and installed the current version of the MFCMAPI executable and the CreateOutlookItemsAddin project as described in the preceding procedure.</span></span> <span data-ttu-id="69505-118">Эти действия позволят вам пунктов меню **Addins,** которые позволяют создавать элементы Outlook с помощью приложения MFCMAPI и проекта CreateOutlookItemsAddin.</span><span class="sxs-lookup"><span data-stu-id="69505-118">These steps will guide you to the **Addins** menu items that enable you to create Outlook items using the MFCMAPI application and the CreateOutlookItemsAddin project.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="69505-119">Папка, выбранная на шаге 8, и команда, выбранная на шаге 9, зависит от типа элемента, рассмотренного в одном из разделов раздела "Создание элементов Outlook с помощью [MAPI".](creating-outlook-items-by-using-mapi.md)</span><span class="sxs-lookup"><span data-stu-id="69505-119">The folder you select in step 8, and the command you select in step 9, depends on the item type discussed in one of the topics from the [Creating Outlook Items by Using MAPI](creating-outlook-items-by-using-mapi.md) section.</span></span> 

### <a name="to-run-the-mfcmapi-application-and-addins-menu-commands"></a><span data-ttu-id="69505-120">Запуск команд приложения MFCMAPI и меню addins</span><span class="sxs-lookup"><span data-stu-id="69505-120">To run the MFCMAPI application and Addins menu commands</span></span>

1. <span data-ttu-id="69505-121">Запустите Mfcmapi.exe папку CreateOutlookItemsAddin\Debug, которая создается при соответствии с инструкциями по установке.</span><span class="sxs-lookup"><span data-stu-id="69505-121">Start Mfcmapi.exe in the CreateOutlookItemsAddin\Debug folder that is created when you follow the installation instructions.</span></span>
    
2. <span data-ttu-id="69505-122">Нажмите **кнопку "ОК",** чтобы отклонять экран-заставку MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="69505-122">Click **OK** to dismiss the MFCMAPI splash screen.</span></span> 
    
3. <span data-ttu-id="69505-123">В меню **"Сеанс"** щелкните **"Логон" и "Таблица магазина отображения".**</span><span class="sxs-lookup"><span data-stu-id="69505-123">On the **Session** menu, click **Logon and Display Store Table**.</span></span>
    
4. <span data-ttu-id="69505-124">В **диалоговом** окне "Выбор профиля" выберите правильный профиль и нажмите кнопку **"ОК".**</span><span class="sxs-lookup"><span data-stu-id="69505-124">In the **Choose Profile** dialog box, select the correct profile, and then click **OK**.</span></span> 
    
5. <span data-ttu-id="69505-125">Дважды **щелкните "Почтовый ящик - _[Имя пользователя] в_** представлении списка таблицы магазина".</span><span class="sxs-lookup"><span data-stu-id="69505-125">Double-click **Mailbox -  _[User Name]_** in the store table list view.</span></span> 
    
6. <span data-ttu-id="69505-126">В представлении дерева папок разоберем корневой узел.</span><span class="sxs-lookup"><span data-stu-id="69505-126">In the folder tree view, expand the root node.</span></span> <span data-ttu-id="69505-127">Имя корневого узла зависит от выбранного типа профиля.</span><span class="sxs-lookup"><span data-stu-id="69505-127">The name displayed for the root node varies depending on the type of profile selected.</span></span> <span data-ttu-id="69505-128">Обычно этот узел отображается в качестве **корневого почтового ящика.**</span><span class="sxs-lookup"><span data-stu-id="69505-128">Typically this node is displayed as **Root - Mailbox**.</span></span>
    
7. <span data-ttu-id="69505-129">В представлении дерева папок разоберем узел, содержащий хранилище данных.</span><span class="sxs-lookup"><span data-stu-id="69505-129">In the folder tree view, expand the node that contains the information store.</span></span> <span data-ttu-id="69505-130">Имя, отображаемая для этого узла, зависит от выбранного типа профиля.</span><span class="sxs-lookup"><span data-stu-id="69505-130">The name displayed for this node varies depending on the type of profile selected.</span></span> <span data-ttu-id="69505-131">Обычно этот узел отображается в IPM_SUBTREE **или** **в верхней части информационного магазина.**</span><span class="sxs-lookup"><span data-stu-id="69505-131">Typically this node is displayed as **IPM_SUBTREE** or **Top of Information Store**.</span></span>
    
8. <span data-ttu-id="69505-132">Дважды щелкните папку для создаваемого типа элемента.</span><span class="sxs-lookup"><span data-stu-id="69505-132">Double-click the folder for the item type to create.</span></span> <span data-ttu-id="69505-133">Например, чтобы создать встречу,  щелкните папку "Встречи".</span><span class="sxs-lookup"><span data-stu-id="69505-133">For example, to create an appointment, click the **Appointments** folder.</span></span> 
    
9. <span data-ttu-id="69505-134">В меню **"Надстройки"** щелкните соответствующую команду для создаемой позиции.</span><span class="sxs-lookup"><span data-stu-id="69505-134">On the **Addins** menu, click the appropriate command for the item to create.</span></span> 
    
## <a name="download-and-view-code-from-the-mfcmapi-application"></a><span data-ttu-id="69505-135">Загрузка и просмотр кода из приложения MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69505-135">Download and view code from the MFCMAPI application</span></span>

<span data-ttu-id="69505-136">Некоторые разделы относятся к коду из самого приложения MFCMAPI.</span><span class="sxs-lookup"><span data-stu-id="69505-136">Some topics refer to source code from the MFCMAPI application itself.</span></span> <span data-ttu-id="69505-137">Ниже описано, как скачать исходный код MFCMAPI и просмотреть его в Visual Studio.</span><span class="sxs-lookup"><span data-stu-id="69505-137">The following steps describe how to download the MFCMAPI source code and view it in Visual Studio.</span></span> 

### <a name="to-download-and-view-the-mfcmapi-application-source-code"></a><span data-ttu-id="69505-138">Скачать и просмотреть исходный код приложения MFCMAPI</span><span class="sxs-lookup"><span data-stu-id="69505-138">To download and view the MFCMAPI application source code</span></span>

1. <span data-ttu-id="69505-139">Загрузите исходный код для текущей версии [приложения MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) в папку в системе.</span><span class="sxs-lookup"><span data-stu-id="69505-139">Download the source code for the current version of the [MFCMAPI](https://go.microsoft.com/fwlink/?LinkID=124154) application to a folder on your system.</span></span> 
    
2. <span data-ttu-id="69505-140">Извлеките файлы в _zip-файле_ MFCMAPI в пустую папку на жестком диске.</span><span class="sxs-lookup"><span data-stu-id="69505-140">Extract the files in MFCMAPI- _changeset_.zip to an empty folder on your hard drive.</span></span>
    
3. <span data-ttu-id="69505-141">Откройте проект MFCMapi (\ _foldername_\ MFCMapi.vcproj) в Visual Studio, чтобы изучить исходный код.</span><span class="sxs-lookup"><span data-stu-id="69505-141">Open the MFCMapi project (\ _foldername_\ MFCMapi.vcproj) in Visual Studio to examine the source code.</span></span>
    
## <a name="see-also"></a><span data-ttu-id="69505-142">См. также</span><span class="sxs-lookup"><span data-stu-id="69505-142">See also</span></span>

- [<span data-ttu-id="69505-143">Создание простого почтового элемента</span><span class="sxs-lookup"><span data-stu-id="69505-143">Create a Simple Mail Item</span></span>](how-to-create-a-simple-mail-item.md)
- [<span data-ttu-id="69505-144">Создание простого элемента повторяющейся задачи</span><span class="sxs-lookup"><span data-stu-id="69505-144">Create a Simple Recurrent Task Item</span></span>](how-to-create-a-simple-recurrent-task-item.md)
- [<span data-ttu-id="69505-145">Создание сложного элемента повторяющейся встречи</span><span class="sxs-lookup"><span data-stu-id="69505-145">Create a Complex Recurrent Appointment Item</span></span>](how-to-create-a-complex-recurrent-appointment-item.md)
- [<span data-ttu-id="69505-146">Чтение и разбиение шаблона повторения</span><span class="sxs-lookup"><span data-stu-id="69505-146">Read and Parse a Recurrence Pattern</span></span>](how-to-read-and-parse-a-recurrence-pattern.md)

