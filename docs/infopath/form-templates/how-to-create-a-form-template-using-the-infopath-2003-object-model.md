---
title: Создание шаблона формы с помощью объектной модели InfoPath 2003
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- Создание шаблонов форм с поддержкой веб-2003 InfoPath, шаблонов форм [InfoPath 2007], совместимого с InfoPath 2003, InfoPath 2007, создание шаблонов форм совместимых с InfoPath 2003
localization_priority: Normal
ms.assetid: c746aeb1-902c-440e-830b-5b9efad0ca04
description: В главе описаны действия, необходимые для создания шаблона формы, работающего с объектной моделью, совместимой с InfoPath 2003.
ms.openlocfilehash: 0cea526c2d41674afc6fee152c3e0584e6b69564
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807491"
---
# <a name="create-a-form-template-using-the-infopath-2003-object-model"></a><span data-ttu-id="449f4-104">Создание шаблона формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="449f4-104">Create a Form Template Using the InfoPath 2003 Object Model</span></span>

<span data-ttu-id="449f4-105">В главе описаны действия, необходимые для создания шаблона формы, работающего с объектной моделью, совместимой с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="449f4-105">The procedures in this topic describe how to create a form template that works with the InfoPath 2003-compatible object model.</span></span>
  
> [!IMPORTANT]
> <span data-ttu-id="449f4-106">Помимо приведенных ниже процедур необходимо также перейдите на вкладку **файл** , выберите команду **Сохранить как**и затем выберите **Шаблон формы InfoPath 2003** в поле **Тип файла** , чтобы сохранить шаблон формы в формат файлов совместимых с InfoPath 2003.</span><span class="sxs-lookup"><span data-stu-id="449f4-106">In addition to the procedures below, you must also click the **File** tab, click **Save As**, and then select **InfoPath 2003 Form Template** in the **Save as type** box to save the form template to the InfoPath 2003-compatible file format.</span></span> <span data-ttu-id="449f4-107">Кроме того чтобы открыть шаблоны форм совместимых с InfoPath 2003, созданных с помощью InfoPath, все пользователи InfoPath 2003 необходимо .NET Framework 2.0 или более поздней версии на своих компьютерах.</span><span class="sxs-lookup"><span data-stu-id="449f4-107">Also, to open InfoPath 2003-compatible form templates created with InfoPath, all InfoPath 2003 users must have the .NET Framework 2.0 or later installed on their computers.</span></span> 
  
### <a name="to-create-an-infopath-2003-compatible-form-template-in-infopath-with-visual-studio-tools-for-applications"></a><span data-ttu-id="449f4-108">Создание шаблона формы, совместимого с InfoPath 2003, в InfoPath с набором средств Visual Studio Tools для работы с приложениями</span><span class="sxs-lookup"><span data-stu-id="449f4-108">To create an InfoPath 2003-compatible form template in InfoPath with Visual Studio Tools for Applications</span></span>

1. <span data-ttu-id="449f4-109">Запустите конструктор InfoPath.</span><span class="sxs-lookup"><span data-stu-id="449f4-109">Start the InfoPath Designer.</span></span>
    
2. <span data-ttu-id="449f4-110">Перейдите на вкладку **файл** и выберите пункт **Параметры формы**.</span><span class="sxs-lookup"><span data-stu-id="449f4-110">Click the **File** tab, and then click **Form Options**.</span></span>
    
3. <span data-ttu-id="449f4-111">В **поле совместимость** выберите **Шаблон формы InfoPath 2003**.</span><span class="sxs-lookup"><span data-stu-id="449f4-111">In the **Compatibility** category, select **InfoPath 2003 Editor Form**.</span></span>
    
4. <span data-ttu-id="449f4-112">В разделе **программирование** Категория выберите **C# (совместимый с InfoPath 2003)** или **Visual Basic (совместимый с InfoPath 2003)** из раскрывающегося списка **язык кода шаблона формы** .</span><span class="sxs-lookup"><span data-stu-id="449f4-112">In the **Programming** category, select either **C# (InfoPath 2003 Compatible)** or **Visual Basic (InfoPath 2003 Compatible)** from the **Form template code language** drop-down list.</span></span> 
    
5. <span data-ttu-id="449f4-113">Нажмите кнопку **ОК**.</span><span class="sxs-lookup"><span data-stu-id="449f4-113">Click **OK**.</span></span>
    
6. <span data-ttu-id="449f4-114">Создание шаблона формы и добавление обработчиков событий в Visual Studio 2012, как описано в диалоговом окне [Добавить события обработчик с помощью объектной модели InfoPath 2003](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span><span class="sxs-lookup"><span data-stu-id="449f4-114">Design your form template, and then add event handlers in Visual Studio 2012, as described in [Add an Event Handler Using the InfoPath 2003 Object Model](how-to-add-an-event-handler-using-the-infopath-2003-object-model.md).</span></span>
    
## <a name="see-also"></a><span data-ttu-id="449f4-115">См. также</span><span class="sxs-lookup"><span data-stu-id="449f4-115">See also</span></span>



[<span data-ttu-id="449f4-116">Пошаговое руководство. Создание и отладка начального шаблона формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="449f4-116">Walkthrough: Creating and Debugging a Basic Form Template Using the InfoPath 2003 Object Model</span></span>](walkthrough-create-and-debug-basic-form-template-using-infopath-object-model.md)
  
[<span data-ttu-id="449f4-117">Создание шаблонов форм, использующих объектную модель InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="449f4-117">Creating Form Templates Using the InfoPath 2003 Object Model</span></span>](creating-form-templates-using-the-infopath-2003-object-model.md)

