---
title: Публикация форм с кодом
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
localization_priority: Normal
ms.assetid: caafab24-6413-4731-813d-cba3ae9ea97e
description: Любым администратором семейства сайтов могут публиковать форм с кодом непосредственно из мастера публикации InfoPath Designer для библиотеки форм в SharePoint. Код выполняется в изолированной среде, что предотвращает выполнение вредоносного кода на сервере. Этот процесс называется публикацией изолированного решения или публикацией в изолированной инфраструктуре SharePoint.
ms.openlocfilehash: c25243a966bc1dc1a559ccf2ba58fabfadbd94a2
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807598"
---
# <a name="publishing-forms-with-code"></a><span data-ttu-id="6732b-105">Публикация форм с кодом</span><span class="sxs-lookup"><span data-stu-id="6732b-105">Publishing Forms with Code</span></span>

<span data-ttu-id="6732b-106">Любым администратором семейства сайтов могут публиковать форм с кодом непосредственно из мастера публикации InfoPath Designer для библиотеки форм в SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6732b-106">Any site collection administrator can publish forms with code directly from the InfoPath Designer publishing wizard to a form library on SharePoint.</span></span> <span data-ttu-id="6732b-107">Код выполняется в изолированной среде, что предотвращает выполнение вредоносного кода на сервере.</span><span class="sxs-lookup"><span data-stu-id="6732b-107">The code is executed in a sandboxed environment so that malicious code cannot harm the server.</span></span> <span data-ttu-id="6732b-108">Этот процесс называется публикацией изолированного решения или публикацией в изолированной инфраструктуре SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6732b-108">This is referred to as publishing a sandboxed solution or publishing to the SharePoint sandbox infrastructure.</span></span>
  
<span data-ttu-id="6732b-109">InfoPath 2010 и SharePoint Server 2010 также поддерживают решений, рассматриваемых администратором.</span><span class="sxs-lookup"><span data-stu-id="6732b-109">InfoPath 2010 and SharePoint Server 2010 also support administrator-deployed solutions.</span></span> <span data-ttu-id="6732b-110">Разработчик формы публикует формы с кодом в локальном хранилище, которое затем просматривается и отправляется администратором фермы SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6732b-110">A form designer publishes forms with code to a local store which are later reviewed and uploaded by a SharePoint farm administrator.</span></span> <span data-ttu-id="6732b-111">Коду предоставляется уровень полного доверия, поэтому в его состав могут быть включены функции, выполнение которых требует особых привилегий (например, ввод-вывод файлов).</span><span class="sxs-lookup"><span data-stu-id="6732b-111">The code is given full trust, and can incorporate functionality requiring elevated privileges such as file IO.</span></span>
  
## <a name="comparing-sandboxed-and-administrator-approved-solutions"></a><span data-ttu-id="6732b-112">Сравнение изолированных решений и решений, подлежащих рассмотрению администратором</span><span class="sxs-lookup"><span data-stu-id="6732b-112">Comparing Sandboxed and Administrator-approved Solutions</span></span>

<span data-ttu-id="6732b-113">В следующей таблице представлены различия между публикацией изолированных решений и публикацией решений, рассматриваемых администратором.</span><span class="sxs-lookup"><span data-stu-id="6732b-113">The following table summarizes the differences between publishing sandboxed and administrator-approved solutions.</span></span> 
  
