---
title: Включение настраиваемого объединения форм InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: f08f9212-af10-1287-477d-adde7674f523
description: The Merge Forms feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form.
ms.openlocfilehash: 598c44bfe63a31237bf82ceb2212b001fbe7cc1f
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32303726"
---
# <a name="enable-custom-merging-of-infopath-forms"></a><span data-ttu-id="ca8d0-103">Включение настраиваемого объединения форм InfoPath</span><span class="sxs-lookup"><span data-stu-id="ca8d0-103">Enable Custom Merging of InfoPath Forms</span></span>

<span data-ttu-id="ca8d0-p101">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form. This is also known as data aggregation. If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form. The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p101">The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form. This is also known as data aggregation. If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form. The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.</span></span>
  
<span data-ttu-id="ca8d0-p102">В состав данных, полученных после объединения форм, могут быть включены любые данные, содержащиеся в целевых и исходных формах, или их часть. По умолчанию выполняются следующие действия:</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p102">The aggregation of data that results from merging forms can include all of the data that is contained in the source and target forms, or only a portion of the original data. The default operations are the following.</span></span>
  
- <span data-ttu-id="ca8d0-p103">Для повторяющихся элементов данные вставляются в соответствующее расположение в целевом документе. Это происходит в том случае, если атрибут **MaxOccurs** конечного элемента больше 1.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p103">For repeating elements, data is inserted at a matching location in the target document. This happens when the **MaxOccurs** attribute of the destination element is greater than 1.</span></span> 
    
- <span data-ttu-id="ca8d0-112">Для неповторяющихся элементов (то есть для элементов, где **MaxOccurs** равен 1) атрибуты исходных элементов добавляются к существующим атрибутам конечного элемента.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-112">For non-repeating elements (that is, for elements where **MaxOccurs** is "1"), the attributes of the source elements are added to the existing attributes of the destination element.</span></span> 
    
## <a name="creating-a-custom-transform"></a><span data-ttu-id="ca8d0-113">Создание пользовательского преобразования</span><span class="sxs-lookup"><span data-stu-id="ca8d0-113">Creating a Custom Transform</span></span>

<span data-ttu-id="ca8d0-p104">Операция по умолчанию при объединении форм лучше всего подходит для форм, основанных на одной схеме XML. В то же время в некоторых случаях может выполняться объединение форм, основанных на различных схемах, или возникнуть необходимость переопределения операции объединения по умолчанию для форм, основанных на одном критерии. В этом случае можно создать преобразование XSL (XSLT), которое содержит указания по объединению. Преобразование применяется в ходе объединения; при этом создается документ DOM, содержащий импортируемую информацию наряду с указаниями по встраиванию этой информации в целевой документ. Эти указания представлены в виде XML-атрибутов пространства имен  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p104">The default operation when merging forms works well for forms that are based on the same XML schema. In some circumstances, however, you may want to merge forms that are based on different schemas or override the default merge operation for forms that are based on the same schema. For these scenarios, you can create an XSL Transform (XSLT), which contains aggregation instructions for the merge operation. The transform is applied at merge time to create a DOM document that contains the information to be imported, together with annotations specifying how to incorporate this information into the target document. These annotations are XML attributes in the namespace  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.</span></span>
  
<span data-ttu-id="ca8d0-p105">XML-атрибуты и их значения выполняют роль указаний по объединению каждого узла с целевым XML-документом. Эти атрибуты описаны в следующих разделах.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p105">The XML attributes and their values serve as aggregation instructions on how each node is merged with the destination XML document. These attributes are described in the following sections.</span></span>
  
### <a name="select"></a><span data-ttu-id="ca8d0-121">select</span><span class="sxs-lookup"><span data-stu-id="ca8d0-121">select</span></span>

<span data-ttu-id="ca8d0-122">Атрибут **agg:select** содержит абсолютное выражение XPath, идентифицирующее целевой элемент.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-122">The **agg:select** attribute contains an absolute XPath expression which identifies the destination element.</span></span> 
  
### <a name="insert"></a><span data-ttu-id="ca8d0-123">insert</span><span class="sxs-lookup"><span data-stu-id="ca8d0-123">insert</span></span>

<span data-ttu-id="ca8d0-p106">Значение insert для атрибута **agg:action** позволяет InfoPath вставить исходный элемент в качестве дочернего элемента для целевого элемента, указанного с помощью атрибута **agg:select**. Дочерние элементы исходного элемента включены в операцию insert. Атрибут **selectChild** позволяет выбрать определенное расположение для операции insert node. Атрибут **order** используется для указания того, вставляются ли исходные элементы до или после существующих целевых элементов. Если атрибут **order** отсутствует, то значение по умолчанию равно after.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p106">A value of "insert" for the **agg:action** attribute instructs InfoPath to insert the source element as a child of the destination element that is specified by using the **agg:select** attribute. The children of the source element are included in the insert operation. The **selectChild** attribute lets you select a certain location for the insert node operation. The **order** attribute is used to specify whether the source elements are inserted before existing destination elements or after. The default value if the **order** attribute is not present is "after".</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a><span data-ttu-id="ca8d0-129">replace</span><span class="sxs-lookup"><span data-stu-id="ca8d0-129">replace</span></span>

