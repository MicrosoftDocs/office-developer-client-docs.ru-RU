---
title: Настройка параметров безопасности для шаблонов форм с кодом
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- пакет [infopath 2007], URL-адреса [InfoPath 2007], назначение FullTrust, управление доступом для кода [InfoPath 2007], UNC-пути [InfoPath 2007], назначение FullTrust, сервер клиентского доступа [InfoPath 2007], безопасность [InfoPath 2007], настройки, группы кода [развертывания политики безопасности Назначение для UNC-пути, FullTrust [InfoPath 2007], назначение для URL-адреса FullTrust InfoPath 2007], [InfoPath 2007]
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Вы можете настроить набор разрешений, применяемый к шаблон формы InfoPath управляемого кода с помощью настройки .NET.
ms.openlocfilehash: f04ce71875eac7695d2900131ca7c9cd333fa90f
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807505"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="43cf1-104">Настройка параметров безопасности для шаблонов форм с кодом</span><span class="sxs-lookup"><span data-stu-id="43cf1-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="43cf1-105">Вы можете настроить набор разрешений, применяемый к шаблон формы InfoPath управляемого кода с помощью настройки .NET.</span><span class="sxs-lookup"><span data-stu-id="43cf1-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="43cf1-106">Среда (CLR) размещенного в InfoPath будет искать группу предварительно заданных кода с именем *Шаблонов форм InfoPath* на уровне политики компьютера в группе весь код.</span><span class="sxs-lookup"><span data-stu-id="43cf1-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="43cf1-107">Среда CLR будет применяться наборов разрешений, которые определены в разделе группы для домена приложения (AppDomain), где выполняется код формы.</span><span class="sxs-lookup"><span data-stu-id="43cf1-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="43cf1-108">Это позволяет настраивать наборов разрешений, которые предоставляются для шаблонов форм InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="43cf1-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="43cf1-109">Например, можно предоставить шаблона формы, загруженные с http://MySite разрешение на доступ к службе каталогов Active Directory.</span><span class="sxs-lookup"><span data-stu-id="43cf1-109">For example, you can grant a form template downloaded from http://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="43cf1-110">Для применения пользовательской политики безопасности, определенной с помощью оснастки "Конфигурация .NET", необходимо развернуть эту политику на всех клиентских компьютерах, на которых будет запускаться шаблон формы.</span><span class="sxs-lookup"><span data-stu-id="43cf1-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="43cf1-111">Дополнительные сведения о модели безопасности для InfoPath с управляемым кодом шаблонов форм, см [О модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="43cf1-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="43cf1-112">Создание группы кода для шаблонов форм InfoPath</span><span class="sxs-lookup"><span data-stu-id="43cf1-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="43cf1-113">Следующая процедура создаст группу кода, что предоставляет нет разрешений на InfoPath управляемого кода шаблонов форм (за исключением тех, которые были установлены или зарегистрирован на локальном компьютере) которого можно назначить наборы разрешений, чтобы находится шаблонов форм InfoPath в определенных URL-адреса или UNC-пути.</span><span class="sxs-lookup"><span data-stu-id="43cf1-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="43cf1-114">Сведения о том, как для создания и назначения разрешений наборах для группы кода в `InfoPath Form Templates` группы кода, выполните следующую процедуру.</span><span class="sxs-lookup"><span data-stu-id="43cf1-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="43cf1-115">В отличие от средства **Конфигурация Microsoft .NET Framework 1.1** , устанавливаемого с распространяемый пакет Microsoft .NET Framework 1.1, **Конфигурация Microsoft .NET Framework 2.0** устанавливается только с помощью Microsoft .NET Framework 2.0 пакет средств разработки (SDK).</span><span class="sxs-lookup"><span data-stu-id="43cf1-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="43cf1-116">Создание пользовательской группы кода безопасности для форм InfoPath с управляемым кодом</span><span class="sxs-lookup"><span data-stu-id="43cf1-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="43cf1-117">Из меню **Пуск** выберите пункт **Администрирование**и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="43cf1-118">Если у вас **Средств администрирования** в меню **Пуск** , с помощью **Панели управления** откройте **Администрирование**и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="43cf1-119">В разделе **Мой компьютер**разверните узел **Политика безопасности во время выполнения** , **компьютер** , узел **Группы кода** , узел **All_Code** и затем щелкните правой кнопкой мыши узел **All_Code** и нажмите кнопку **Создать** , чтобы открыть **Создать Группы кода** диалоговое окно.</span><span class="sxs-lookup"><span data-stu-id="43cf1-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="43cf1-120">Назовите новую группу кода `InfoPath Form Templates` (этот текст нужно ввести точно), а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="43cf1-121">Задать тип условия для группы кода **Весь**код и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="43cf1-122">Щелкните **использовать существующий набор разрешений**, назначьте набор разрешений **Nothing** для этой группы кода, нажмите кнопку **Далее**и нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="43cf1-123">Чтобы применить новые параметры, закройте и перезапустите InfoPath.</span><span class="sxs-lookup"><span data-stu-id="43cf1-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="43cf1-124">При необходимости можно управлять набор разрешений для всех шаблонов форм InfoPath с управляемым кодом, назначив набор разрешений, отличный от набор разрешений **Nothing в группу кода **Шаблонов форм InfoPath** ** .</span><span class="sxs-lookup"><span data-stu-id="43cf1-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="43cf1-125">Вы можете изменить набор разрешений для группы кода безопасности в любое время, щелкнув правой кнопкой мыши группу в.</span><span class="sxs-lookup"><span data-stu-id="43cf1-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="43cf1-126">**NET конфигурации 2.0** оснастку, выберите пункт **Свойства**, а затем выбрав вкладку **Набор разрешений** .</span><span class="sxs-lookup"><span data-stu-id="43cf1-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="43cf1-127">Назначение разрешения "FullTrust" для форм, расположенных по указанному URL-адресу или UNC-пути</span><span class="sxs-lookup"><span data-stu-id="43cf1-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="43cf1-128">Можно создавать группы кода в группе **Шаблонов форм InfoPath** , чтобы предоставить разрешение полного доверия, задайте для шаблонов форм из определенного URL-адрес или UNC-пути.</span><span class="sxs-lookup"><span data-stu-id="43cf1-128">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location.</span></span> <span data-ttu-id="43cf1-129">После этого будет запускаться полностью доверенной каждый шаблон формы, опубликованной в указанном расположении.</span><span class="sxs-lookup"><span data-stu-id="43cf1-129">After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="43cf1-130">Шаблон формы, загруженными из локального компьютера (группа кода My Computer Zone) загружается по InfoPath в случайном порядке URL-адресу.</span><span class="sxs-lookup"><span data-stu-id="43cf1-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="43cf1-131">По этой причине нельзя использовать следующую процедуру, чтобы предоставить набор разрешений FullTrust для шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="43cf1-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="43cf1-132">Предоставление разрешений FullTrust шаблона формы, установленных локально значение, используйте одну из процедур, описанных в разделе «Развертывание формы шаблонов, который требуется полное доверие» в разделе [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="43cf1-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="43cf1-133">Назначение набора разрешений "FullTrust" для форм InfoPath, расположенных по указанному URL-адресу или UNC-пути</span><span class="sxs-lookup"><span data-stu-id="43cf1-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="43cf1-134">Из меню **Пуск** выберите пункт **Администрирование**и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="43cf1-135">Если у вас **Средств администрирования** в меню **Пуск** , с помощью **Панели управления** откройте **Администрирование**и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="43cf1-136">В разделе **Мой компьютер**разверните узел **Политика безопасности во время выполнения** , **компьютер** , узел **Группы кода** , узел **All_Code** и затем щелкните узел **Шаблоны форм InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="43cf1-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="43cf1-137">В списке **задач** на правой панели нажмите кнопку **Добавить дочернюю группу кода**, имя группы кода и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="43cf1-138">В списке **выберите тип условия для этой группы кода** выберите **URL-адрес**и введите URL-адрес или UNC-расположение шаблонов форм InfoPath с управляемым кодом, которые вы хотите предоставить набор разрешений **FullTrust** .</span><span class="sxs-lookup"><span data-stu-id="43cf1-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="43cf1-p106">Чтобы ограничить набор разрешений одним шаблоном формы, укажите полный путь к этому шаблону формы. Например:</span><span class="sxs-lookup"><span data-stu-id="43cf1-p106">To restrict the permission set to a single form template, specify the full path of that particular form template. For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `http://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="43cf1-p107">Чтобы предоставить набор разрешений для всех шаблонов форм в рамках URL-адреса или UNC-пути, не указывайте имя шаблона и добавьте звездочку в конце URL-адреса или UNC-пути. Например:</span><span class="sxs-lookup"><span data-stu-id="43cf1-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `http://MySite/MySubsite/*`
    
