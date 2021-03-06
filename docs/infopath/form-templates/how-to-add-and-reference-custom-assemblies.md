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
# <a name="add-and-reference-custom-assemblies"></a>Добавление и ссылка настраиваемые сборки

Если в проект шаблона формы с управляемым кодом добавляется ссылка на пользовательскую сборку, то при компиляции и публикации проекта эта сборка включается в файл шаблона формы (XSN-файл).
  
## <a name="add-and-reference-a-custom-assembly"></a>Добавление пользовательской сборки и ссылки на нее

Чтобы избежать конфликта с процессом управления системой проектов InfoPath файлами, добавляемыми в файл шаблона формы, не копируйте пользовательские сборки, на которые требуется указать ссылки, в папку верхнего уровня проекта шаблона формы. По умолчанию это будет путь в следующем формате:  < диск >:\Users\ *UserName* \Documents\InfoPath Projects\ *ProjectName* 
  
Если требуется переместить настраиваемые сборки, на которые требуется указать ссылки, внутри папки проекта, то следует создать вложенную папку в главной папке проекта, скопировать настраиваемые сборки в эту вложенную папку и указать соответствующие ссылки на эту папку. Однако обратите внимание, что создавать вложенную папку для сборок, на которые добавлены ссылки, необязательно. Если такая сборка не расположена в папке верхнего уровня проекта, система проектов InfoPath скопирует сборку в файл шаблона формы (XSN-файл) при компиляции и публикации проекта.
  
### <a name="reference-a-custom-assembly-from-its-default-location"></a>Добавление ссылки на пользовательскую сборку, расположенную в папке по умолчанию

1. Откройте проект шаблона формы в наборе Visual Studio 2012.
    
2. В меню **Проект** выберите пункт **Добавить ссылку**.
    
3. Найдите и укажите сборку на вкладке **Обзор**, после чего нажмите кнопку **ОК**, чтобы добавить ссылку. 
    
## <a name="see-also"></a>См. также

#### <a name="tasks"></a>Задачи

[Создание шаблона формы с помощью объектной модели InfoPath 2003](how-to-create-a-form-template-using-the-infopath-2003-object-model.md)