||<span data-ttu-id="6732b-114">**Изолированные решения**</span><span class="sxs-lookup"><span data-stu-id="6732b-114">**Sandboxed Solutions**</span></span>|<span data-ttu-id="6732b-115">**Решения, рассматриваемые администратором**</span><span class="sxs-lookup"><span data-stu-id="6732b-115">**Administrator-approved Solutions**</span></span>|
|:-----|:-----|:-----|
|<span data-ttu-id="6732b-116">**Требуемые разрешения**</span><span class="sxs-lookup"><span data-stu-id="6732b-116">**Permissions Required**</span></span> <br/> |<span data-ttu-id="6732b-117">Могут публиковаться любым администратором семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="6732b-117">Can be published by any site collection administrator.</span></span>  <br/> |<span data-ttu-id="6732b-118">Могут развертываться администратором фермы.</span><span class="sxs-lookup"><span data-stu-id="6732b-118">Can be deployed by a farm administrator.</span></span>  <br/> |
|<span data-ttu-id="6732b-119">**Публикация**</span><span class="sxs-lookup"><span data-stu-id="6732b-119">**Publishing**</span></span> <br/> |<span data-ttu-id="6732b-120">Могут публиковаться прямо из InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6732b-120">Can be published directly from InfoPath.</span></span>  <br/> |<span data-ttu-id="6732b-121">Могут публиковаться с помощью центра администрирования или средства командной строки stsadm.</span><span class="sxs-lookup"><span data-stu-id="6732b-121">Can be deployed using Central Administration or the stsadm command-line tool.</span></span>  <br/> |
|<span data-ttu-id="6732b-122">**Защита**</span><span class="sxs-lookup"><span data-stu-id="6732b-122">**Protection**</span></span> <br/> |<span data-ttu-id="6732b-p104">Код запускается в изолированной среде. Это защищает сервер от выполнения вредоносного кода.</span><span class="sxs-lookup"><span data-stu-id="6732b-p104">Code is run in a sandboxed environment. This helps protect the server from malicious code.</span></span>  <br/> |<span data-ttu-id="6732b-125">Код может запускаться с уровнем полного доверия и доступом ко всем ресурсам сервера.</span><span class="sxs-lookup"><span data-stu-id="6732b-125">Code can run with full trust and access any resource on the server.</span></span>  <br/> |
|<span data-ttu-id="6732b-126">**Рекомендации по использованию**</span><span class="sxs-lookup"><span data-stu-id="6732b-126">**Recommended Use**</span></span> <br/> |<span data-ttu-id="6732b-127">Формы, требующие небольшого объема кода.</span><span class="sxs-lookup"><span data-stu-id="6732b-127">Forms that only require a small amount of code.</span></span>  <br/> |<span data-ttu-id="6732b-128">Формы, содержащие большой объем кода.</span><span class="sxs-lookup"><span data-stu-id="6732b-128">Forms that contain many lines of code.</span></span>  <br/> |
   
### <a name="publishing-form-templates-as-sandboxed-solutions"></a><span data-ttu-id="6732b-129">Публикация шаблонов формы в качестве изолированных решений</span><span class="sxs-lookup"><span data-stu-id="6732b-129">Publishing Form Templates as Sandboxed Solutions</span></span>

<span data-ttu-id="6732b-p105">Публикация формы с кодом в качестве решения изолированные решения не отличается от публикации другой формы в библиотеку документов. С помощью мастера публикации форма будет отправлена на сервер и будет выполняться в изолированной среде.</span><span class="sxs-lookup"><span data-stu-id="6732b-p105">Publishing a form with code as a sandboxed solution is no different from publishing any other form to a document library. Just use the publishing wizard as usual and your form will be uploaded to the server and will operate in the sandbox.</span></span>
  
<span data-ttu-id="6732b-132">Обратите внимание на то, что при развертывании формы в качестве решения изолированные решения существуют определенные ограничения:</span><span class="sxs-lookup"><span data-stu-id="6732b-132">Note that there are certain restrictions to deploying your form as a sandboxed solution:</span></span>
  
- <span data-ttu-id="6732b-133">Форма должна быть формой InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6732b-133">Must be an InfoPath form.</span></span>
    
- <span data-ttu-id="6732b-134">В качестве языка программирования форма должна использовать C# или Visual Basic.</span><span class="sxs-lookup"><span data-stu-id="6732b-134">Must use C# or Visual Basic as the programming language.</span></span>
    
- <span data-ttu-id="6732b-135">Не удается отправить по электронной почте подключениями к данным.</span><span class="sxs-lookup"><span data-stu-id="6732b-135">Cannot submit to email data connections.</span></span>
    
- <span data-ttu-id="6732b-136">Распространение свойств при соединениях между частями невозможно.</span><span class="sxs-lookup"><span data-stu-id="6732b-136">Cannot have properties promoted for part-to-part connections.</span></span>
    
- <span data-ttu-id="6732b-137">Наличие управляемых элементов управления метаданными или подключений к данным невозможно.</span><span class="sxs-lookup"><span data-stu-id="6732b-137">Must not have any managed meta-data controls or data connections.</span></span>
    
