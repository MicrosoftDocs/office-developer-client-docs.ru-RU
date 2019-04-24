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
# <a name="enable-custom-merging-of-infopath-forms"></a>Включение настраиваемого объединения форм InfoPath

The **Merge Forms** feature of the Microsoft InfoPath editor is designed to combine the data from multiple forms into a single form. This is also known as data aggregation. If merging forms is enabled, you can click the **File** tab, click **Save &amp; Send**, click **Merge Forms** under **Import &amp; Link**, and then click the **Merge Forms** button to select one or more forms to merge with the currently opened form. The form that is currently open is the target form and the forms selected in the **Merge Forms** dialog box are known as the source forms.
  
В состав данных, полученных после объединения форм, могут быть включены любые данные, содержащиеся в целевых и исходных формах, или их часть. По умолчанию выполняются следующие действия:
  
- Для повторяющихся элементов данные вставляются в соответствующее расположение в целевом документе. Это происходит в том случае, если атрибут **MaxOccurs** конечного элемента больше 1. 
    
- Для неповторяющихся элементов (то есть для элементов, где **MaxOccurs** равен 1) атрибуты исходных элементов добавляются к существующим атрибутам конечного элемента. 
    
## <a name="creating-a-custom-transform"></a>Создание пользовательского преобразования

Операция по умолчанию при объединении форм лучше всего подходит для форм, основанных на одной схеме XML. В то же время в некоторых случаях может выполняться объединение форм, основанных на различных схемах, или возникнуть необходимость переопределения операции объединения по умолчанию для форм, основанных на одном критерии. В этом случае можно создать преобразование XSL (XSLT), которое содержит указания по объединению. Преобразование применяется в ходе объединения; при этом создается документ DOM, содержащий импортируемую информацию наряду с указаниями по встраиванию этой информации в целевой документ. Эти указания представлены в виде XML-атрибутов пространства имен  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`.
  
XML-атрибуты и их значения выполняют роль указаний по объединению каждого узла с целевым XML-документом. Эти атрибуты описаны в следующих разделах.
  
### <a name="select"></a>select

Атрибут **agg:select** содержит абсолютное выражение XPath, идентифицирующее целевой элемент. 
  
### <a name="insert"></a>insert

Значение insert для атрибута **agg:action** позволяет InfoPath вставить исходный элемент в качестве дочернего элемента для целевого элемента, указанного с помощью атрибута **agg:select**. Дочерние элементы исходного элемента включены в операцию insert. Атрибут **selectChild** позволяет выбрать определенное расположение для операции insert node. Атрибут **order** используется для указания того, вставляются ли исходные элементы до или после существующих целевых элементов. Если атрибут **order** отсутствует, то значение по умолчанию равно after. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="insert" agg:order="before">Some Value</my:field1>

```

### <a name="replace"></a>replace

Значение replace атрибута **agg:action** позволяет InfoPath заменить исходным элементом все целевые элементы, на которые ссылается атрибут **select**. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="replace">Some Value</my:field1>
```

### <a name="mergeattributes"></a>Мержеаттрибутес

Если значение атрибута **agg:action** равно mergeAttributes, то атрибуты исходного элемента объединяются с атрибутами каждого из целевых элементов, на которые ссылается атрибут **select**. 
  
```XML
<my:PMAwS agg:action="mergeAttributes"
 agg:select="/my:Root/my:PMAwS">
```

### <a name="delete"></a>delete

Если значение атрибута **agg:action** равно delete, то из целевого документа будут удалены все целевые элементы, на которые ссылается атрибут **select**. 
  
```XML
<my:field1 agg:select="/my:myFields/my:field1"
 agg:action="delete"/>
```

Наряду с атрибутами, указанными в пространстве имен  `https://schemas.microsoft.com/office/InfoPath/2003/aggregation`, разработчик может использовать пространство имен  `https://schemas.microsoft.com/office/infopath/2003/aggregation-target` для указания XSL объекта, который реализует интерфейс **IXMLDOMDocument**. Одним из наиболее полезных инструментов этого интерфейса является метод **get-documentElement**.
  
### <a name="get-documentelement"></a>Get — documentElement

Функция **target:get-documentElement** предоставляет доступ к объектной модели целевого документа. Она может использоваться для изменения способа объединения в зависимости от содержания целевого документа. 
  
```XML
<xsl:when test="function-available('target:get-documentElement')">
    <xsl:variable name="target" select="target:get-documentElement()" />
    <xsl:if test="not(boolean($target/my:Customer[Name="MyName"]))">
        <my:Customer agg:action="insert" agg:select="/my:MergeForms" />
    </xsl:if>
</xsl:when>

```

## <a name="steps-for-creating-a-custom-merge"></a>Действия по созданию пользовательского объединения

1. Выберите виды исходных XML-документов, данные из которых необходимо объединить. Создайте репрезентативный пример каждого типа исходных документов.
    
2. Создайте схему XML для каждого типа исходных документов XML в существующей форме InfoPath. Для этого необходимо экспортировать схему XML с помощью команды **Экспортировать исходные файлы** на вкладке **Публикация** в Backstage. Для XML-документов, созданных не в InfoPath, можно использовать другие приложения, например Microsoft Visual Studio. Это приложение позволяет создать схему из примера XML-документа. Также пример формы из XML-документа можно создать в InfoPath, а затем экспортировать схему, которая может быть выведена из структуры документа с помощью InfoPath. 
    
