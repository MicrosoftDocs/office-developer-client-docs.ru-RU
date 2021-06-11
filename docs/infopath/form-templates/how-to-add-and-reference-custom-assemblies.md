---
title: Добавление и ссылка настраиваемые сборки
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
keywords:
- infopath 2003-compatible form templates, using custom assemblies,assemblies [InfoPath 2007], adding custom using InfoPath 2003 object model
localization_priority: Normal
ms.assetid: 20e1f43e-8279-48fc-8f34-16a2729dbc9b
description: Если в проект шаблона формы с управляемым кодом добавляется ссылка на пользовательскую сборку, то при компиляции и публикации проекта эта сборка включается в файл шаблона формы (XSN-файл).
ms.openlocfilehash: 19b5f06231bb03cfac8b32b157e03956b5fc334e
ms.sourcegitcommit: 8657170d071f9bcf680aba50b9c07f2a4fb82283
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/28/2019
ms.locfileid: "33431171"
---
# <a name="add-and-reference-custom-assemblies"></a><span data-ttu-id="a0dc9-104">Добавление и ссылка настраиваемые сборки</span><span class="sxs-lookup"><span data-stu-id="a0dc9-104">Add and Reference Custom Assemblies</span></span>

<span data-ttu-id="a0dc9-105">Если в проект шаблона формы с управляемым кодом добавляется ссылка на пользовательскую сборку, то при компиляции и публикации проекта эта сборка включается в файл шаблона формы (XSN-файл).</span><span class="sxs-lookup"><span data-stu-id="a0dc9-105">When you add a reference to a custom assembly in a managed-code form template project, that assembly is included within the form template file (.xsn) when your project is compiled and published.</span></span>
  
## <a name="add-and-reference-a-custom-assembly"></a><span data-ttu-id="a0dc9-106">Добавление пользовательской сборки и ссылки на нее</span><span class="sxs-lookup"><span data-stu-id="a0dc9-106">Add and Reference a Custom Assembly</span></span>

<span data-ttu-id="a0dc9-107">Чтобы избежать конфликта с процессом управления системой проектов InfoPath файлами, добавляемыми в файл шаблона формы, не копируйте пользовательские сборки, на которые требуется указать ссылки, в папку верхнего уровня проекта шаблона формы.</span><span class="sxs-lookup"><span data-stu-id="a0dc9-107">To avoid a conflict with how the InfoPath project system manages files that are added to the form template file, do not copy any custom assemblies that you want to reference into the top-level folder of a form template project.</span></span> <span data-ttu-id="a0dc9-108">По умолчанию это будет путь в следующем формате:  < диск >:\Users\ *UserName* \Documents\InfoPath Projects\ *ProjectName*</span><span class="sxs-lookup"><span data-stu-id="a0dc9-108">By default, this will be a path in the following format: < *drive*  >:\Users\  *UserName*  \Documents\InfoPath Projects\  *ProjectName*</span></span> 
  
<span data-ttu-id="a0dc9-p102">Если требуется переместить настраиваемые сборки, на которые требуется указать ссылки, внутри папки проекта, то следует создать вложенную папку в главной папке проекта, скопировать настраиваемые сборки в эту вложенную папку и указать соответствующие ссылки на эту папку. Однако обратите внимание, что создавать вложенную папку для сборок, на которые добавлены ссылки, необязательно. Если такая сборка не расположена в папке верхнего уровня проекта, система проектов InfoPath скопирует сборку в файл шаблона формы (XSN-файл) при компиляции и публикации проекта.</span><span class="sxs-lookup"><span data-stu-id="a0dc9-p102">If you do want to move custom assemblies that you reference to a location within the project folder, you must create a subfolder under the main project folder, and then copy and reference custom assemblies from that subfolder. However, be aware that creating a subfolder for referenced assemblies is not necessary. As long as a referenced assembly is not located within the project's top-level folder, the InfoPath project system will copy the assembly into the form template file (.xsn) when the project is compiled and published.</span></span>
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a><span data-ttu-id="a0dc9-112">Добавление ссылки на пользовательскую сборку, расположенную в папке по умолчанию</span><span class="sxs-lookup"><span data-stu-id="a0dc9-112">Reference a custom assembly from its default location</span></span>

1. <span data-ttu-id="a0dc9-113">Откройте проект шаблона формы в наборе Visual Studio 2012.</span><span class="sxs-lookup"><span data-stu-id="a0dc9-113">Open the form template project in Visual Studio 2012.</span></span>
    
2. <span data-ttu-id="a0dc9-114">В меню **Проект** выберите пункт **Добавить ссылку**.</span><span class="sxs-lookup"><span data-stu-id="a0dc9-114">On the **Project** menu, click **Add Reference**.</span></span>
    
3. <span data-ttu-id="a0dc9-115">Найдите и укажите сборку на вкладке **Обзор**, после чего нажмите кнопку **ОК**, чтобы добавить ссылку.</span><span class="sxs-lookup"><span data-stu-id="a0dc9-115">Click the **Browse** tab, locate and specify the assembly, and then click **OK** to add the reference.</span></span> 
    
## <a name="see-also"></a><span data-ttu-id="a0dc9-116">См. также</span><span class="sxs-lookup"><span data-stu-id="a0dc9-116">See also</span></span>

#### <a name="tasks"></a><span data-ttu-id="a0dc9-117">Задачи</span><span class="sxs-lookup"><span data-stu-id="a0dc9-117">Tasks</span></span>

[<span data-ttu-id="a0dc9-118">Создание шаблона формы с помощью объектной модели InfoPath 2003</span><span class="sxs-lookup"><span data-stu-id="a0dc9-118">Create a Form Template Using the InfoPath 2003 Object Model</span></span>](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