<span data-ttu-id="6732b-138">Чтобы разрешить администраторам семейства использовать решения изолированные решения в Microsoft SharePoint Server 2010 или сервер под управлением Microsoft SharePoint Foundation 2010, администратору фермы необходимо запустить службу пользовательского кода Windows SharePoint.</span><span class="sxs-lookup"><span data-stu-id="6732b-138">To enable site collection administrators to use sandboxed solutions on Microsoft SharePoint Server 2010 or a server that runs Microsoft SharePoint Foundation 2010, the farm administrator must start the Windows SharePoint User Code service.</span></span>
  
### <a name="to-start-the-windows-sharepoint-user-code-service"></a><span data-ttu-id="6732b-139">Запуск службы пользовательского кода Windows SharePoint</span><span class="sxs-lookup"><span data-stu-id="6732b-139">To start the Windows SharePoint User Code service</span></span>

1. <span data-ttu-id="6732b-140">Откройте центр администрирования.</span><span class="sxs-lookup"><span data-stu-id="6732b-140">Open Central Administration.</span></span>
    
2. <span data-ttu-id="6732b-141">В разделе **Системные службы** щелкните команду **Управление службами на сервере**.</span><span class="sxs-lookup"><span data-stu-id="6732b-141">Under **System Services**, click **Manage services on server**.</span></span>
    
3. <span data-ttu-id="6732b-142">Запустите **службу пользовательского кода Microsoft SharePoint Foundation**.</span><span class="sxs-lookup"><span data-stu-id="6732b-142">Start the **Microsoft SharePoint Foundation User Code Service**.</span></span>
    
### <a name="to-publish-a-sandboxed-solution"></a><span data-ttu-id="6732b-143">Публикация изолированного решения</span><span class="sxs-lookup"><span data-stu-id="6732b-143">To publish a sandboxed solution</span></span>

1. <span data-ttu-id="6732b-144">Откройте шаблон формы в конструкторе InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6732b-144">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="6732b-145">Откройте вкладку **Файл**, а затем щелкните элемент **Сервер SharePoint** на вкладке **Публикация** в Backstage.</span><span class="sxs-lookup"><span data-stu-id="6732b-145">Click the **File** tab, and then click **SharePoint Server** on the **Publish** tab in the Backstage.</span></span> 
    
3. <span data-ttu-id="6732b-146">Введите URL-адрес сайта SharePoint, на который выполняется публикация, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-146">Enter the URL of the SharePoint site to publish to, and then click **Next**.</span></span> 
    
    > [!IMPORTANT]
    > <span data-ttu-id="6732b-147">Для публикации формы на сайте в качестве решения изолированные решения необходимо иметь привилегии администратора семейства сайтов.</span><span class="sxs-lookup"><span data-stu-id="6732b-147">You must be a site collection administrator on this site to publish this form template as a sandboxed solution.</span></span> 
  
4. <span data-ttu-id="6732b-148">Выберите элемент **Библиотека форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-148">Select **Form Library**, and then click **Next**.</span></span>
    
5. <span data-ttu-id="6732b-149">Выберите команду **Создать библиотеку форм**, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-149">Select **Create a new form library**, and then click **Next**.</span></span>
    
6. <span data-ttu-id="6732b-150">Введите имя и описание для библиотеки форм, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-150">Enter the name and descriptions for your form library, and then click **Next**.</span></span>
    
7. <span data-ttu-id="6732b-151">Нажмите кнопку **Опубликовать**.</span><span class="sxs-lookup"><span data-stu-id="6732b-151">Click **Publish**.</span></span>
    
<span data-ttu-id="6732b-152">Примеры решений для ситуаций, в которых шаблоны форм следует публиковать в качестве решения изолированные решения, представлены в разделе [Примеры изолированных решений](sample-sandboxed-solutions.md).</span><span class="sxs-lookup"><span data-stu-id="6732b-152">For example solutions that demonstrate scenarios that are appropriate for form templates published as sandboxed solutions, see [Sample Sandboxed Solutions](sample-sandboxed-solutions.md).</span></span>
  
### <a name="publishing-form-templates-as-administrator-deployed-solutions"></a><span data-ttu-id="6732b-153">Публикация шаблонов формы в качестве решений, рассматриваемых администратором</span><span class="sxs-lookup"><span data-stu-id="6732b-153">Publishing Form Templates as Administrator-Deployed Solutions</span></span>

