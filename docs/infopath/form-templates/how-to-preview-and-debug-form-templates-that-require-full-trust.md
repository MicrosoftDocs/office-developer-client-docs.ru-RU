---
title: Предварительный просмотр и отлагивание шаблонов форм, которые требуют полного доверия
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- отладка [infopath 2007], infopath 2003-compatible form templates,previewing InfoPath 2003-compatible form templates,form templates [InfoPath 2007], previewing 2003-compatible,form templates [InfoPath 2007], debugging 2003-compatible,debugging InfoPath 2003-compatible form templates
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: По умолчанию при попытке отлаживать или предварительно просматривать проект с управляемым кодом, содержащий код, который вызывает член объектной модели, которому требуется полное доверие, например свойство LoginName, которое требует доступа к сведениям о домене входа пользователя, Microsoft InfoPath отобразит следующие сообщения об ошибке.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33411262"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="a04a6-104">Предварительный просмотр и отлагивание шаблонов форм, которые требуют полного доверия</span><span class="sxs-lookup"><span data-stu-id="a04a6-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="a04a6-105">По умолчанию при попытке отлаживать или предварительно просматривать проект с управляемым кодом, содержащий код, который вызывает член объектной модели, которому требуется полное доверие, например свойство **LoginName,** которое требует доступа к сведениям о домене входа пользователя, Microsoft InfoPath отобразит следующие сообщения об ошибке.</span><span class="sxs-lookup"><span data-stu-id="a04a6-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="a04a6-106">При просмотре:</span><span class="sxs-lookup"><span data-stu-id="a04a6-106">When previewing:</span></span>
  
<span data-ttu-id="a04a6-p101">"В коде формы появилось необработанное исключение". И далее: "Приложению InfoPath не удалось выполнить это действие из-за ошибки в коде формы".</span><span class="sxs-lookup"><span data-stu-id="a04a6-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="a04a6-109">При отладке</span><span class="sxs-lookup"><span data-stu-id="a04a6-109">When debugging:</span></span>
  
<span data-ttu-id="a04a6-110">Фокус будет перемещаться на строку кода в редакторе кода, который вызывает член, требуя полного доверия, и отобразится следующее сообщение: **"SecurityException** was unhandled by user code - Request failed".</span><span class="sxs-lookup"><span data-stu-id="a04a6-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="a04a6-111">Чтобы разрешить бизнес-логике шаблона формы вызывать этот элемент при его отладке и просмотре, необходимо установить для уровня безопасности шаблона формы значение **Полное доверие**, воспользовавшись приведенной далее процедурой.</span><span class="sxs-lookup"><span data-stu-id="a04a6-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="a04a6-112">Настройка шаблона формы с управляемым кодом, требующего полного доверия</span><span class="sxs-lookup"><span data-stu-id="a04a6-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="a04a6-113">Настройка значения "Полное доверие" для уровня безопасности формы</span><span class="sxs-lookup"><span data-stu-id="a04a6-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="a04a6-114">В InfoPath откройте шаблон в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="a04a6-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="a04a6-115">Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="a04a6-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="a04a6-116">В списке **Категория** выберите пункт **Безопасность и доверие**.</span><span class="sxs-lookup"><span data-stu-id="a04a6-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="a04a6-117">В группе **Уровень безопасности** снимите флажок **Автоматически определять уровень безопасности (рекомендуется)**.</span><span class="sxs-lookup"><span data-stu-id="a04a6-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="a04a6-118">Выберите **Полное доверие** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="a04a6-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="a04a6-119">После выполнения этой процедуры можно выполнить отлаживать проект, как описано в предварительных версиях и отлаживать шаблоны форм [InfoPath с кодом.](how-to-preview-and-debug-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="a04a6-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="a04a6-120">Для развертывания шаблона формы с управляемым кодом, требующего полного доверия, необходимы дополнительные действия, такие как добавление цифровой подписи или установка и регистрация шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="a04a6-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="a04a6-121">Сведения о развертывании шаблона формы с управляемым кодом после отладки см. в под названием "Развертывание шаблонов форм [InfoPath с кодом".](how-to-deploy-infopath-form-templates-with-code.md)</span><span class="sxs-lookup"><span data-stu-id="a04a6-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="a04a6-122">См. также</span><span class="sxs-lookup"><span data-stu-id="a04a6-122">See also</span></span>



[<span data-ttu-id="a04a6-123">Предварительный просмотр и отлаживка шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="a04a6-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="a04a6-124">Развертывание шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="a04a6-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

