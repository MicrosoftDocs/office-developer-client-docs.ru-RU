---
title: Просмотр и отладка шаблонов форм, требующих полного доверия
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- отладка [infopath 2007] совместимых 2003 шаблонов форм infopath, Просмотр шаблонов форм совместимых с InfoPath 2003, просмотр совместимых 2003 шаблонов форм [InfoPath 2007], отладка совместимых 2003, отладка шаблонов форм [InfoPath 2007] Шаблоны форм, совместимые с InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: По умолчанию при попытке отладки или проекта предварительного просмотра с управляемым кодом, который содержит код, вызывающий элемент объектной модели, требующего полного доверия такими как свойство LoginName которого требуется доступ к сведениям о домен для входа пользователя, корпорация Майкрософт InfoPath будет отображаться следующие сообщения об ошибках.
ms.openlocfilehash: e9077b4ec0f8369b869e986020e4860f325fc023
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807487"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="0b91b-104">Просмотр и отладка шаблонов форм, требующих полного доверия</span><span class="sxs-lookup"><span data-stu-id="0b91b-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="0b91b-105">По умолчанию при попытке отладки или проекта предварительного просмотра с управляемым кодом, который содержит код, вызывающий элемент объектной модели, требующего полного доверия такими как свойство **LoginName** которого требуется доступ к сведениям о домен для входа пользователя, Microsoft InfoPath будет отображаться следующие сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="0b91b-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="0b91b-106">При просмотре:</span><span class="sxs-lookup"><span data-stu-id="0b91b-106">When previewing:</span></span>
  
<span data-ttu-id="0b91b-p101">"В коде формы появилось необработанное исключение". И далее: "Приложению InfoPath не удалось выполнить это действие из-за ошибки в коде формы".</span><span class="sxs-lookup"><span data-stu-id="0b91b-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="0b91b-109">При отладке</span><span class="sxs-lookup"><span data-stu-id="0b91b-109">When debugging:</span></span>
  
<span data-ttu-id="0b91b-110">Фокус перемещается на строке кода в редакторе кода, который звонит члена, требующего полного доверия, и отображается следующее сообщение: « **SecurityException** было обработано пользовательским кодом – не удалось выполнить запрос».</span><span class="sxs-lookup"><span data-stu-id="0b91b-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="0b91b-111">Чтобы разрешить бизнес-логика шаблона формы для вызова этот член при отладке или предварительного просмотра, необходимо присвоить уровень безопасности шаблона формы **Полное доверие** как описано в следующей процедуре.</span><span class="sxs-lookup"><span data-stu-id="0b91b-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="0b91b-112">Настройка шаблона формы с управляемым кодом, требующего полного доверия</span><span class="sxs-lookup"><span data-stu-id="0b91b-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="0b91b-113">Настройка значения "Полное доверие" для уровня безопасности формы</span><span class="sxs-lookup"><span data-stu-id="0b91b-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="0b91b-114">В InfoPath откройте шаблон в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="0b91b-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="0b91b-115">Щелкните вкладку **Файл**, а затем  **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="0b91b-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="0b91b-116">В списке **категории** выберите **Безопасность и доверие.**</span><span class="sxs-lookup"><span data-stu-id="0b91b-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="0b91b-117">В разделе **Уровень безопасности**снимите флажок **автоматически определять уровень безопасности**.</span><span class="sxs-lookup"><span data-stu-id="0b91b-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="0b91b-118">Выберите **Полное доверие**и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="0b91b-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="0b91b-119">После выполнения этой процедуры, описанные в [Предварительный просмотр и отладка шаблонов форм InfoPath с кодом](how-to-preview-and-debug-infopath-form-templates-with-code.md)отладку проекта.</span><span class="sxs-lookup"><span data-stu-id="0b91b-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="0b91b-120">Успешное развертывание шаблона формы с управляемым кодом, требующего полного доверия требуются дополнительные действия, такие как цифровые подписи или Установка и регистрация шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="0b91b-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="0b91b-121">Сведения о развертывании шаблона формы с управляемым кодом после его отладки содержатся [Развертывание шаблонов форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="0b91b-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="0b91b-122">См. также</span><span class="sxs-lookup"><span data-stu-id="0b91b-122">See also</span></span>



[<span data-ttu-id="0b91b-123">Просмотр и отладка шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="0b91b-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="0b91b-124">Развертывание шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="0b91b-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

