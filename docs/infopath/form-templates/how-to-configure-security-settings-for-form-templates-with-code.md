---
title: Настройка параметров безопасности для шаблонов форм с кодом
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- пакет развертывания политики безопасности [InfoPath 2007], URL-адреса [InfoPath 2007], назначение FullTrust, безопасность доступа к коду [InfoPath 2007], UNC [InfoPath 2007], назначение FullTrust, CAS [InfoPath 2007], безопасность [InfoPath 2007], Настройка, группы кода [ InfoPath 2007], FullTrust [InfoPath 2007], назначение UNC, FullTrust [InfoPath 2007], назначение URL-адресов
localization_priority: Normal
ms.assetid: 24d1a322-581f-497e-b97b-bd02c4516551
description: Набор разрешений, применяемый к шаблону формы InfoPath с управляемым кодом, можно настроить с помощью оснастки "Конфигурация .NET".
ms.openlocfilehash: 77f3546d976bb5ea353aa3fbe58ba7af6cd92a6d
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32300164"
---
# <a name="configure-security-settings-for-form-templates-with-code"></a><span data-ttu-id="24ab5-104">Настройка параметров безопасности для шаблонов форм с кодом</span><span class="sxs-lookup"><span data-stu-id="24ab5-104">Configure Security Settings for Form Templates with Code</span></span>

<span data-ttu-id="24ab5-105">Набор разрешений, применяемый к шаблону формы InfoPath с управляемым кодом, можно настроить с помощью оснастки "Конфигурация .NET".</span><span class="sxs-lookup"><span data-stu-id="24ab5-105">You can customize the permission set that is applied to an InfoPath managed code form template by using the .NET Configuration snap-in.</span></span>
  
<span data-ttu-id="24ab5-106">Общеязыковая среда выполнения (CLR), размещенная в InfoPath, будет искать предопределенную группу кода с именем " *шаблоны форм InfoPath* " на уровне политики компьютера в группе All_Code.</span><span class="sxs-lookup"><span data-stu-id="24ab5-106">The common language runtime (CLR) hosted by InfoPath will look for a predefined code group named  *InfoPath Form Templates*  at the Machine policy level under the All_Code group.</span></span> <span data-ttu-id="24ab5-107">Среда CLR применит наборы разрешений, определенные в этой группе, к домену приложений (AppDomain), в котором запускается код формы.</span><span class="sxs-lookup"><span data-stu-id="24ab5-107">The CLR will apply the permission sets that are defined under that group to the application domain (AppDomain) where the form code runs.</span></span> <span data-ttu-id="24ab5-108">Это позволяет настраивать наборы разрешений, которые предоставляются шаблонам форм InfoPath с управляемым кодом.</span><span class="sxs-lookup"><span data-stu-id="24ab5-108">This enables you to customize the permission sets that are granted to InfoPath managed code form templates.</span></span> <span data-ttu-id="24ab5-109">Например, вы можете предоставить шаблон формы, скачанный из https://MySite разрешения на доступ к Active Directory.</span><span class="sxs-lookup"><span data-stu-id="24ab5-109">For example, you can grant a form template downloaded from https://MySite permission to access the Active Directory.</span></span> 
  
<span data-ttu-id="24ab5-110">Для применения пользовательской политики безопасности, определенной с помощью оснастки "Конфигурация .NET", необходимо развернуть эту политику на всех клиентских компьютерах, на которых будет запускаться шаблон формы.</span><span class="sxs-lookup"><span data-stu-id="24ab5-110">For custom security policy defined by using the .NET Configuration snap-in to be applied, it must be deployed on all the client computers where the form template will run.</span></span>
  