<span data-ttu-id="6732b-154">Публикация формы в качестве шаблона, рассматриваемого администратором, рекомендуется в том случае, если форма имеет несколько подключений к данным, требует уровня полного доверия, или в том случае, если необходим шаблон для всей фермы.</span><span class="sxs-lookup"><span data-stu-id="6732b-154">Publishing your form as an administrator-approved template is recommended if your form has many data connections, if it requires full-trust security, or if you require a farm-wide template.</span></span>
  
<span data-ttu-id="6732b-155">Перед тем как такое решение будет доступно на сайте SharePoint, администратор фермы должен выполнить определенные действия, а разработчик должен подготовить решение к рассмотрению.</span><span class="sxs-lookup"><span data-stu-id="6732b-155">There are several steps that a farm administrator must complete before an administrator-deployed solution is available on SharePoint, and you as the developer must prepare the solution before the administrator is engaged.</span></span>
  
<span data-ttu-id="6732b-156">Во-первых, если форма будет развернута с полным доверием, то необходимо установить уровень безопасности, как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="6732b-156">First, if your form is going to be deployed as full trust, you must set the security level as described in the following procedure.</span></span>
  
### <a name="to-set-the-security-level-of-a-form-template-to-full-trust"></a><span data-ttu-id="6732b-157">Установка уровня полного доверия для шаблона формы</span><span class="sxs-lookup"><span data-stu-id="6732b-157">To set the security level of a form template to full trust</span></span>

1. <span data-ttu-id="6732b-158">Откройте шаблон формы в конструкторе InfoPath.</span><span class="sxs-lookup"><span data-stu-id="6732b-158">Open the form template in the InfoPath designer.</span></span>
    
2. <span data-ttu-id="6732b-159">Щелкните вкладку **Файл**, а затем на вкладке **Информация** щелкните команду **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="6732b-159">Click the **File** tab, on the **Info** tab click **Form Options**.</span></span>
    
3. <span data-ttu-id="6732b-160">Щелкните категорию **Безопасность и доверие**, а затем снимите флажок **Автоматически определять уровень безопасности**.</span><span class="sxs-lookup"><span data-stu-id="6732b-160">Click the **Security and Trust** category, and then clear the **Automatically determine security level** check box.</span></span> 
    
4. <span data-ttu-id="6732b-161">Выберите параметр **Полное доверие**.</span><span class="sxs-lookup"><span data-stu-id="6732b-161">Select **Full Trust**.</span></span>
    
<span data-ttu-id="6732b-162">Затем выполните публикацию формы, как описано ниже. При этом следует помнить об отличиях от стандартной процедуры публикации.</span><span class="sxs-lookup"><span data-stu-id="6732b-162">Then, publish the form by using the following procedure, but be aware that there are some differences from a standard publishing procedure.</span></span>
  
### <a name="to-publish-an-administrator-deployed-solution"></a><span data-ttu-id="6732b-163">Публикация решения, развертываемого администратором</span><span class="sxs-lookup"><span data-stu-id="6732b-163">To publish an administrator-deployed solution</span></span>

1. <span data-ttu-id="6732b-164">На первой странице **мастера публикации** укажите расположение сайта SharePoint Server 2010 или SharePoint Foundation 2010, а затем нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-164">In the first page of the **Publishing Wizard**, specify the location of the SharePoint Server 2010 or SharePoint Foundation 2010 site, and then click **Next**.</span></span>
    
2. <span data-ttu-id="6732b-p106">InfoPath автоматически установит флажок **Шаблоны форм, утвержденные администратором** на второй странице мастера. Нажмите кнопку **Далее**.</span><span class="sxs-lookup"><span data-stu-id="6732b-p106">InfoPath will automatically select the **Administrator-approved form template** check box on the second page of the wizard. Click **Next**.</span></span>
    
3. <span data-ttu-id="6732b-p107">Третья страница предназначена только для сценариев развертывания администратором. Не выбирайте SharePoint Server, а опубликуйте форму в локальное хранилище. Администратор SharePoint отправит файл из этого расположения в ходе развертывания.</span><span class="sxs-lookup"><span data-stu-id="6732b-p107">The third page is unique to administrator-deployed scenarios. Instead of selecting a SharePoint Server, publish the form to a local store. The SharePoint administrator will upload the file from this location during the administrator deployment process.</span></span>
    
4. <span data-ttu-id="6732b-170">Установите необходимые параметры на остальных страницах **мастера публикации**.</span><span class="sxs-lookup"><span data-stu-id="6732b-170">Complete the remaining pages of the **Publishing Wizard**.</span></span>
    

