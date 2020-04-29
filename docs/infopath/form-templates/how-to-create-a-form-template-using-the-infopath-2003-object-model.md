---
title: Создание шаблона формы с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- шаблоны форм, совместимые с InfoPath 2003, шаблоны форм [InfoPath 2007], создание InfoPath 2003 — совместимый, InfoPath 2007, создание шаблонов форм, совместимых с InfoPath 2003
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: В главе описаны действия, необходимые для создания шаблона формы, работающего с объектной моделью, совместимой с InfoPath 2003.
ms.openlocfilehash: 35a9fcfbb0d93a19e013bde6980bc94af3bb5dd9
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33418185"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a><span data-ttu-id="4131c-104">Создание шаблона формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="4131c-104">Create a Form Template Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="4131c-105">В главе описаны действия, необходимые для создания шаблона формы, работающего с объектной моделью, совместимой с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="4131c-105">The procedures in this topic describe how to create a form template that works with the InfoPath 2003-compatible object model.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="4131c-106">Помимо описанных далее процедур, также необходимо выбрать пункт **Сохранить как** на вкладке **Файл**, а затем выбрать **Шаблон формы InfoPath 2003** в поле **Вывод** для сохранения шаблона формы в файл с форматом, совместимым с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="4131c-106">In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format.</span></span> <span data-ttu-id="4131c-107">Кроме того, чтобы открыть шаблоны форм, совместимые с InfoPath 2003, созданные с помощью InfoPath, на компьютерах пользователей InfoPath 2003 должна быть установлена платформа .NET Framework версии 2,0 или более поздней.</span><span class="sxs-lookup"><span data-stu-id="4131c-107">Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers.</span></span> 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a><span data-ttu-id="4131c-108">Создание шаблона формы, совместимого с InfoPath 2003, в InfoPath с набором средств Visual Studio Tools для работы с приложениями</span><span class="sxs-lookup"><span data-stu-id="4131c-108">To create an InfoPath 2003-compatible form template in InfoPath with Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="4131c-109">Запустите конструктор InfoPath.</span><span class="sxs-lookup"><span data-stu-id="4131c-109">Start the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="4131c-110">На вкладке **Файл** выберите пункт **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="4131c-110">Click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="4131c-111">В поле **Совместимость** выберите **Шаблон формы InfoPath 2003**.</span><span class="sxs-lookup"><span data-stu-id="4131c-111">In the **Compatibility** category, select **InfoPath 2003 Editor Form**.</span></span>
    
4. <span data-ttu-id="4131c-112">В разделе **Программирование** выберите категорию либо **C# (совместимый с InfoPath 2003)** или **Visual Basic (совместимый с InfoPath 2003)** в раскрывающемся списке **Язык кода шаблона формы**.</span><span class="sxs-lookup"><span data-stu-id="4131c-112">In the **Programming** category, select either **C# (InfoPath 2003 Compatible)** or **Visual Basic (InfoPath 2003 Compatible)** from the **Form template code language** drop-down list.</span></span> 
    
5. <span data-ttu-id="4131c-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="4131c-113">Click **OK**.</span></span>
    
6. <span data-ttu-id="4131c-114">Создайте шаблон формы, а затем добавьте обработчики событий в Visual Studio 2012, как описано в статье [Добавление обработчика событий с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="4131c-114">Design your form template, and then add event handlers in Visual Studio 2012, as described in [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="4131c-115">См. также</span><span class="sxs-lookup"><span data-stu-id="4131c-115">See also</span></span>



[<span data-ttu-id="4131c-116">Пошаговое руководство. Создание и отладка начального шаблона формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="4131c-116">Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model</span></span>](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[<span data-ttu-id="4131c-117">Создание шаблонов форм с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="4131c-117">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)