<span data-ttu-id="ca8d0-130">Значение replace атрибута **agg:action** позволяет InfoPath заменить исходным элементом все целевые элементы, на которые ссылается атрибут **select**.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-130">A value of "replace" for the **agg:action** attribute instructs InfoPath to replace each of the destination elements referred to by the **select** attribute with the source element.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a><span data-ttu-id="ca8d0-131">Мержеаттрибутес</span><span class="sxs-lookup"><span data-stu-id="ca8d0-131">mergeAttributes</span></span>

<span data-ttu-id="ca8d0-132">Если значение атрибута **agg:action** равно mergeAttributes, то атрибуты исходного элемента объединяются с атрибутами каждого из целевых элементов, на которые ссылается атрибут **select**.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-132">If the value of the **agg:action** attribute is "mergeAttributes", the attributes of the source element are merged with the attributes of each of the destination elements referred to by the **select** attribute.</span></span> 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a><span data-ttu-id="ca8d0-133">delete</span><span class="sxs-lookup"><span data-stu-id="ca8d0-133">delete</span></span>

<span data-ttu-id="ca8d0-134">Если значение атрибута **agg:action** равно delete, то из целевого документа будут удалены все целевые элементы, на которые ссылается атрибут **select**.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-134">If the value of the **agg:action** attribute is "delete", each of the destination elements referred to by the **select** attribute are deleted from the destination document.</span></span> 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

<span data-ttu-id="ca8d0-p107">Наряду с атрибутами, указанными в пространстве имен  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`, разработчик может использовать пространство имен  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` для указания XSL объекта, который реализует интерфейс **IXMLDOMDocument**. Одним из наиболее полезных инструментов этого интерфейса является метод **get-documentElement**.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p107">In conjunction with the attributes specified in the  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation` namespace, you use the  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` namespace to denote an XSL object that implements the interface **IXMLDOMDocument**. One of the most useful members of this interface is the method **get-documentElement**.</span></span>
  
### <a name="get-documentelement"></a><span data-ttu-id="ca8d0-137">Get — documentElement</span><span class="sxs-lookup"><span data-stu-id="ca8d0-137">get-documentElement</span></span>

<span data-ttu-id="ca8d0-p108">Функция **target:get-documentElement** предоставляет доступ к объектной модели целевого документа. Она может использоваться для изменения способа объединения в зависимости от содержания целевого документа.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p108">The **target:get-documentElement** function provides access to the Document Object Model of the destination document. It can be used to change the way the merge operation works based on the current contents of the destination document.</span></span> 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a><span data-ttu-id="ca8d0-140">Действия по созданию пользовательского объединения</span><span class="sxs-lookup"><span data-stu-id="ca8d0-140">Steps for Creating a Custom Merge</span></span>

1. <span data-ttu-id="ca8d0-p109">Выберите виды исходных XML-документов, данные из которых необходимо объединить. Создайте репрезентативный пример каждого типа исходных документов.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p109">Select the kinds of XML source documents from which you want to merge data. Collect a representative sample of each kind of source document.</span></span>
    
2. <span data-ttu-id="ca8d0-p110">Создайте схему XML для каждого типа исходных документов XML в существующей форме InfoPath. Для этого необходимо экспортировать схему XML с помощью команды **Экспортировать исходные файлы** на вкладке **Публикация** в Backstage. Для XML-документов, созданных не в InfoPath, можно использовать другие приложения, например Microsoft Visual Studio. Это приложение позволяет создать схему из примера XML-документа. Также пример формы из XML-документа можно создать в InfoPath, а затем экспортировать схему, которая может быть выведена из структуры документа с помощью InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p110">Derive the XML schema for each kind of XML source document for an existing InfoPath form. This step is easily accomplished by exporting the XML schema with the **Export Source Files** command on the **Publish** tab of the Backstage. For XML documents that were not created in InfoPath, you can use a tool such as Microsoft Visual Studio to create a schema from the sample XML document, or you can create a sample form from the XML document in InfoPath, and then export the schema that InfoPath derives from the document structure.</span></span> 
    