<span data-ttu-id="24ab5-111">Дополнительные сведения о модели безопасности для шаблонов форм с управляемым кодом InfoPath приведены [в статье о модели безопасности для шаблонов форм с кодом](about-the-security-model-for-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="24ab5-111">For more information about the security model for InfoPath managed code form templates, see [About the Security Model for Form Templates with Code](about-the-security-model-for-form-templates-with-code.md)</span></span>
  
## <a name="creating-a-code-group-for-infopath-form-templates"></a><span data-ttu-id="24ab5-112">Создание группы кода для шаблонов форм InfoPath</span><span class="sxs-lookup"><span data-stu-id="24ab5-112">Creating a Code Group for InfoPath Form Templates</span></span>

<span data-ttu-id="24ab5-113">Следующая процедура создаст группу кода, которая не предоставляет разрешения для шаблонов форм с управляемым кодом InfoPath (за исключением тех, которые установлены или зарегистрированы на локальном компьютере), в которой можно назначить наборы разрешений шаблонам форм InfoPath, размещенным по определенным URL-адресам или UNC.</span><span class="sxs-lookup"><span data-stu-id="24ab5-113">The following procedure will create a code group that grants no permissions to InfoPath managed code form templates (except those that are installed or registered on your local computer) under which you can assign permission sets to InfoPath form templates located at specific URLs or UNCs.</span></span> <span data-ttu-id="24ab5-114">Сведения о том, как создавать и назначать наборы разрешений группам кода в группе `InfoPath Form Templates` кода, приведены в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="24ab5-114">For information about how to create and assign permission sets to code groups within the  `InfoPath Form Templates` code group, see the following procedure.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24ab5-115">В отличие от средства **настройки Microsoft .NET framework 1,1** , устанавливаемого вместе с распространяемым пакетом Microsoft .net Framework 1,1, **Конфигурация microsoft .NET Framework 2,0** устанавливается только с платформой Microsoft .NET Framework. Пакет средств разработки программного обеспечения (SDK) 2,0.</span><span class="sxs-lookup"><span data-stu-id="24ab5-115">Unlike the **Microsoft .NET Framework 1.1 Configuration** tool that is installed with the Microsoft .NET Framework 1.1 Redistributable Package, the **Microsoft .NET Framework 2.0 Configuration** is installed only with the Microsoft .NET Framework 2.0 Software Development Kit (SDK).</span></span> 
  
### <a name="to-create-a-custom-security-code-group-for-infopath-managed-code-forms"></a><span data-ttu-id="24ab5-116">Создание пользовательской группы кода безопасности для форм InfoPath с управляемым кодом</span><span class="sxs-lookup"><span data-stu-id="24ab5-116">To create a custom security code group for InfoPath managed code forms</span></span>

1. <span data-ttu-id="24ab5-117">В меню **Пуск** выберите пункт **Администрирование** и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-117">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="24ab5-118">Если пункт **Администрирование** отсутствует в меню **Пуск**, то из **Панели управления** откройте **Администрирование** и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-118">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="24ab5-119">В разделе **Мой компьютер**разверните узел **Политика безопасности во время выполнения** , узел **компьютера** , **группы кода** , узел **All_Code** , а затем щелкните правой кнопкой мыши узел **All_Code** и выберите команду создать \*\*\*\* , чтобы открыть диалоговое окно \*\*Создание \*\*Диалоговое окно "группа кода".</span><span class="sxs-lookup"><span data-stu-id="24ab5-119">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then right-click the **All_Code** node and click **New** to open the **Create Code Group** dialog box.</span></span> 
    
3. <span data-ttu-id="24ab5-120">Введите имя новой группы `InfoPath Form Templates` кода (этот текст должен быть точным), а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-120">Name the new code group  `InfoPath Form Templates` (this text must be exact), and then click **Next**.</span></span>
    
4. <span data-ttu-id="24ab5-121">Установите для группы кодов тип условия **Весь код**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-121">Set the condition type for the code group to **All Code**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="24ab5-122">Щелкните **Использовать существующий набор разрешений**, назначьте для группы кода набор разрешений значение **Ничего**, нажмите кнопку **Далее**, а затем кнопку **Готово**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-122">Click **Use existing permission set**, assign the **Nothing** permission set to the code group, click **Next**, and then click **Finish**.</span></span>
    
6. <span data-ttu-id="24ab5-123">Чтобы применить новые параметры, закройте и перезапустите InfoPath.</span><span class="sxs-lookup"><span data-stu-id="24ab5-123">To apply the new settings, close and restart InfoPath.</span></span>
    
<span data-ttu-id="24ab5-124">При желании вы можете управлять набором разрешений для всех шаблонов форм InfoPath с управляемым кодом, назначая набор разрешений, отличный от набора разрешений **Nothing** , для группы кода **шаблонов форм InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-124">If you prefer, you can manage the permission set for all InfoPath managed code form templates by assigning a permission set other than the **Nothing** permission set to the **InfoPath Form Templates** code group.</span></span> 
> [!NOTE]
> <span data-ttu-id="24ab5-125">Вы можете изменить набор разрешений для группы кода безопасности в любое время, щелкнув группу правой кнопкой мыши в разделе.</span><span class="sxs-lookup"><span data-stu-id="24ab5-125">You can change the permission set for a security code group at any time by right-clicking the group in the .</span></span> <span data-ttu-id="24ab5-126">Оснастка **net Configuration 2,0** , выберите пункт **свойства**, а затем щелкните вкладку **набор разрешений** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-126">**NET Configuration 2.0** snap-in, clicking **Properties**, and then clicking the **Permission Set** tab.</span></span> 
  
## <a name="assigning-fulltrust-to-forms-at-a-specific-url-or-unc"></a><span data-ttu-id="24ab5-127">Назначение разрешения "FullTrust" для форм, расположенных по указанному URL-адресу или UNC-пути</span><span class="sxs-lookup"><span data-stu-id="24ab5-127">Assigning FullTrust to Forms at a Specific URL or UNC</span></span>

<span data-ttu-id="24ab5-p104">В группе **Шаблоны форм InfoPath** можно создать группы кода, чтобы предоставить набор разрешений полного доверия для шаблонов форм из отдельно взятого URL-адреса или UNC-пути. После этого каждый шаблон формы, публикуемый в указанном месте, будет запускаться с полным доверием.</span><span class="sxs-lookup"><span data-stu-id="24ab5-p104">You can create code groups under the **InfoPath Form Templates** group to grant the full trust permission set to form templates from a particular URL or UNC location. After doing this, every form template published to the specified location will run fully trusted.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="24ab5-130">Шаблон формы, загруженный с локального компьютера (группа кода зоны), загружается InfoPath с использованием случайного URL-адреса.</span><span class="sxs-lookup"><span data-stu-id="24ab5-130">A form template that is loaded from the local computer (My Computer Zone code group) is loaded by InfoPath using a random URL.</span></span> <span data-ttu-id="24ab5-131">По этой причине невозможно использовать следующую процедуру, чтобы предоставить набор разрешений FullTrust такому шаблону формы.</span><span class="sxs-lookup"><span data-stu-id="24ab5-131">For this reason, you cannot use the following procedure to grant the FullTrust permission set to such a form template.</span></span> <span data-ttu-id="24ab5-132">Чтобы предоставить локально установленный шаблон формы набор разрешений FullTrust, используйте одну из процедур, описанных в разделе "Развертывание шаблонов форм, требующих полного доверия" в разделе [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md) .</span><span class="sxs-lookup"><span data-stu-id="24ab5-132">To grant a locally installed form template the FullTrust permission set, use one of the procedures that are described in the "Deploying Form Templates That Require Full Trust" section of the [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md) topic.</span></span> 
  
### <a name="to-assign-fulltrust-to-infopath-forms-at-a-specific-url-or-unc-location"></a><span data-ttu-id="24ab5-133">Назначение набора разрешений "FullTrust" для форм InfoPath, расположенных по указанному URL-адресу или UNC-пути</span><span class="sxs-lookup"><span data-stu-id="24ab5-133">To assign FullTrust to InfoPath forms at a specific URL or UNC location</span></span>

1. <span data-ttu-id="24ab5-134">В меню **Пуск** выберите пункт **Администрирование** и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-134">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="24ab5-135">Если пункт **Администрирование** отсутствует в меню **Пуск**, то из **Панели управления** откройте **Администрирование** и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-135">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="24ab5-136">В разделе **Мой компьютер**разверните узел **Политика безопасности во время выполнения** , **узел компьютера** , **группы кода** , узел **All_Code** , а затем щелкните узел **шаблоны форм InfoPath** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-136">Under **My Computer**, expand the **Runtime Security Policy** node, the **Machine** node, **Code Groups** node, the **All_Code** node, and then click the **InfoPath Form Templates** node.</span></span> 
    
3. <span data-ttu-id="24ab5-137">В **Списке задач** на панели справа выберите **Добавить дочернюю группу кода**, задайте имя этой группе кода и нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-137">In **Tasks** list in the right pane, click **Add a Child Code Group**, name the code group, and then click **Next**.</span></span>
    
4. <span data-ttu-id="24ab5-138">В списке **выберите тип условия для этой группы кода** выберите **URL-адрес**, а затем введите URL-адрес или UNC-адрес для расположения шаблонов форм InfoPath с управляемым кодом, которые требуется предоставить набор разрешений **FullTrust** .</span><span class="sxs-lookup"><span data-stu-id="24ab5-138">In the **Choose the condition type for this code group** list, select **URL**, and then enter the URL or UNC for the location of the InfoPath managed code form templates that you want to grant the **FullTrust** permission set.</span></span> 
    
    <span data-ttu-id="24ab5-139">Чтобы ограничить набор разрешений одним шаблоном формы, укажите полный путь к этому шаблону формы.</span><span class="sxs-lookup"><span data-stu-id="24ab5-139">To restrict the permission set to a single form template, specify the full path of that particular form template.</span></span> <span data-ttu-id="24ab5-140">Например:</span><span class="sxs-lookup"><span data-stu-id="24ab5-140">For example:</span></span>
    
     `\\MyServer\MyShare\MyFormTemplate.xsn`
    
     `https://MySite/MySubsite/MyFormTempate.xsn`
    
    <span data-ttu-id="24ab5-p107">Чтобы предоставить набор разрешений для всех шаблонов форм в рамках URL-адреса или UNC-пути, не указывайте имя шаблона и добавьте звездочку в конце URL-адреса или UNC-пути. Например:</span><span class="sxs-lookup"><span data-stu-id="24ab5-p107">To grant the permission set to all form templates in a URL or UNC, omit the name of the template and add an asterisk at the end of the URL or UNC. For example:</span></span>
    
     `\\MyServer\MyShare\*`
    
     `https://MySite/MySubsite/*`
    
5. <span data-ttu-id="24ab5-143">Нажмите кнопку **Далее**, затем щелкните **Использовать существующий набор разрешений** и назначьте набор разрешений **FullTrust** для этой группы кода.</span><span class="sxs-lookup"><span data-stu-id="24ab5-143">Click **Next**, and then click **Use existing permission set** and assign the **FullTrust** permission set to the code group.</span></span> 
    
6. <span data-ttu-id="24ab5-144">Нажмите кнопку **Далее**, а затем — **Готово**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-144">Click **Next**, and then click **Finish**.</span></span>
    
7. <span data-ttu-id="24ab5-145">Чтобы применить новые параметры, закройте и перезапустите InfoPath.</span><span class="sxs-lookup"><span data-stu-id="24ab5-145">To apply the new settings, close and restart InfoPath.</span></span>
    
> [!NOTE]
> <span data-ttu-id="24ab5-146">Чтобы применить более ограниченный или пользовательский набор разрешений, выберите на шаге 4 соответствующий вариант вместо **FullTrust**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-146">To apply a more restrictive or custom permission set, select the appropriate option instead of **FullTrust** in step 4.</span></span> 
  
## <a name="creating-a-deployment-package-for-infopath-security-policy"></a><span data-ttu-id="24ab5-147">Создание пакета развертывания для политики безопасности InfoPath</span><span class="sxs-lookup"><span data-stu-id="24ab5-147">Creating a Deployment Package for InfoPath Security Policy</span></span>

<span data-ttu-id="24ab5-148">Определив пользовательскую политику безопасности для шаблонов с управляемыми формами InfoPath, можно создать пакет установщика Windows (MSI), чтобы развернуть эту политику безопасности на компьютерах пользователей с помощью групповой политики или Microsoft Systems Management Server.</span><span class="sxs-lookup"><span data-stu-id="24ab5-148">After defining custom security policy for InfoPath managed-form templates, you can create a Windows Installer Package (.msi) to deploy this security policy on users' computers by using Group Policy or Microsoft Systems Management Server.</span></span>
  
### <a name="to-create-a-deployment-package-for-custom-infopath-security-policy"></a><span data-ttu-id="24ab5-149">Создание пакета развертывания для пользовательской политики безопасности InfoPath</span><span class="sxs-lookup"><span data-stu-id="24ab5-149">To create a deployment package for custom InfoPath security policy</span></span>

1. <span data-ttu-id="24ab5-150">В меню **Пуск** выберите пункт **Администрирование** и щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-150">From the **Start** menu, point to **Administrative Tools**, and then click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
    <span data-ttu-id="24ab5-151">Если пункт **Администрирование** отсутствует в меню **Пуск**, то из **Панели управления** откройте **Администрирование** и дважды щелкните **Конфигурация Microsoft .NET Framework 2.0**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-151">If you do not have **Administrative Tools** on the **Start** menu, from the **Control Panel** open **Administrative Tools**, and then double-click **Microsoft .NET Framework 2.0 Configuration**.</span></span>
    
2. <span data-ttu-id="24ab5-152">Щелкните правой кнопкой мыши пункт **Политика безопасности во время выполнения**, а затем выберите **Создать пакет развертывания**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-152">Right-click **Runtime Security Policy**, and then click **Create Deployment Package**.</span></span>
    
3. <span data-ttu-id="24ab5-153">В разделе **Выберите уровень политики безопасности для развертывания** щелкните **Компьютер**, укажите папку и имя файла для пакета установщика Windows, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="24ab5-153">Under **Select the security policy to deploy**, click **Machine**, specify the folder and file name for the Windows Installer Package, and then click **Next**.</span></span>
    
4. <span data-ttu-id="24ab5-154">Нажмите кнопку **Готово**, чтобы создать пакет развертывания.</span><span class="sxs-lookup"><span data-stu-id="24ab5-154">Click **Finish** to create the deployment package.</span></span> 
    
5. <span data-ttu-id="24ab5-155">Для получения сведений об использовании средства настройки .NET Framework выполните поиск по справке по Visual Studio или веб-сайту MSDN для "средства настройки .NET Framework Configuration (Mscorcfg. msc)".</span><span class="sxs-lookup"><span data-stu-id="24ab5-155">For information about how to use the .NET Framework Configuration tool, search Visual Studio Help or the MSDN website for ".NET Framework Configuration Tool (Mscorcfg.msc)".</span></span>
    
## <a name="see-also"></a><span data-ttu-id="24ab5-156">См. также</span><span class="sxs-lookup"><span data-stu-id="24ab5-156">See also</span></span>



[<span data-ttu-id="24ab5-157">Модель безопасности для шаблонов форм с кодом</span><span class="sxs-lookup"><span data-stu-id="24ab5-157">About the Security Model for Form Templates with Code</span></span>](about-the-security-model-for-form-templates-with-code.md)