3. Определите объединяемые данные в каждом типе исходных документов XML. Выполнение этого действия будет практически полностью зависеть от требований исходной и целевой формы. В некоторых случаях необходимо скопировать все данные из исходной формы, а в других ситуациях может потребоваться только один или несколько элементов из базового XML-документа формы. При определении объединяемых данных необходимо обратить особое внимание на исходный и целевой документы, чтобы элементы обоих форм были логически связаны.
    
4. Создайте преобразование XSL для каждого вида исходного документа XML. Это действие займет основное время при настройке объединения форм. Преобразование XSL служит для преобразования исходного документа XML в формат, который можно объединить с целевой формой. При создании преобразования необходимо сделать выбор между объединением из путей расположения XML и объединением по указаниям объединения InfoPath.
    
    Средство Visual Studio облегчает создание преобразований XSL. Средство Visual Studio выполняет подсветку синтаксиса и структуры документа. Кроме того, при вводе тегов средство автоматически вставляет закрывающие теги в элементы XSL, что позволяет сократить время, затрачиваемое на повторный набор символов и поиск опечаток. Разработчик также может создавать преобразования XSL в текстовом редакторе, например в Блокноте.
    
    Начните с XSL-преобразования identity transform, которое выводит полученный XML-файл:
    
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

    Затем добавьте переопределяющие разделы шаблона для элементов, требующих особой обработки. Например, этот шаблон заменяет элемент  `<src:Task>` на элемент  `<my:field1>` и устанавливает значение атрибута **agg:action** равным replace. 
    
    ```XML
        <xsl:template match="src:Task"> 
            <my:field1 agg:select="/my:myFields/my:field1" agg:action="replace"> 
                <xsl:value-of select="."/> 
            </my:field1> 
        </xsl:template>
    ```

5. Добавьте файлы преобразования XSL и файлы схемы в шаблон формы. После создания производных схем для всех видов исходных документов и преобразования XSL объединения данных InfoPath для всех типов документов добавьте эти компоненты в качестве ресурсов формы. Щелкните элемент **Файлы ресурсов** на вкладке **Данные**, а затем нажмите кнопку **Добавить** в диалоговом окне **Файлы ресурсов**, перейдите к схеме или файлу преобразования XSL, а затем нажмите кнопку **ОК**. Повторите эти действия для всех созданных файлов схемы и преобразований XSL.
    
    Если добавляемые схемы используют атрибут **targetNamespace**, необходимо добавить элемент property в файл формы XSF, чтобы сообщить InfoPath пространство имен схемы. Чтобы обратиться к этому файлу, перейдите на вкладку **Файл**, щелкните элемент **Публикация**, а затем выберите команду **Экспортировать исходные файлы**. Выберите расположение для файлов и нажмите кнопку **ОК**. После этого закройте редактируемый шаблон формы InfoPath.
    
    Перейдите к расположению, указанному для извлеченных файлов, и найдите файл с расширением XSF. Обычно этот файл называется manifest.xsf. Откройте его в Блокноте, найдите тег  `<xsf:file>`, соответствующий схеме, а затем добавьте элемент свойства namespace, чтобы указать пространство имен **targetNamespace**, как показано в следующем примере. 
    
    ```xml
        <xsf:file name="IndvTasks.xsd"> 
            <xsf:fileProperties> 
                <xsf:property name="fileType" type="string" value="Resource" /> 
                <xsf:property name="namespace" type="string" 
                value="urn:office-microsoft-com:InfoPath-designer-aggregation-IndStatusReport" /> 
            </xsf:fileProperties> 
        </xsf:file>
    ```

6. Последним подготовительным действием для обеспечения поддержки пользовательского объединения форм является обновление элемента **importParameters** в XSF-файле, связанном с формой. 

    Найдите тег  `<xsf:importParameters>` в файле XSF. Для каждой созданной для формы схемы/XSL-преобразования добавьте элемент **xsf: импортсаурце** в элемент **xsf: ImportParameters** : `<xsf:importParameters enabled="yes"> <xsf:importSource name="" schema="IndvTasks.xsd" transform="ImportTasks.xsl"></xsf:importSource> </xsf:importParameters>`. 
    
    Атрибут **Name** элемента **xsf: импортсаурце** содержит имя шаблона формы, которое может быть найдено в исходном XML-документе. Это значение обычно можно оставить пустым. Атрибут **schema** содержит имя файла схемы, добавленного к шаблону формы на предыдущем шаге. Атрибут **transform** содержит имя преобразования XSL, которое используется для преобразования форм, соответствующих схеме. 
    
    Настраиваемое преобразование можно использовать как с событием [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) , так и без него. 
    
## <a name="creating-a-custom-merge-in-code"></a>Создание пользовательского объединения в коде

Пользовательское объединение с кодом поддерживается с помощью обработчика события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) и соответствующего атрибута **useScriptHandler** элемента **importParameters** в файле XSF, связанном с формой. 

Для включения события [Merge](https://msdn.microsoft.com/library/Microsoft.Office.InfoPath.FormEvents.Merge.aspx) в управляемом коде необходимо установить флажок **Объединить с использованием пользовательского кода** и нажать кнопку **Изменить** в категории **Дополнительно** диалогового окна **Параметры формы**, которое открывается из Backstage. 
  