5. <span data-ttu-id="43cf1-143">Нажмите кнопку **Далее**, а затем щелкните **использовать существующий набор разрешений** и назначьте набор разрешений **FullTrust** для группы кода.</span><span class="sxs-lookup"><span data-stu-id="43cf1-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="43cf1-144">Нажмите кнопку **Далее**и затем нажмите кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="43cf1-145">Чтобы применить новые параметры, закройте и перезапустите InfoPath.</span><span class="sxs-lookup"><span data-stu-id="43cf1-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="43cf1-146">Чтобы применить более ограниченный или пользовательский набор разрешений, выберите соответствующий вариант вместо **FullTrust** на шаге 4.</span><span class="sxs-lookup"><span data-stu-id="43cf1-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="43cf1-147">Создание пакета развертывания для политики безопасности InfoPath</span><span class="sxs-lookup"><span data-stu-id="43cf1-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="43cf1-148">После определения настраиваемой политики безопасности для шаблонов управляемого форм InfoPath, можно создать пакет установщика Windows (MSI-файл) для развертывания этой политики безопасности на компьютерах пользователей с помощью групповой политики или Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="43cf1-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="43cf1-149">Создание пакета развертывания для пользовательской политики безопасности InfoPath</span><span class="sxs-lookup"><span data-stu-id="43cf1-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="43cf1-150">Из меню **Пуск** выберите пункт **Администрирование**и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="43cf1-151">Если у вас **Средств администрирования** в меню **Пуск** , с помощью **Панели управления** откройте **Администрирование**и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="43cf1-152">Щелкните правой кнопкой мыши **Политика безопасности во время выполнения**и нажмите кнопку **Создать пакет развертывания**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="43cf1-153">В разделе **выберите уровень политики безопасности для развертывания**щелкните **компьютер**, укажите папку и имя файла для пакета установщика Windows и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="43cf1-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="43cf1-154">Нажмите кнопку **Готово** , чтобы создать пакет развертывания.</span><span class="sxs-lookup"><span data-stu-id="43cf1-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="43cf1-155">Для получения сведений об использовании средства настройки поиска справки Visual Studio или веб-сайта MSDN для «Инструмента настройки .NET Framework (Mscorcfg.msc)».</span><span class="sxs-lookup"><span data-stu-id="43cf1-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN Web site for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="43cf1-156">См. также</span><span class="sxs-lookup"><span data-stu-id="43cf1-156">See also</span></span>



[<span data-ttu-id="43cf1-157">Модель безопасности для шаблонов форм с кодом</span><span class="sxs-lookup"><span data-stu-id="43cf1-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