3. <span data-ttu-id="ca8d0-p111">Определите объединяемые данные в каждом типе исходных документов XML. Выполнение этого действия будет практически полностью зависеть от требований исходной и целевой формы. В некоторых случаях необходимо скопировать все данные из исходной формы, а в других ситуациях может потребоваться только один или несколько элементов из базового XML-документа формы. При определении объединяемых данных необходимо обратить особое внимание на исходный и целевой документы, чтобы элементы обоих форм были логически связаны.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p111">Identify the data that you want to merge from each kind of XML source document. This step will depend almost entirely on the requirements of both your source and destination forms. For some forms, you may want to copy all of the data from the source form. For others, you may want only one or two elements from the form's underlying XML document. When identifying what data that you want to merge, pay extra attention to both the source and destination documents to ensure that the elements map logically between the two forms.</span></span>
    
4. <span data-ttu-id="ca8d0-p112">Создайте преобразование XSL для каждого вида исходного документа XML. Это действие займет основное время при настройке объединения форм. Преобразование XSL служит для преобразования исходного документа XML в формат, который можно объединить с целевой формой. При создании преобразования необходимо сделать выбор между объединением из путей расположения XML и объединением по указаниям объединения InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p112">Create an XSL transform for each kind of XML source document. When configuring the merging of your forms, this step will take the most time. The purpose of the XSL transform is to transform the source XML document into a format that can be merged with the destination form. When designing your transform, decide whether you want to use merging from XML location paths, or merging from InfoPath aggregation instructions.</span></span>
    
    <span data-ttu-id="ca8d0-p113">Средство Visual Studio облегчает создание преобразований XSL. Средство Visual Studio выполняет подсветку синтаксиса и структуры документа. Кроме того, при вводе тегов средство автоматически вставляет закрывающие теги в элементы XSL, что позволяет сократить время, затрачиваемое на повторный набор символов и поиск опечаток. Разработчик также может создавать преобразования XSL в текстовом редакторе, например в Блокноте.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p113">Visual Studio is a convenient tool for creating XSL transforms. Visual Studio provides syntax coloring and a document outline. It also automatically provides closing tags for your XSL elements, which can help decrease redundant typing and hard-to-find spelling errors. You can also create XSL transforms with a text editor such as Notepad.</span></span>
    
    <span data-ttu-id="ca8d0-159">Начните с XSL-преобразования identity transform, которое выводит полученный XML-файл:</span><span class="sxs-lookup"><span data-stu-id="ca8d0-159">Start with the identity transform, which is simply an XSL transform that outputs the same XML file that is input:</span></span>
    
    ```XML
        <?xml version="1.0"?> 
        <xsl:stylesheet version="1.0" xmlns:xsl="https://www.w3.org/1999/XSL/Transform" 
        xmlns:agg="https://schemas.microsoft.com/office/infopath/2003/aggregation" 
        xmlns:target="https://schemas.microsoft.com/office/infopath/2003/aggregation-target" 
        xmlns:my="https://schemas.microsoft.com/office/infopath/2003/myXSD/2003-05-29T20:30:47"> 
            <xsl:template match="/"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
            <xsl:template match="@* | node()"> 
                <xsl:copy> 
                <xsl:apply-templates select="@* | node()" /> 
                </xsl:copy> 
            </xsl:template> 
        </xsl:stylesheet>
    ```

    <span data-ttu-id="ca8d0-p114">Затем добавьте переопределяющие разделы шаблона для элементов, требующих особой обработки. Например, этот шаблон заменяет элемент  `<src:Task>` на элемент  `<my:field1>` и устанавливает значение атрибута **agg:action** равным replace.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p114">Then add overriding template sections for the elements you want to add special handling for. For example, this template changes a  `<src:Task>` element into a  `<my:field1>` element and sets the value of the **agg:action** attribute to "replace".</span></span> 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. <span data-ttu-id="ca8d0-p115">Добавьте файлы преобразования XSL и файлы схемы в шаблон формы. После создания производных схем для всех видов исходных документов и преобразования XSL объединения данных InfoPath для всех типов документов добавьте эти компоненты в качестве ресурсов формы. Щелкните элемент **Файлы ресурсов** на вкладке **Данные**, а затем нажмите кнопку **Добавить** в диалоговом окне **Файлы ресурсов**, перейдите к схеме или файлу преобразования XSL, а затем нажмите кнопку **ОК**. Повторите эти действия для всех созданных файлов схемы и преобразований XSL.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p115">Add the XSL transform files and schema files in the form template. After you have derived schemas for each kind of source document and created an XSL transform to convert each document type so that InfoPath can merge its data, add them to as resources to your form. Click **Resource Files** on the **Data** tab, and then click **Add** in the **Resource Files** dialog box, browse to your schema or XSL transform file, and then click **OK**. Do this to for each schema file and XSL transform file that you created.</span></span>
    
    <span data-ttu-id="ca8d0-p116">Если добавляемые схемы используют атрибут **targetNamespace**, необходимо добавить элемент property в файл формы XSF, чтобы сообщить InfoPath пространство имен схемы. Чтобы обратиться к этому файлу, перейдите на вкладку **Файл**, щелкните элемент **Публикация**, а затем выберите команду **Экспортировать исходные файлы**. Выберите расположение для файлов и нажмите кнопку **ОК**. После этого закройте редактируемый шаблон формы InfoPath.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p116">If the schemas that you add use the **targetNamespace** attribute, you must add a property element to the form's .xsf file so that InfoPath knows the namespace of the schema. To access this file, click the **File** tab, click **Publish**, and then click **Export Source Files**. Select a location for the files, and then click **OK**. Then close the InfoPath form template that you are designing.</span></span>
    
    <span data-ttu-id="ca8d0-p117">Перейдите к расположению, указанному для извлеченных файлов, и найдите файл с расширением XSF. Обычно этот файл называется manifest.xsf. Откройте его в Блокноте, найдите тег  `<xsf:file>`, соответствующий схеме, а затем добавьте элемент свойства namespace, чтобы указать пространство имен **targetNamespace**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-p117">Browse to the location that you specified for the extracted files and find the file that has an .xsf file name extension. Usually, this file is called manifest.xsf. Open the file in Notepad, find the  `<xsf:file>` tag that corresponds to your schema, and add a "namespace" property element to specify the **targetNamespace** as shown in the following example.</span></span> 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. <span data-ttu-id="ca8d0-173">Последним подготовительным действием для обеспечения поддержки пользовательского объединения форм является обновление элемента **importParameters** в XSF-файле, связанном с формой.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-173">The last step in preparing your form to support custom merging is to update the **importParameters** element in the .xsf file associated with the form.</span></span> 

    <span data-ttu-id="ca8d0-174">Найдите тег  `<xsf:importParameters>` в файле XSF.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-174">First, find the  `<xsf:importParameters>` tag in the .xsf file.</span></span> <span data-ttu-id="ca8d0-175">Для каждой созданной для формы схемы/XSL-преобразования добавьте элемент **xsf: импортсаурце** в элемент **xsf: ImportParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-175">For each schema/XSL transform pair you have created for your form, add an **xsf:importSource** element to the **xsf:importParameters** element:  `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`.</span></span> 
    
    <span data-ttu-id="ca8d0-176">Атрибут **Name** элемента **xsf: импортсаурце** содержит имя шаблона формы, которое может быть найдено в исходном XML-документе.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-176">The **name** attribute of the **xsf:importSource** element contains the form template's name that may be found in a source XML document.</span></span> <span data-ttu-id="ca8d0-177">Это значение обычно можно оставить пустым.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-177">Usually, you can leave this empty.</span></span> <span data-ttu-id="ca8d0-178">Атрибут **schema** содержит имя файла схемы, добавленного к шаблону формы на предыдущем шаге.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-178">The **schema** attribute contains the name of a schema file that you added to the form template in the previous step.</span></span> <span data-ttu-id="ca8d0-179">Атрибут **transform** содержит имя преобразования XSL, которое используется для преобразования форм, соответствующих схеме.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-179">Finally, the **transform** attribute contains the name of the XSL transform that you want to use to convert forms that conform to the schema.</span></span> 
    
    <span data-ttu-id="ca8d0-180">Настраиваемое преобразование можно использовать как с событием [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , так и без него.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-180">You can use a custom transform either with the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event or on its own.</span></span> 
    
## <a name="creating-a-custom-merge-in-code"></a><span data-ttu-id="ca8d0-181">Создание пользовательского объединения в коде</span><span class="sxs-lookup"><span data-stu-id="ca8d0-181">Creating a Custom Merge in Code</span></span>

<span data-ttu-id="ca8d0-182">Пользовательское объединение с кодом поддерживается с помощью обработчика события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) и соответствующего атрибута **useScriptHandler** элемента **importParameters** в файле XSF, связанном с формой.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-182">Custom merging with code is supported by using the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event handler, with its corresponding **useScriptHandler** attribute of the **importParameters** element in the .xsf file associated with the form.</span></span> 

<span data-ttu-id="ca8d0-183">Для включения события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в управляемом коде необходимо установить флажок **Объединить с использованием пользовательского кода** и нажать кнопку **Изменить** в категории **Дополнительно** диалогового окна **Параметры формы**, которое открывается из Backstage.</span><span class="sxs-lookup"><span data-stu-id="ca8d0-183">In managed code, you can enable the [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) event by checking the box **Merge using custom code**, and then clicking the **Edit** button, in the **Advanced** category of the **Form Options** dialog box available from the Backstage.</span></span> 
  

