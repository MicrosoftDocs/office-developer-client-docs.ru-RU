---
title: Использование пользовательского XSLT-кода в шаблонах форм InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: 32c80bcd-a5d6-af32-38ba-9ca9ff148b99
description: Большинство элементов представления, необходимых в конструкторе форм Microsoft InfoPath, может быть создано пользователем. Если необходим пользовательский элемент представления, который не может создать InfoPath, можно вручную изменить преобразование XSL (XSLT), используемое InfoPath для создания представления. Чтобы сделать это, извлеките форму в соответствующие файлы компонентов при помощи команды Экспортировать исходные файлы на вкладке Опубликовать приложения Microsoft Office Backstage, далее измените преобразование в предпочитаемом редакторе XML, например Microsoft Visual Studio или Блокноте.
ms.openlocfilehash: a61980191dbedeec33b06ad8173ce50126fea781
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32299905"
---
# <a name="using-custom-xslt-in-infopath-form-templates"></a><span data-ttu-id="ac30f-105">Использование пользовательского XSLT-кода в шаблонах форм InfoPath</span><span class="sxs-lookup"><span data-stu-id="ac30f-105">Using Custom XSLT in InfoPath Form Templates</span></span>

<span data-ttu-id="ac30f-p102">Большинство элементов представления, необходимых в конструкторе форм Microsoft InfoPath, может быть создано пользователем. Если необходим пользовательский элемент представления, который не может создать InfoPath, можно вручную изменить преобразование XSL (XSLT), используемое InfoPath для создания представления. Чтобы сделать это, извлеките форму в соответствующие файлы компонентов при помощи команды **Экспортировать исходные файлы** на вкладке **Опубликовать** приложения Microsoft Office Backstage, далее измените преобразование в предпочитаемом редакторе XML, например Microsoft Visual Studio или Блокноте.</span><span class="sxs-lookup"><span data-stu-id="ac30f-p102">You can create most of the view elements you're likely to need in the Microsoft InfoPath form designer. If you need a custom view element that InfoPath can't create for you, however, you can manually modify the XSL Transformation (XSLT) that InfoPath uses to generate the view. To do so, extract the form into its component files by using **Export Source Files** on the **Publish** tab of the Microsoft Office Backstage, and then edit the transform in your preferred XML editor, such as Microsoft Visual Studio or Notepad.</span></span> 
  
<span data-ttu-id="ac30f-p103">Если изменить преобразования представлений вне InfoPath, а затем открыть представление в режиме конструктора и внести изменения, InfoPath перезапишет изменения, сделанные вручную. Чтобы приложение InfoPath не перезаписывало сделанные изменения, их необходимо помещать в элемент преобразования  `<xsl:template>` и использовать режим  `xd:preserve` следующим образом:</span><span class="sxs-lookup"><span data-stu-id="ac30f-p103">If you make changes to a view transform outside of InfoPath and then open the view in design mode and make changes, InfoPath will overwrite the changes you made manually. To keep InfoPath from overwriting the changes you make, you must place those changes in an  `<xsl:template>` element in the transform and use the  `xd:preserve` mode, as shown here:</span></span> 
  
```XML
<xsl:template match="my:field1" mode="xd:preserve"> 
   <div> 
      The value of field1 is <xsl:value-of select="."/> 
   </div> 
</xsl:template>
```

<span data-ttu-id="ac30f-111">Чтобы включить шаблон в преобразованный файл, используйте элемент  `<xsl:apply-templates>` в том же режиме  `xd:preserve`:</span><span class="sxs-lookup"><span data-stu-id="ac30f-111">To include the template in the transformed file, use the  `<xsl:apply-templates>` element with the same  `xd:preserve` mode:</span></span> 
  
```XML
<xsl:apply-templates select="my:field1" mode="xd:preserve"/>
```

<span data-ttu-id="ac30f-p104">Элементы и конструкторы, заданные в шаблонах XSL в режиме  `xd:preserve`, не будут отображаться в среде разработки InfoPath. InfoPath будет отмечать настраиваемый раздел элементом управления с надписью **Защитить блок кода** и красной границей. При открытии формы для заполнения пользовательские преобразования XSL применяются и элементы управления **Защитить блок кода** не отображаются.</span><span class="sxs-lookup"><span data-stu-id="ac30f-p104">Elements and constructs defined within XSL templates with the  `xd:preserve` mode will not be displayed in the InfoPath design environment. Instead, InfoPath will mark the custom section with a control labeled **Preserve Code Block** with a red border. When a user opens the form to fill it out, the custom XSL transforms are applied and the **Preserve Code Block** controls will not appear.</span></span> 
  

