---
title: Предварительный просмотр и отладка шаблонов форм, требующих полного доверия
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Отладка [InfoPath 2007], шаблоны форм, совместимые с InfoPath 2003, предварительный просмотр шаблонов форм, совместимых с InfoPath 2003, шаблоны форм [InfoPath 2007], предварительный просмотр совместимых с 2003, шаблонов форм [InfoPath 2007], отладка 2003 совместимость, отладка Шаблоны форм, совместимые с InfoPath 2003
localization_priority: Normal
ms.assetid: 5c491666-06f0-42ec-967e-1c70cd5e03a0
description: По умолчанию при попытке отладки или предварительного просмотра проекта с управляемым кодом, который содержит код, который вызывает элемент объектной модели, требующий полного доверия, например свойство LoginName, которое требует доступа к сведениям о домене входа пользователя, Microsoft В InfoPath будут отображены следующие сообщения об ошибках.
ms.openlocfilehash: 0780db286e2ca9cef381c2d24cb621c7c243dcb7
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303600"
---
# <a name="preview-and-debug-form-templates-that-require-full-trust"></a><span data-ttu-id="9467f-104">Предварительный просмотр и отладка шаблонов форм, требующих полного доверия</span><span class="sxs-lookup"><span data-stu-id="9467f-104">Preview and Debug Form Templates that Require Full Trust</span></span>

<span data-ttu-id="9467f-105">По умолчанию при попытке отладить или предварительно просмотреть проект с управляемым кодом, содержащий код, который вызывает элемент объектной модели, требующий полного доверия, например свойство **LoginName** , которое требует доступа к сведениям о домене входа пользователя, В Microsoft InfoPath отобразятся следующие сообщения об ошибках.</span><span class="sxs-lookup"><span data-stu-id="9467f-105">By default, if you attempt to debug or preview a managed-code project that contains code that invokes an object model member that requires full trust, such as the **LoginName** property which requires access to information about the user's login domain, Microsoft InfoPath will display the following error messages.</span></span> 
  
<span data-ttu-id="9467f-106">При просмотре:</span><span class="sxs-lookup"><span data-stu-id="9467f-106">When previewing:</span></span>
  
<span data-ttu-id="9467f-p101">"В коде формы появилось необработанное исключение". И далее: "Приложению InfoPath не удалось выполнить это действие из-за ошибки в коде формы".</span><span class="sxs-lookup"><span data-stu-id="9467f-p101">"An unhandled exception has occurred in the form's code." Followed by, "InfoPath cannot complete this action, because of an error in the form's code."</span></span>
  
<span data-ttu-id="9467f-109">При отладке</span><span class="sxs-lookup"><span data-stu-id="9467f-109">When debugging:</span></span>
  
<span data-ttu-id="9467f-110">Фокус перейдет к строке кода в редакторе кода, вызывающему элемент, требующий полного доверия, и появится следующее сообщение: " **SecurityException** не обработано пользовательским кодом — запрос не выполнен".</span><span class="sxs-lookup"><span data-stu-id="9467f-110">Focus will move to the line of code in the code editor that is calling the member that requires full trust, and the following message will be displayed: " **SecurityException** was unhandled by user code - Request failed".</span></span> 
  
<span data-ttu-id="9467f-111">Чтобы разрешить бизнес-логике шаблона формы вызывать этот элемент при его отладке и просмотре, необходимо установить для уровня безопасности шаблона формы значение **Полное доверие**, воспользовавшись приведенной далее процедурой.</span><span class="sxs-lookup"><span data-stu-id="9467f-111">To allow the form template's business logic to call this member when it is being debugged or previewed, you must set your form template's security level to **Full Trust** as described in the following procedure.</span></span> 
  
## <a name="configuring-a-managed-code-form-template-that-requires-full-trust"></a><span data-ttu-id="9467f-112">Настройка шаблона формы с управляемым кодом, требующего полного доверия</span><span class="sxs-lookup"><span data-stu-id="9467f-112">Configuring a Managed Code Form Template that Requires Full Trust</span></span>

### <a name="set-your-forms-security-level-to-full-trust"></a><span data-ttu-id="9467f-113">Настройка значения "Полное доверие" для уровня безопасности формы</span><span class="sxs-lookup"><span data-stu-id="9467f-113">Set your form's security level to Full Trust</span></span>

1. <span data-ttu-id="9467f-114">В InfoPath откройте шаблон в режиме конструктора.</span><span class="sxs-lookup"><span data-stu-id="9467f-114">In InfoPath, open the form template in design mode.</span></span>
    
2. <span data-ttu-id="9467f-115">Перейдите на вкладку **Файл** и выберите пункт **Параметры формы** на вкладке **Сведения**.</span><span class="sxs-lookup"><span data-stu-id="9467f-115">Click the **File** tab, and then click **Form Options** on the **Info** tab.</span></span> 
    
3. <span data-ttu-id="9467f-116">В списке **Категория** выберите пункт **Безопасность и доверие**.</span><span class="sxs-lookup"><span data-stu-id="9467f-116">In the **Category** list, click **Security and Trust.**</span></span>
    
4. <span data-ttu-id="9467f-117">В группе **Уровень безопасности** снимите флажок **Автоматически определять уровень безопасности (рекомендуется)**.</span><span class="sxs-lookup"><span data-stu-id="9467f-117">Under **Security Level**, clear **Automatically determine security level**.</span></span>
    
5. <span data-ttu-id="9467f-118">Выберите **Полное доверие** и нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="9467f-118">Select **Full Trust**, and then click **OK**.</span></span>
    
<span data-ttu-id="9467f-119">После выполнения этой процедуры вы можете отладить проект, как описано в статье [Preview and debug Templates Forms с кодом](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="9467f-119">After this procedure is performed, you can debug your project as described in [Preview and Debug InfoPath Form Templates with Code](how-to-preview-and-debug-infopath-form-templates-with-code.md).</span></span>
  
> [!NOTE]
> <span data-ttu-id="9467f-120">Для развертывания шаблона формы с управляемым кодом, требующего полного доверия, необходимы дополнительные действия, такие как добавление цифровой подписи или установка и регистрация шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="9467f-120">Successfully deploying a managed code form template that requires full trust requires additional steps, such as digitally signing, or installing and registering the form template.</span></span> <span data-ttu-id="9467f-121">Для получения сведений о развертывании шаблона формы с управляемым кодом после его отладки [разверните шаблоны форм InfoPath с кодом](how-to-deploy-infopath-form-templates-with-code.md).</span><span class="sxs-lookup"><span data-stu-id="9467f-121">For information on deploying a managed code form template after it is debugged see, [Deploy InfoPath Form Templates with Code](how-to-deploy-infopath-form-templates-with-code.md).</span></span> 
  
## <a name="see-also"></a><span data-ttu-id="9467f-122">См. также</span><span class="sxs-lookup"><span data-stu-id="9467f-122">See also</span></span>



[<span data-ttu-id="9467f-123">Предварительный просмотр и отладка шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="9467f-123">Preview and Debug InfoPath Form Templates with Code</span></span>](how-to-preview-and-debug-infopath-form-templates-with-code.md)
  
[<span data-ttu-id="9467f-124">Развертывание шаблонов форм InfoPath с кодом</span><span class="sxs-lookup"><span data-stu-id="9467f-124">Deploy InfoPath Form Templates with Code</span></span>](how-to-deploy-infopath-form-templates-with-code.md)

