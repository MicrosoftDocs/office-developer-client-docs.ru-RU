---
title: Работа с XML-схемами в InfoPath
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
localization_priority: Normal
ms.assetid: c1d70e9f-b9fc-7bdb-107e-d0cd8191607b
description: В шаблоне формы, создаваемом с помощью Microsoft InfoPath, схема XML (XSD) используется для выполнения проверки данных в XML, который представляет вводные, отредактированные и выводные данные из формы InfoPath. Каждый шаблон формы, созданный в конструкторе форм InfoPath, содержит как минимум один файл схемы XSD (XSD), используемый для проверки во время выполнения.
ms.openlocfilehash: 6921a2206c098992a0a24e85c263992a0e2c98b1
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19807615"
---
# <a name="working-with-xml-schemas-in-infopath"></a><span data-ttu-id="e430a-104">Работа с XML-схемами в InfoPath</span><span class="sxs-lookup"><span data-stu-id="e430a-104">Working with XML Schemas in InfoPath</span></span>

<span data-ttu-id="e430a-p102">В шаблоне формы, создаваемом с помощью Microsoft InfoPath, схема XML (XSD) используется для выполнения проверки данных в XML, который представляет вводные, отредактированные и выводные данные из формы InfoPath. Каждый шаблон формы, созданный в конструкторе форм InfoPath, содержит как минимум один файл схемы XSD (XSD), используемый для проверки во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e430a-p102">A form template that you create with Microsoft InfoPath uses an XML Schema (XSD) to perform structural and data validation on the XML that is input, edited, and output from an InfoPath form. Every form template created in the InfoPath form designer contains at least one XSD schema file (.xsd) that is used for validation at run time.</span></span>
  
> [!NOTE]
> <span data-ttu-id="e430a-p103">Содержащиеся в данной статье сведения предназначены для шаблонов форм, разработанных для использования в редакторе InfoPath. Совместимые с браузером шаблоны форм имеют более строгие требования к схемам XSD. Дополнительные сведения см. в документации о схемах XML в совместимых с браузером шаблонах форм, доступной на веб-сайте MSDN.</span><span class="sxs-lookup"><span data-stu-id="e430a-p103">The information contained in this topic applies to form templates designed for use in the InfoPath editor. Browser-compatible form templates have stricter XSD Schema requirements. For more information, see the documentation about XML Schemas in browser-compatible form templates available on MSDN.</span></span> 
  
## <a name="using-externally-authored-xml-schemas"></a><span data-ttu-id="e430a-110">Использование созданных во внешней среде схем XML</span><span class="sxs-lookup"><span data-stu-id="e430a-110">Using Externally-authored XML Schemas</span></span>

<span data-ttu-id="e430a-111">Чтобы загрузить файл схемы XSD, созданный вне приложения InfoPath, выполните следующие действия.</span><span class="sxs-lookup"><span data-stu-id="e430a-111">To load an XSD schema file that was authored outside of InfoPath, follow these steps.</span></span>
  
### <a name="to-create-a-form-template-based-on-an-external-schema"></a><span data-ttu-id="e430a-112">Создание шаблона формы на основе внешней схемы</span><span class="sxs-lookup"><span data-stu-id="e430a-112">To create a form template based on an external schema</span></span>

1. <span data-ttu-id="e430a-113">В Backstage, нажмите **Создать**, щелкните **XML или схему** в разделе **Дополнительные шаблоны форм**, а затем нажмите **Создать форму**.</span><span class="sxs-lookup"><span data-stu-id="e430a-113">In the Backstage, click **New**, click **XML or Schema** under **Advanced Form Templates**, and then click **Design This Form**.</span></span>
    
2. <span data-ttu-id="e430a-114">В **мастере источника данных**, укажите нужный файл схемы XSD, а затем нажмите кнопку **Далее** и следуйте инструкциям на оставшихся страницах мастера.</span><span class="sxs-lookup"><span data-stu-id="e430a-114">In the **Data Source Wizard**, specify the XSD schema file you want to use, and then click **Next** and complete the remaining pages of the wizard.</span></span> 
    
## <a name="unsupported-xsd-constructs"></a><span data-ttu-id="e430a-115">Неподдерживаемые конструкции XSD</span><span class="sxs-lookup"><span data-stu-id="e430a-115">Unsupported XSD Constructs</span></span>

<span data-ttu-id="e430a-p104">В следующих разделах описываются конструкции XSD, которые приложение InfoPath не может обрабатывать во время выполнения. Создавая шаблоны форм в конструкторе форм InfoPath, этих конструкций рекомендуется избегать.</span><span class="sxs-lookup"><span data-stu-id="e430a-p104">The following sections describe XSD constructs that InfoPath cannot handle at run time. Avoid these constructs when creating a form template in the InfoPath form designer.</span></span>
  
## <a name="entity-and-entities-types"></a><span data-ttu-id="e430a-118">Типы ENTITY и ENTITIES</span><span class="sxs-lookup"><span data-stu-id="e430a-118">ENTITY and ENTITIES Types</span></span>

<span data-ttu-id="e430a-p105">Для типов **ENTITY** и **ENTITIES** требуется определение типа документа (DTD), которое не поддерживается в InfoPath. В InfoPath не допускается разработка шаблона формы по такой схеме и выводится сообщение об ошибке с рекомендацией изменить тип **ENTITY** на тип **NCName**, производным которого является **ENTITY**.</span><span class="sxs-lookup"><span data-stu-id="e430a-p105">The **ENTITY** and **ENTITIES** types require a document type definition (DTD) for validation, which InfoPath does not support. InfoPath does not allow you to design a form template against such a schema and displays an error message that recommends changing the **ENTITY** type to the **NCName** type from which **ENTITY** derives.</span></span> 
  
> [!NOTE]
>  <span data-ttu-id="e430a-121">Если шаблон формы InfoPath создается вручную не в режиме конструктора и в этом шаблоне используется XSD с типами **ENTITY** и **ENTITIES**, шаблон формы может работать во время выполнения в случае, если файл Template.xml содержит необходимый DTD для этих типов.</span><span class="sxs-lookup"><span data-stu-id="e430a-121">If you manually author an InfoPath form template outside of design mode, and it uses an XSD that includes **ENTITY** and **ENTITIES** types, the form template may work at run time if the Template.xml file contains the required DTD for these types.</span></span> 
  
## <a name="required-xsdany-element"></a><span data-ttu-id="e430a-122">Обязательный элемент "xsd:any"</span><span class="sxs-lookup"><span data-stu-id="e430a-122">Required xsd:any Element</span></span>

<span data-ttu-id="e430a-p106">Экземпляр элемента подстановочного знака **xsd:any**, то есть экземпляр элемента **xsd:any** со значением атрибута **minOccurs** больше нуля ("required any"), запрещает детерминированное создание в InfoPath допустимого экземпляра для данного фрагмента схемы. При генерировании формы, использующей этот фрагмент схемы, в приложении InfoPath должна быть возможность создания допустимого экземпляра. Выполняя действия в **мастере источника данных**, при работе со схемами, имеющими обязательные элементы **xsd:any**, потребуется выбрать элемент схемы, который будет использоваться вместо обязательного элемента **xsd:any**.</span><span class="sxs-lookup"><span data-stu-id="e430a-p106">An occurrence of an **xsd:any** wildcard element, that is, an occurrence of an **xsd:any** element with a **minOccurs** attribute value greater than zero ("required any"), prevents InfoPath from deterministically creating a valid instance for this schema fragment. InfoPath must be able to create a valid instance when generating a form that uses this schema fragment. As part of running the **Data Source Wizard**, schemas with required **xsd:any** elements require you to choose which schema element you want to use in place of the required **xsd:any** element.</span></span> 
  
## <a name="elements-with-an-abstract-complex-type"></a><span data-ttu-id="e430a-126">Элементы абстрактного сложного типа</span><span class="sxs-lookup"><span data-stu-id="e430a-126">Elements with an Abstract Complex Type</span></span>

<span data-ttu-id="e430a-p107">Режим конструктора InfoPath поддерживает разработку шаблона формы в схемах, использующих абстрактные сложные типы. Например, если у элемента с именем  `shippingAddress` есть абстрактный сложный тип с именем  `address`, имеющий две производные,   `USAddress` и  `CanadianAddress`  InfoPath принимает любой экземпляр  `shippingAddress` в качестве выбора между  `shippingAddress` с типом  `USAddress` и  `shippingAddress` с типом  `CanadianAddress`. В этом примере, если указанные схемы не содержат типов, производных от адреса, InfoPath запрашивает дополнительную схему, удовлетворяющую данному требованию.</span><span class="sxs-lookup"><span data-stu-id="e430a-p107">InfoPath design mode supports designing a form template against schemas that use abstract complex types. For example, if an element named  `shippingAddress` has an abstract complex type named  `address` that has two derivations,  `USAddress` and  `CanadianAddress`, InfoPath treats any instance of  `shippingAddress` as a choice between  `shippingAddress` with type  `USAddress` and  `shippingAddress` with type  `CanadianAddress` . In this example, if the provided schemas contain no types that derive from address, then InfoPath requests an additional schema that fulfills this requirement.</span></span> 
  
## <a name="xsd-constructs-with-reduced-functionality"></a><span data-ttu-id="e430a-130">Конструкции XSD с ограниченной функциональностью</span><span class="sxs-lookup"><span data-stu-id="e430a-130">XSD Constructs with Reduced Functionality</span></span>

<span data-ttu-id="e430a-131">В следующем разделе описаны конструкции XSD, функциональность которых ограничивается при использовании для создания шаблона формы в конструкторе форм InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e430a-131">The following sections describe XSD constructs that have reduced functionality when used to create a form template in the InfoPath form designer.</span></span>
  
## <a name="substitution-groups"></a><span data-ttu-id="e430a-132">Группы подстановки</span><span class="sxs-lookup"><span data-stu-id="e430a-132">Substitution Groups</span></span>

<span data-ttu-id="e430a-p108">Все элементы группы подстановки отображаются в области задач **Поля**. В приложении InfoPath возможности подстановки представлены в виде варианта всех групп подстановки (включая определяющий элемент (если он не является абстрактным)). Если для абстрактного элемента группы подстановки отсутствуют, InfoPath выведет запрос на предоставление схемы, содержащей хотя бы один элемент, который является группой подстановки.</span><span class="sxs-lookup"><span data-stu-id="e430a-p108">All members of the substitution group appear in the **Fields** task pane. InfoPath represents the substitution possibilities as a choice of all the substitution groups (including the defining element, if it is not abstract). If there are no substitution groups for an abstract element, InfoPath prompts you to provide a schema that contains at least one element that is a substitution group.</span></span> 
  
## <a name="unbounded-choice-elements"></a><span data-ttu-id="e430a-136">Неограниченные элементы выбора</span><span class="sxs-lookup"><span data-stu-id="e430a-136">Unbounded Choice Elements</span></span>

<span data-ttu-id="e430a-137">В следующем фрагменте схемы представлен неограниченный элемент выбора:</span><span class="sxs-lookup"><span data-stu-id="e430a-137">The following schema fragment shows an unbounded choice element:</span></span>
  
```XML
<xsd:choice maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2"/> 
</xsd:choice> 

```

<span data-ttu-id="e430a-p109">В приложении InfoPath повторяющиеся элементы выбора отображаются в виде повторяющихся вариантов в области задач **Поля**. Элемент управления **Повторяющаяся группа выбора** можно использовать для представления разнородного списка, определенного повторяющимся элементом выбора в XSD.</span><span class="sxs-lookup"><span data-stu-id="e430a-p109">InfoPath displays repeating choice elements as repeating choices in the **Fields** task pane. There is a **Repeating Choice Group** control that you can use to represent the heterogeneous list defined by the repeating choice element in the XSD.</span></span> 
  
## <a name="repeating-sequence"></a><span data-ttu-id="e430a-140">Повторяющаяся последовательность</span><span class="sxs-lookup"><span data-stu-id="e430a-140">Repeating Sequence</span></span>

<span data-ttu-id="e430a-141">В следующем фрагменте схемы представлена повторяющаяся последовательность:</span><span class="sxs-lookup"><span data-stu-id="e430a-141">The following schema fragment shows a repeating sequence:</span></span>
  
```XML
<xsd:sequence maxOccurs="unbounded"> 
    <xsd:element name="my_element_1"/> 
    <xsd:element name="my_element_2" minOccurs="0"/> 
</xsd:sequence> 

```

<span data-ttu-id="e430a-142">До тех пор пока в повторяющейся последовательности будет находиться необходимый элемент, приложение InfoPath будет загружать XSD без изменений, позволяя выполнять привязку элементов управления повторяющегося раздела к повторяющейся последовательности.</span><span class="sxs-lookup"><span data-stu-id="e430a-142">As long as the repeating sequence contains a required element, InfoPath loads the XSD without modifying it and allows you to bind repeating section controls to the repeating sequence.</span></span>
  
## <a name="choice-of-model-groups"></a><span data-ttu-id="e430a-143">Выбор групп моделей</span><span class="sxs-lookup"><span data-stu-id="e430a-143">Choice of Model Groups</span></span>

<span data-ttu-id="e430a-144">В следующем фрагменте схемы представлен элемент выбора, содержащий несколько групп моделей:</span><span class="sxs-lookup"><span data-stu-id="e430a-144">The following schema fragment shows the choice element containing several model groups:</span></span>
  
```XML
<xsd:choice> 
    <xsd:element name="my_element_1"/> 
    <xsd:sequence> 
        <xsd:element name="my_element_2"/> 
        <xsd:element name="my_element_3"/> 
    </xsd:sequence> 
</xsd:choice> 

```

<span data-ttu-id="e430a-p110">Режим конструктора InfoPath поддерживает такие конструкции XSD без внесения изменений со стороны конструктора форм. Приложение InfoPath не изменяет значение схемы и упрощает указанную выше конструкцию выбора до эквивалентного свернутого одного варианта в области задач **Поля**.</span><span class="sxs-lookup"><span data-stu-id="e430a-p110">InfoPath design mode supports such XSD constructs without requiring any modification by the form designer. While InfoPath does not modify the meaning of the schema, it simplifies the choice construct above into an equivalent collapsed single choice in the **Fields** task pane.</span></span> 
  
## <a name="optional-sibling-with-same-qualified-name"></a><span data-ttu-id="e430a-147">Необязательный элемент того же уровня с тем же классифицированным именем</span><span class="sxs-lookup"><span data-stu-id="e430a-147">Optional Sibling with Same Qualified Name</span></span>

<span data-ttu-id="e430a-148">В следующем фрагменте схемы представлен необязательный элемент того же уровня с тем же классифицированным именем (`QName`):</span><span class="sxs-lookup"><span data-stu-id="e430a-148">The following schema fragment shows an optional sibling with same qualified name (QName`QName`):</span></span>
  
```xml
<xsd:sequence> 
    <xsd:element name="my_element_1" minOccurs="0"/> 
    <xsd:element name="my_element_2"/> 
            <xsd:element name="my_element_1"/> 
</xsd:sequence> 

```

<span data-ttu-id="e430a-p111">Выражения **XPath** для этих узлов могут быть сложными, поскольку в конструкторе форм InfoPath необходимо принимать во внимание каждый возможный экземпляр XML. InfoPath не открывает части схемы, для которых создание правильных привязок **XPath** может быть затруднительным. О пропущенных разделах схемы выводятся соответствующие предупреждения.</span><span class="sxs-lookup"><span data-stu-id="e430a-p111">**XPath** expressions for these nodes can be complex because every potential XML instance must be accounted for in the InfoPath form designer. InfoPath does not expose parts of the schema for which it may have difficulty creating correct **XPath** bindings. Warnings appear regarding the portions of the schema that are ignored.</span></span> 
  
## <a name="xsd-constructs-with-special-meaning-in-infopath"></a><span data-ttu-id="e430a-152">Конструкции XSD, имеющие особое значение в InfoPath</span><span class="sxs-lookup"><span data-stu-id="e430a-152">XSD Constructs with Special Meaning in InfoPath</span></span>

<span data-ttu-id="e430a-p112">В следующих разделах описываются конструкции XSD, имеющие особое значение при использовании для создания шаблона формы в режиме конструктора. В этих разделах рассказывается о принципах использования таких конструкций в схемах для активации различных типов поведений.</span><span class="sxs-lookup"><span data-stu-id="e430a-p112">The following sections describe XSD constructs that have special meaning when used in creating a form template in design mode. These sections describe how you can use the constructs in your schema to enable certain behaviors.</span></span>
  
## <a name="adding-new-element-fields-and-groups-with-the-fields-task-pane"></a><span data-ttu-id="e430a-155">Добавление новых полей и групп элементов с помощью области задач "Поля"</span><span class="sxs-lookup"><span data-stu-id="e430a-155">Adding New Element Fields and Groups with the Fields Task Pane</span></span>

<span data-ttu-id="e430a-p113">Схему можно построить так, чтобы использовать область задач **Поля** для добавления новых полей и групп элементов во время разработки. Для этого элемент в схеме необходимо объявить с помощью дополнительного неограниченного элемента **xsd:any**, который указывает атрибут пространства имен с подстановочным знаком **##any**. Затем в режиме конструктора можно использовать область задач **Поля** для добавления к элементу новых полей и групп. Например, новый контент можно добавить к следующему элементу.</span><span class="sxs-lookup"><span data-stu-id="e430a-p113">You can construct your schema so that you can use the **Fields** task pane to add new element fields and groups to an element at design time. To do so, you declare an element in your schema with an optional, unbounded **xsd:any** element that specifies the namespace attribute with the **##any** wildcard. Then, in design mode, you can use the **Fields** task pane to add new element fields and groups to that element. For example, you could add new content to the following element:</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
         <xsd:sequence> 
             <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="##any"processContents="lax"/> 
         </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="adding-new-attribute-fields-with-the-fields-task-pane"></a><span data-ttu-id="e430a-160">Добавление новых полей атрибута с помощью области задач "Поля"</span><span class="sxs-lookup"><span data-stu-id="e430a-160">Adding New Attribute Fields with the Fields Task Pane</span></span>

<span data-ttu-id="e430a-p114">Так же как и в случае с элементом, разработчик может объявить атрибут с элементом **anyAttribute** с атрибутом пространства имен в виде подстановочного знака **##any**. Во время разработки область задач **Поля** используется для добавления нового контента к этому атрибуту схемы.</span><span class="sxs-lookup"><span data-stu-id="e430a-p114">Similarly to the element case, you can declare an attribute with an **anyAttribute** element that has the namespace attribute specified as the **##any** wildcard. At design time, you can use the **Fields** task pane to add new content to that schema attribute.</span></span> 
  
```XML
<xsd:element name="open"> 
    <xsd:complexType> 
        <xsd:anyAttribute namespace="##any" processContents="lax"/> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="storing-xml-signatures-in-the-data-source"></a><span data-ttu-id="e430a-163">Хранение подписей XML в источнике данных</span><span class="sxs-lookup"><span data-stu-id="e430a-163">Storing XML Signatures in the Data Source</span></span>

<span data-ttu-id="e430a-p115">Чтобы пользователи могли во время выполнения ставить на форму цифровую подпись, схема источника данных должна объявить именованную подпись элемента для хранения данных о подписях XML (цифровой подписи), которые создаются при подписывании формы пользователем. Это объявление осуществляется с помощью элемента **xsd:any** с атрибутом пространства имен, указанным в качестве пространства имен подписей XML с подстановочным знаком, а именно: "http://www.w3c.org/2000/09/xmldsig#"</span><span class="sxs-lookup"><span data-stu-id="e430a-p115">To enable users to digitally sign a form at run time, the schema of the data source must declare an element named signature for storing the XML Signatures (digital signature) information that is created when a user signs the form. You make this declaration by using the **xsd:any** element with the namespace attribute specified as the XML Signatures namespace with a wildcard character, as follows: "http://www.w3c.org/2000/09/xmldsig#"</span></span> 
  
```XML
<xsd:element name="signature"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3c.org/2000/09/xmldsig#"  
             processContents="lax" minOccurs="0" maxOccurs="unbounded"/> 
        <xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="binding-a-field-to-a-rich-text-box-control"></a><span data-ttu-id="e430a-166">Привязка поля к элементу управления "Rich Text Box"</span><span class="sxs-lookup"><span data-stu-id="e430a-166">Binding a Field to a Rich Text Box Control</span></span>

 <span data-ttu-id="e430a-p116">Элементы управления **Rich Text Box** в InfoPath предназначены для создания общих XHTML; следовательно, схема должна указывать, что в XML и экземпляре формы является допустимым любое число узлов текста и XHTML. Для формирования такой спецификации служит следующая конструкция XSD.</span><span class="sxs-lookup"><span data-stu-id="e430a-p116">**Rich Text Box** controls in InfoPath generate generic XHTML; consequently, your schema must specify that any number of text and XHTML nodes is valid in the XML of the form instance. You can achieve this specification with the following XSD construct:</span></span> 
  
```XML
<xsd:element name="xhtml"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any minOccurs="0" maxOccurs="unbounded" namespace="http://www.w3.org/1999/xhtml" processContents="lax"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

> [!NOTE]
> <span data-ttu-id="e430a-p117">InfoPath никогда не изменяет содержимое файла схемы XSD, но при разработке приложение может логически вывести его подмножество. Файл схемы в рамках шаблона формы никогда не изменяется как во время разработки, так и во время выполнения.</span><span class="sxs-lookup"><span data-stu-id="e430a-p117">InfoPath never modifies the content of the schema file (.xsd), but it may logically infer a subset of it for design purposes. The schema file is always untouched within the form template at both design time and run time.</span></span> 
  
## <a name="debugging-common-xsd-errors"></a><span data-ttu-id="e430a-171">Общие ошибки отладки XSD</span><span class="sxs-lookup"><span data-stu-id="e430a-171">Debugging Common XSD Errors</span></span>

<span data-ttu-id="e430a-p118">Если созданные во внешней среде файлы XSD загружаются для создания шаблонов форм в конструкторе форм InfoPath, возможен вывод следующих типов сообщений об ошибках: сообщения об ошибках MSXML или сообщения об ошибках InfoPath. Сообщения об ошибках MSXML отображаются в разделе **Сведения** диалогового окна сообщения об ошибках InfoPath и всегда начинаются со ссылки на имя пути к файлу схемы, вызвавшему ошибку. В InfoPath поддерживаются лишь некоторые допустимые конструкции схемы XSD; они рассматриваются в разделе "Неподдерживаемые конструкции XSD". В следующих разделах представлено описание общих ошибок, которые могут привести к сбоям загрузки схем в InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e430a-p118">If you load externally authored XSD files to create form templates in the InfoPath form designer, you may receive either of two types of error messages: MSXML error messages or InfoPath error messages. MSXML error messages appear in the **Details** section of an InfoPath error message dialog box, and they always begin with a reference to the name or path of the schema file that is raising the error. Some valid XSD schema constructs are not supported by InfoPath; these are discussed in the Unsupported XSD Constructs section. The following sections describe some common errors that can cause schemas to fail to load successfully in InfoPath.</span></span> 
  
## <a name="the-xsd-namespace-declaration"></a><span data-ttu-id="e430a-176">Объявление пространства имен XSD</span><span class="sxs-lookup"><span data-stu-id="e430a-176">The XSD Namespace Declaration</span></span>

<span data-ttu-id="e430a-p119">Аналогично всем стандартам W3C схемы XML (XSD) прошли длительный процесс экспертной оценки, прежде чем стать рекомендуемым средством. Существовало множество рабочих проектов и, соответственно, на основе новых устанавливаемых стандартов было создано много XSD-файлов. В ходе этого процесса корпорация Майкрософт разработала специальный язык схемы, XML-Data Reduced (XDR), который был включен в MSXML 3.0. Начиная с выпуска MSXML 4.0 основные службы XML Майкрософт поддерживают полную рекомендацию XSD. Многие программы по созданию схем не использовали XSD до полной рекомендации. В более старых версиях этих программ могут быть созданы устаревшие файлы XSD, не поддерживаемые инфраструктурой MSXML 5.0, от которой зависит InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e430a-p119">Similar to all W3C standards, XML Schemas (XSD) went through a lengthy review process on its way to becoming a recommendation. There were many working drafts, and consequently, many XSD files were written based on these evolving standards. During this process, Microsoft created a proprietary schema language called XML-Data Reduced (XDR) that was included with MSXML 3.0. Starting with the release of MSXML 4.0, Microsoft XML Core Services supports the full recommendation of XSD. Many programs for creating schemas did not wait for XSD to become a full recommendation. Older versions of these programs may produce outdated XSD files that the MSXML 5.0 infrastructure, on which InfoPath depends, does not support.</span></span>
  
<span data-ttu-id="e430a-183">Чтобы убедиться, что файл XSD поддерживает полную рекомендацию XSD, он должен содержать в теге \<schema\> следующее объявление пространства имен:</span><span class="sxs-lookup"><span data-stu-id="e430a-183">To ensure that an XSD file supports the full XSD recommendation, it should contain the following XML namespace declaration in the \<schema\> tag:</span></span>
  
```XML
xmlns:xsd="http://www.w3.org/2001/XMLSchema"
```

<span data-ttu-id="e430a-p120">Подобно всем объявлениям пространства имен XML префиксом XML (в данном случае "XSD") может быть любая допустимая строка префикса. Наиболее распространены префиксы "XSD", "XS" и "" (префикса нет). Если это объявление пространства имен отсутствует, MSXML обычно сообщает об ошибке, связанной с неправильным определением корня.</span><span class="sxs-lookup"><span data-stu-id="e430a-p120">Similar to all XML namespace declarations, the XML prefix (in this case 'xsd') can be any valid prefix string. Some common prefixes you may see in practice are 'xsd', 'xs', and '' (no prefix). MSXML usually reports an error about the root not being properly defined if this namespace declaration is missing.</span></span>
  
## <a name="importing-and-including-schemas"></a><span data-ttu-id="e430a-187">Импорт и включение схем</span><span class="sxs-lookup"><span data-stu-id="e430a-187">Importing and Including Schemas</span></span>

<span data-ttu-id="e430a-p121">Схемы XSD являются расширяемыми и могут импортировать и включать в свой состав другие схемы. Обычно импорт схемы выполняется, если указанная в атрибуте **targetNamespace** схема отличается от текущей схемы. Схему необходимо включить в другую, если указанная в атрибуте **targetNamespace** схема совпадает с текущей.</span><span class="sxs-lookup"><span data-stu-id="e430a-p121">XSD schemas are extensible and can import and include other schemas. Generally, you should import a schema if the schema specified in the **targetNamespace** attribute differs from the current schema. You should include it if the schema specified in the **targetNamespace** attribute is the same as the current schema.</span></span> 
  
<span data-ttu-id="e430a-191">Семантики импорта и включения схем выглядят следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e430a-191">The semantics for importing and including schemas are as follows:</span></span>
  
```XML
<xsd:import namespace = "[anyURI]" schemaLocation = "[anyURI]"/> 
<xsd:include schemaLocation = "[anyURI]"/> 

```

<span data-ttu-id="e430a-p122">При отсутствии атрибута **schemaLocation** (так бывает с некоторыми конверторами) MSXML выводит ошибку, поскольку не удается найти файл. При получении подобного сообщения следует проверить, что ресурс или расположение, указанные в атрибуте "schemaLocation", доступны пользователям шаблона формы. Разумеется, ошибки возникают и в случае, когда атрибут **schemaLocation** ссылается на нерабочий или несуществующий сервер или каталог либо если у пользователей нет прав на доступ. Кроме того, нужно проверить допустимость всех импортированных и включенных схем.</span><span class="sxs-lookup"><span data-stu-id="e430a-p122">If the **schemaLocation** attribute is missing (as happens with some converters), then MSXML raises an error because it cannot find the file. If you get this error, also check to make sure that the resource or location specified in the schemaLocation attribute is accessible by users of the form template. Obviously, errors occur if the **schemaLocation** attribute references a server or directory that is down or nonexistent or if users do not have access permissions. Also, be sure to examine all imported and included schemas to make sure they are valid.</span></span> 
  
> [!NOTE]
> <span data-ttu-id="e430a-p123">Ошибки, вызванные проблемами с атрибутом **schemaLocation**, представляют сложность только при первом импорте InfoPath схем; то есть при первой разработке формы на основе существующей схемы. После этого InfoPath работает с кэшированными версиями файлов схемы, сохраненных в шаблоне формы.</span><span class="sxs-lookup"><span data-stu-id="e430a-p123">Errors caused by problems with the **schemaLocation** attribute are an issue only when InfoPath first imports the schemas; that is, when you first start designing a form based on an existing schema. After that, InfoPath works with cached versions of the schema files that are stored in the form template.</span></span> 
  
<span data-ttu-id="e430a-p124">Использование пустого атрибута пространства имен допускается при импорте схемы, если она не указывает атрибут **targetNamespace**. Обычно пространство имен при импорте должно соответствовать атрибуту **targetNamespace**, указанному в импортируемой схеме.</span><span class="sxs-lookup"><span data-stu-id="e430a-p124">An empty namespace attribute is allowed when importing a schema, if that schema does not specify a **targetNamespace** attribute. In general, the namespace on the import must match the **targetNamespace** specified in the schema that you import.</span></span> 
  
## <a name="nondeterministic-schemas"></a><span data-ttu-id="e430a-200">Недетерминированные схемы</span><span class="sxs-lookup"><span data-stu-id="e430a-200">Nondeterministic Schemas</span></span>

<span data-ttu-id="e430a-p125">Инфраструктура MSXML 5.0, от которой зависит приложение InfoPath, может с большой вероятностью выявлять и выводить ошибки для оповещения о недетерминированных схемах, однако в итоговых сообщениях об ошибках не указывается номер строки, определяющий часть схемы, вызвавшую ошибку. В этом разделе рассматриваются вопросы о детерминированности файлов схемы XSD, а также объясняется значение недетерминированности. Здесь представлены и общие ошибки, которых следует избегать.</span><span class="sxs-lookup"><span data-stu-id="e430a-p125">The MSXML 5.0 infrastructure that InfoPath depends upon can reliably detect and raise errors to alert you to nondeterministic schemas, but the resultant error message does not provide a line number to tell you which part of the schema is raising the error. This section discusses why it is important for XSD schema files to be deterministic and what it means to be nondeterministic. It also shows some common errors to avoid.</span></span>
  
<span data-ttu-id="e430a-p126">Схемы XSD существуют для проверки структуры данных XML и семантик типов. Для решения этой задачи система проверки (в данном случае MSXML 5.0) должна сопоставить узлы XML объявлениям XSD. Без этого сопоставления проверка не выполняется. Если сопоставление гарантировано, то схема является детерминированной. Если существует один экземпляр XML, делающий сопоставление невозможным, схема является недетерминированной.</span><span class="sxs-lookup"><span data-stu-id="e430a-p126">XSD schemas exist for the purpose of validating XML data structure and type semantics. To accomplish this task, the validating system (in this case, MSXML 5.0) must map XML nodes to XSD declarations. Without this mapping, the validating system cannot accomplish its task. If a mapping can be guaranteed, then the schema is deterministic. If there is a single XML instance that makes this mapping impossible, then the schema is nondeterministic.</span></span>
  
<span data-ttu-id="e430a-209">В следующем примере представлена недетерминированная схема.</span><span class="sxs-lookup"><span data-stu-id="e430a-209">The following example schema is nondeterministic:</span></span>
  
```XML
<xsd:element name="file_Information"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element name="file_name"/> 
            <xsd:choice> 
                <xsd:element name="file_path"/> 
                <xsd:sequence> 
                    <xsd:element name="file_path" minOccurs="0"/> 
                    <xsd:element name="URI"/> 
                </xsd:sequence> 
            </xsd:choice> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="e430a-210">Чтобы показать, почему сегмент XSD является недетерминированным, предположим, что имеется следующий фрагмент XML, который нужно проверить с помощью этой схемы.</span><span class="sxs-lookup"><span data-stu-id="e430a-210">To illustrate why this XSD segment is nondeterministic, assume you have the following XML fragment that you want to validate with this schema:</span></span>
  
```XML
<file_Information> 
    <file_name>my_Schema.xsd</file_name> 
    <file_path>c:\xsd</file_path> 
</file_Information> 

```

<span data-ttu-id="e430a-p127">В данном фрагменте XML не ясно, является ли элемент  *\<file_path\>*  необходимым узлом из первой части объявления выбора или дополнительным узлом из второй части объявления выбора. Это различие очень важно по следующим причинам.</span><span class="sxs-lookup"><span data-stu-id="e430a-p127">In this XML fragment, it is not clear whether the  *\<file_path\>*  element is the required node from the first part of the choice declaration or the optional one from the second part of the choice declaration. This distinction is important for the following reasons:</span></span> 
  
1. <span data-ttu-id="e430a-213">Если фрагмент XML проверен по первой части объявления выбора, тогда XML считается допустимым в данной схеме.</span><span class="sxs-lookup"><span data-stu-id="e430a-213">If the XML fragment is validated against the first part of the choice declaration, then the XML is valid against the schema.</span></span>
    
2. <span data-ttu-id="e430a-214">Если фрагмент XML проверен по второй части объявления выбора, тогда схема признается недопустимой из-за отсутствия необходимого узла \<URI\>.</span><span class="sxs-lookup"><span data-stu-id="e430a-214">If the XML fragment is validated against the second part of the choice declaration, then the schema is not valid, because the required \<URI\> node is missing.</span></span> 
    
<span data-ttu-id="e430a-p128">Некоторые системы проверки XSD не выдают ошибки при проверке по данной схеме, поскольку существует допустимый путь. MSXML является более жестким и выводит ошибку о недетерминированности схемы.</span><span class="sxs-lookup"><span data-stu-id="e430a-p128">Some XSD validation systems err toward validating against this schema because there is a valid path. MSXML is stricter and raises an error stating that the schema is nondeterministic.</span></span>
  
<span data-ttu-id="e430a-p129">Далее представлено еще несколько примеров недетерминированных схем. В первом рассматриваются дополнительные элементы. Такие ситуации часто возникают с преобразованиями из XDR в XSD и связаны с различиями в заданных по умолчанию учетных данных в двух языках схем. Сначала следует рассмотреть дополнительные элементы, объявленные с помощью элементов **xsd:choice** и **xsd:sequence**. Дополнительные элементы, объявленные в элементе **xsd:sequence**, обычно проходят проверку надлежащим образом до тех пор, пока элементы с одинаковыми именами не будут присутствовать более одного раза и между ними будут находиться только дополнительные элементы.</span><span class="sxs-lookup"><span data-stu-id="e430a-p129">What follows are a few more examples of nondeterministic schemas. The first deals with optional elements. These cases often arise from XDR to XSD converters because of differences in the default cardinalities in the two schema languages. The first case to consider is optional elements declared with **xsd:choice** and **xsd:sequence** elements. Optional elements declared in an **xsd:sequence** element usually validate properly, as long as you do not have elements with the same name more than once, with only optional elements in between. For example:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:element ref="aNode" /> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="e430a-223">Чтобы понять, почему этот сегмент схемы является недетерминированным, предположим, что имеется следующий недопустимый фрагмент XML.</span><span class="sxs-lookup"><span data-stu-id="e430a-223">To understand why this schema segment is nondeterministic, assume you have the following invalid XML fragment:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
    <anotherNode/> 
</container> 

```

<span data-ttu-id="e430a-224">Глядя на этот фрагмент, становится ясна причина его недействительности: перед элементом  `<aNode>` находятся два элемента  `<anotherNode>`, тогда как допускается только один.</span><span class="sxs-lookup"><span data-stu-id="e430a-224">Looking at this fragment, you can see why it is invalid: there are two  `<aNode>` elements before the  `<anotherNode>` element, when only one is allowed.</span></span> 
  
<span data-ttu-id="e430a-225">Теперь предположим, что нужно проверить следующий экземпляр XML.</span><span class="sxs-lookup"><span data-stu-id="e430a-225">Now assume that you have the following XML instance to validate:</span></span>
  
```XML
<container> 
    <aNode/> 
    <aNode/> 
</container> 

```

<span data-ttu-id="e430a-p130">Сложность заключается в определении действительности экземпляра. Есть ли два элемента  `<aNode>`, из которых допускается только один, или есть элемент  `<aNode>`, в котором он допускается, и другой, в котором он допускается? Схема является недетерминированной, поскольку узнать ответ невозможно.</span><span class="sxs-lookup"><span data-stu-id="e430a-p130">The challenge is to determine whether this instance is valid. Do you have two  `<aNode>` elements where only one is allowed, or do you have an  `<aNode>` element where it is allowed and another where it is allowed? The schema is nondeterministic because there is no way to know.</span></span> 
  
<span data-ttu-id="e430a-p131">Таким же образом использование дополнительных элементов, объявленных в элементе **xsd:choice**, обычно является проблематичным. В следующем упрощенном примере нельзя определить, происходит ли выбор один раз при отсутствии дополнительного элемента либо он не происходит вообще.</span><span class="sxs-lookup"><span data-stu-id="e430a-p131">Similarly, optional elements declared in an **xsd:choice** element are usually problematic. In the following simplified example, there is no way to determine whether the choice occurred once with the optional element not being there or whether it never occurred at all.</span></span> 
  
```XML
<xsd:choice> 
    <xsd:element name="node" minOccurs="0"/> 
</xsd:choice> 

```

<span data-ttu-id="e430a-p132">Последний не вызывающий доверия способ заключается в использовании элемента **xsd:any** без определения пространства имен, как в  `<xsd:any namespace="##other"/>`, после элемента **xsd:sequence**. Эта конструкция вносит особые сложности, когда следует за дополнительным элементом. При повторном обращении к предыдущему примеру и изменении последнего узла на элемент **xsd:any** видно, что предыдущие аргументы о недетерминированности по-прежнему применимы, как показано далее.</span><span class="sxs-lookup"><span data-stu-id="e430a-p132">The final questionable practice is using an **xsd:any** element without a namespace definition, as in  `<xsd:any namespace="##other"/>` , after an **xsd:sequence** element. This construct is especially troublesome when it follows an optional element. If you revisit the previous example and change just the last node to an **xsd:any** element, you can see that all the previous arguments about nondeterminism still apply, as follows:</span></span> 
  
```XML
<xsd:element name="container"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:element ref="aNode" /> 
            <xsd:element ref="anotherNode" minOccurs="0"/> 
            <xsd:any />     
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="illegal-enumeration-values"></a><span data-ttu-id="e430a-234">Недопустимые значения перечисления</span><span class="sxs-lookup"><span data-stu-id="e430a-234">Illegal Enumeration Values</span></span>

<span data-ttu-id="e430a-p133">Обычно схемы XSD не выполняют никаких проверок до тех пор, пока не будет проверен фактический документ экземпляра. Исключением является наличие в схеме перечисления. В этом случае схема проверяет значения перечисления по типам перечисления, чтобы гарантировать, что они представляют правильные значения узлов. Далее приведено два примера.</span><span class="sxs-lookup"><span data-stu-id="e430a-p133">XSD schemas typically do not perform any type validation until you validate an actual instance document. An exception to this is when you have an enumeration in your schema. In this case, the schema validates the enumeration values against the enumeration types to ensure they are proper node values. Here are two examples:</span></span>
  
```XML
<xsd:simpleType name="showTimes"> 
    <xsd:restriction base="xsd:time"> 
        <xsd:enumeration value="18:30:00"/> 
        <xsd:enumeration value="20:45:00"/> 
        <xsd:enumeration value="eleven o'clock"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="e430a-239">Эта схема недопустима, поскольку значение "eleven o'clock" не является допустимым для элемента типа **xsd:time**.</span><span class="sxs-lookup"><span data-stu-id="e430a-239">This schema is invalid because "eleven o'clock" is not a valid value for an element of type **xsd:time**.</span></span>
  
<span data-ttu-id="e430a-240">Далее приведен более сложный пример.</span><span class="sxs-lookup"><span data-stu-id="e430a-240">The following is a more complex example:</span></span>
  
```XML
<xsd:simpleType name="concession"> 
    <xsd:restriction base="xsd:NMTOKEN"> 
        <xsd:enumeration value="GummyBears"/> 
        <xsd:enumeration value="SnowCaps"/> 
        <xsd:enumeration value="M&Ms"/> 
    </xsd:restriction> 
</xsd:simpleType> 

```

<span data-ttu-id="e430a-p134">Чтобы понять причину, по которой этой пример признается недействительным, необходимо разобраться в способе определения типа **xsd:NMTOKEN**. В спецификации типов данных W3C тип **NMTOKEN** определен следующим образом: "NMTOKEN (маркер имени)  это сочетание символов имени."</span><span class="sxs-lookup"><span data-stu-id="e430a-p134">To understand why this example is invalid, you must understand how the type **xsd:NMTOKEN** is defined. The W3C data types specification defines the **NMTOKEN** type as follows: "An NMTOKEN (name token) is any mixture of name characters."</span></span> 
  
<span data-ttu-id="e430a-243">При дальнейшем изучении становится ясно, что "&" не является допустимым символом имени, и поэтому "M&Ms" не проходит проверку в качестве типа **NMTOKEN**.</span><span class="sxs-lookup"><span data-stu-id="e430a-243">If you investigate further, you find that '' is not a valid name character, and therefore "MMs" does not validate as an NMTOKEN type.</span></span> 
  
## <a name="empty-sequence-or-choice-elements"></a><span data-ttu-id="e430a-244">Пустые элементы последовательности или выбора</span><span class="sxs-lookup"><span data-stu-id="e430a-244">Empty Sequence or Choice Elements</span></span>

<span data-ttu-id="e430a-245">Иногда MSXML выдает ошибки об объявлениях схемы, содержащих пустые элементы **xsd:choice** или **xsd:sequence**, как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="e430a-245">MSXML sometimes raises errors about schema declarations that contain empty **xsd:choice** or **xsd:sequence** elements, as shown in the following example.</span></span> 
  
```XML
<xsd:element name="emptyContainer"> 
    <xsd:complexType> 
        <xsd:choice /> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="e430a-246">Для решения проблемы следует удалить пустой тег  `<xsd:choice />`.</span><span class="sxs-lookup"><span data-stu-id="e430a-246">Removing the empty  `<xsd:choice />` tag should resolve this problem.</span></span> 
  
## <a name="regular-expressions"></a><span data-ttu-id="e430a-247">Регулярные выражения</span><span class="sxs-lookup"><span data-stu-id="e430a-247">Regular Expressions</span></span>

<span data-ttu-id="e430a-p135">В MSXML 5.0 могут возникнуть проблемы, связанные с проверкой загружаемых шаблонов регулярных выражений. Регулярные выражения могут быть сложными, поэтому их нужно использовать с осторожностью. Похоже, каждое средство синтаксического анализа XSD использует гибкий язык регулярных выражений (т. е. официальный язык регулярных выражений XSD с элементами из других подобных языков). Если конструктор форм InfoPath не может проанализировать регулярное выражение, возможно, приложение InfoPath сформировало недопустимые демонстрационные данные либо не сформировало их совсем. Такая ситуация приемлема во время разработки, так как демонстрационные данные в InfoPath используются только для форматирования. Но при использовании регулярного выражения, которое не поддерживается MSXML, в InfoPath не удастся проверить значение при заполнении пользователем формы. В документе [XML Schema. Часть 0: основные сведения (издание второе)](http://www.w3.org/TR/xmlschema-0/) описано, какие регулярные выражения XSD допустимы. Дополнительные сведения о регулярных выражениях XSD и регулярных выражениях уровня 1 Юникода см. в статье о [регулярных выражениях Юникода](http://www.unicode.org/reports/tr18/).</span><span class="sxs-lookup"><span data-stu-id="e430a-p135">MSXML 5.0 can have problems validating regular expression patterns on load. Regular expressions can be complicated, and you should be careful when you are using them. Every XSD parser seems to have flexible regular expression languages; that is, they implement the official XSD regular expression language plus elements from other regular expression languages. If InfoPath form designer has problems parsing a regular expression, then the sample data InfoPath generates might be invalid or might not be generated at all. This is acceptable at design time, because InfoPath uses only sample data for formatting. However, if you use a regular expression that MSXML does not support, then InfoPath cannot validate a value against it when a user is filling out a form. [XML Schema Part 0: Primer Second Edition](http://www.w3.org/TR/xmlschema-0/)describes what is supported in XSD regular expressions. For more information about XSD regular expressions and Unicode level 1 regular expressions, see [Unicode Regular Expressions](http://www.unicode.org/reports/tr18/) .</span></span> 
  
## <a name="targetnamespace-attribute-issues"></a><span data-ttu-id="e430a-256">Проблемы, связанные с атрибутом "targetNamespace"</span><span class="sxs-lookup"><span data-stu-id="e430a-256">targetNamespace Attribute Issues</span></span>

<span data-ttu-id="e430a-p136">Файлы XSD интересны тем, что атрибут **targetNamespace** по умолчанию ссылается только на объявления верхнего уровня несмотря на то, что  `attributeFormDefault=qualified` и  `elementFormDefault=qualified` можно задать на переопределение этого заданного по умолчанию поведения. В качестве примера предположим, что в наличии имеется следующий файл XSD.</span><span class="sxs-lookup"><span data-stu-id="e430a-p136">XSD is interesting in that, by default, the **targetNamespace** attribute refers to only the top-level declarations, although you can set  `attributeFormDefault=qualified` and  `elementFormDefault=qualified` to override this default behavior. As an example, assume that you have the following XSD.</span></span> 
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element name="local"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
</xsd:schema> 

```

<span data-ttu-id="e430a-259">И далее, документ XML выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e430a-259">And that, your XML instance document resembles the following example.</span></span>
  
```XML
<ns:root xmlns:ns="http://ns"> 
    <local/> 
</ns:root> 

```

<span data-ttu-id="e430a-p137">Поскольку квалификация по умолчанию отключена, для локальных определений не требуется конечное пространство имен. Однако если локальное определение меняется на глобальное, ссылка должна быть снабжена префиксом пространства имен. Например, следующая схема является недопустимой.</span><span class="sxs-lookup"><span data-stu-id="e430a-p137">Local definitions do not require the target namespace because qualification is turned off by default. However, if you change your local definition to be global, then your reference must be qualified with the namespace prefix. For example, the following schema is invalid.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="e430a-p138">Эта схема недействительна, поскольку "global" находится в пространстве имен "http://ns". ref="global" не распознается, так как заданное по умолчанию пространство имен отлично от "http://ns". Для устранения этой ошибки необходимо добавить префикс для конечного пространства имен и применять его для всех глобальных ссылок и использований типов. Исправленная схема выглядит следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e430a-p138">This schema is invalid because "global" is in the namespace "http://ns". The simple ref="global" is not recognized because the default namespace is not "http://ns". To fix this, you must add a prefix for the target namespace and use that for all global references and type uses. The corrected schema looks like the following.</span></span>
  
```XML
<xsd:schema xmlns:xsd="http://www.w3.org/2001/XMLSchema"  
    xmlns:ns="http://ns" targetNamespace="http://ns" > 
    <xsd:element name="root"> 
        <xsd:complexType> 
            <xsd:sequence> 
                <xsd:element ref="ns:global"/> 
            </xsd:sequence> 
        </xsd:complexType> 
    </xsd:element> 
 
    <xsd:element name="global"/> 
</xsd:schema> 

```

<span data-ttu-id="e430a-267">Если в схеме указан атрибут **targetNamespace**, необходимо убедиться, что все глобальные ссылки имеют правильный префикс пространства имен.</span><span class="sxs-lookup"><span data-stu-id="e430a-267">If your schema has the **targetNamespace** attribute specified, ensure that all global references are qualified with the correct namespace prefix.</span></span> 
  
## <a name="xml-processing-instruction-encoding-unicode-vs-ansii"></a><span data-ttu-id="e430a-268">Кодировка инструкции обработки XML (Юникод и ANSII)</span><span class="sxs-lookup"><span data-stu-id="e430a-268">XML Processing Instruction Encoding (Unicode vs. ANSII)</span></span>

<span data-ttu-id="e430a-p139">XML поддерживает только наборы символов в кодировке Юникод. Поэтому при сохранении файлов с символами ANSII данные могут быть потеряны. Сохранение же файлов в кодировке UTF-16 может быть излишним. Чтобы сократить затраты на внедрение средство чтения XML, автор XML-документа должен указать используемую кодировку в инструкции обработки XML. Можно распознать следующую знакомую инструкцию обработки.</span><span class="sxs-lookup"><span data-stu-id="e430a-p139">XML supports only Unicode character sets. Therefore, you may lose information if you save files that use ANSII characters. However, saving files as UTF-16 may be excessive for your particular use. To reduce the implementation cost of an XML reader, the XML author must state which encoding they are using in the top-level XML processing instruction. You may recognize the following processing instruction.</span></span>
  
```XML
xml version="1.0" encoding="UTF-8"
```

<span data-ttu-id="e430a-p140">Этот тег инструкции обработки указывает, что файл имеет кодировку UTF-8. Необходимо убедиться, что кодировка файла совпадает с кодировкой, определенной в теге инструкции обработки. Чтобы определить кодировку, можно посмотреть на байты файла и найти отметки порядка байт Юникода. Однако есть более простой способ. При возникновении трудностей с открытием схемы XSD нужно выбрать кодировку UTF-8, открыть схему в текстовом редакторе (например, в Блокноте), а затем сохранить файл с помощью кодировки UTF-8 (в Блокноте в диалоговом окне **Сохранить как** есть раскрывающийся список **Кодировка**). Если файл по-прежнему не открывается, проблема не связана с кодировкой.</span><span class="sxs-lookup"><span data-stu-id="e430a-p140">This processing instruction tag specifies that the encoding of the file is UTF-8. You must ensure that the file encoding is the same as the encoding stated in the processing instruction tag. You can determine the encoding by looking at the bytes of the file and looking for the Unicode byte order marks. But there is an easier way. If you have problems opening an XSD schema, specify the encoding as "UTF-8", open it in a text editor such as Notepad, and then save the file by using UTF-8 encoding (Notepad provides the **Encoding** drop-down list in the **Save As** dialog box). If you still have problems opening the file, it is not an encoding issue.</span></span> 
  
## <a name="maxoccurs-attribute-inside-the-xsdall-element"></a><span data-ttu-id="e430a-280">Атрибут "maxOccurs" в элементе "xsd:all"</span><span class="sxs-lookup"><span data-stu-id="e430a-280">maxOccurs Attribute Inside the xsd:all Element</span></span>

<span data-ttu-id="e430a-p141">В связи со способом определения недетерминизма в рекомендации для схемы XML единственным допустимым значением для атрибута **maxOccurs** элемента **xsd:element** в элементе **xsd:all** является 1. Например, допустимо следующее.</span><span class="sxs-lookup"><span data-stu-id="e430a-p141">Due to the way nondeterminism is defined in the XML Schema recommendation, the only valid value for the **maxOccurs** attribute of an **xsd:element** element inside an **xsd:all** element is 1. For example, the following is valid.</span></span> 
  
```XML
<xsd:all> 
    <xsd:element name="x" minOccurs="0"/> 
    <xsd:element name="docs" minOccurs="0"/> 
</xsd:all> 

```

<span data-ttu-id="e430a-283">Однако данный пример не является допустимым.</span><span class="sxs-lookup"><span data-stu-id="e430a-283">However, this example is not valid.</span></span>
  
```XML
<xsd:all>     
    <xsd:element name="x" minOccurs="0" maxOccurs="unbounded"/> 
    <xsd:element name="docs" minOccurs="0" maxOccurs="unbounded"/> 
</xsd:all> 

```

<span data-ttu-id="e430a-p142">Этот пример недопустим, поскольку системе проверки не удается определить, соответствуют ли два экземпляра  `<x/>` одному объявлению или же объявлению и другому неправильному определению. На одних и тех же строках не могут находиться два элемента с одинаковым именем в теге  `<xsd:all>`.</span><span class="sxs-lookup"><span data-stu-id="e430a-p142">This example is invalid because the validation system cannot determine whether two occurrences of  `<x/>` map to the single declaration or to the declaration and another invalid definition. Along the same lines, you cannot have two elements of the same name in an  `<xsd:all>` tag.</span></span> 
  
<span data-ttu-id="e430a-p143">Данный пример также интересен тем, что позволяет иметь любое количество узлов  `<x/>` и  `<docs/>`, расположенных в любом порядке внутри содержащего элемента. Несмотря на недопустимость этой структуры, существует обходной метод. Для достижения результата, показанного в следующем примере, можно использовать элемент **xsd:choice**.</span><span class="sxs-lookup"><span data-stu-id="e430a-p143">This example is also interesting because it allows you to have any number of  `<x/>` and  `<docs/>` nodes inside a containing element in any order. Although this construct is invalid, there is a workaround. By using the **xsd:choice** element, you can achieve the same result, as demonstrated in the following example.</span></span> 
  
```XML
<xsd:choice minOccurs="0" maxOccurs="unbounded"> 
    <xsd:element name="x" /> 
    <xsd:element name="docs" /> 
</xsd:choice> 

```

## <a name="how-to-edit-or-author-an-xsd-for-infopath"></a><span data-ttu-id="e430a-289">Изменение или создание XSD для InfoPath</span><span class="sxs-lookup"><span data-stu-id="e430a-289">How to Edit or Author an XSD for InfoPath</span></span>

<span data-ttu-id="e430a-290">В следующих разделах приведены два примера по изменению и созданию схемы для вывода в InfoPath определенных результатов.</span><span class="sxs-lookup"><span data-stu-id="e430a-290">The two examples in the following sections show how to edit or author a schema to produce specific results in InfoPath.</span></span>
  
## <a name="allowing-user-defined-elements-to-be-inserted-in-the-fields-task-pane"></a><span data-ttu-id="e430a-291">Вставка определенных пользователем элементов в область задач "Поля"</span><span class="sxs-lookup"><span data-stu-id="e430a-291">Allowing User-defined Elements to Be Inserted in the Fields Task Pane</span></span>

<span data-ttu-id="e430a-p144">Чтобы определенные пользователем элементы могли отображаться в рамках родительского элемента в области задач **Поля**, в родительский элемент необходимо вставить элемент **xsd:any**. Чтобы вставлять определенные пользователем элементы в  `<your_node_name>`, объявление XSD должно выглядеть следующим образом.</span><span class="sxs-lookup"><span data-stu-id="e430a-p144">To allow user-defined elements to appear under a parent element in the **Fields** task pane, you must insert an **xsd:any** element under the parent element. To allow user-defined elements to be inserted inside  `<your_node_name>` , the XSD declaration should resemble the following.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType> 
        <xsd:sequence> 
            <xsd:any namespace="##any | ##other"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

<span data-ttu-id="e430a-294">Чтобы разрешить использование определенных пользователями атрибутов, к объявлению элемента необходимо добавить  `<xsd:anyAttribute namespace="##any | ##other"/>`.</span><span class="sxs-lookup"><span data-stu-id="e430a-294">If you also want to allow user-defined attributes, then you must add  `<xsd:anyAttribute namespace="##any | ##other"/>` to the element declaration.</span></span> 
  
## <a name="allowing-rich-text-elements-to-be-bound-in-infopath-design-and-edit-modes"></a><span data-ttu-id="e430a-295">Привязка элементов "Rich Text" в режимах конструктора и правки InfoPath</span><span class="sxs-lookup"><span data-stu-id="e430a-295">Allowing Rich Text Elements to be Bound in InfoPath Design and Edit Modes</span></span>

<span data-ttu-id="e430a-296">Если нужно объявить элемент, который можно привязать к элементу управления **Rich Text Box**, он должен иметь следующую форму, содержащую элемент **xsd:any** с атрибутом пространства имен в виде "http://www.w3.org/1999/xhtml", как показано в следующем примере.</span><span class="sxs-lookup"><span data-stu-id="e430a-296">If you want to declare an element that can be bound to a **Rich Text Box** control, then it should have the following form, which includes the **xsd:any** element that has a namespace attribute set to "http://www.w3.org/1999/xhtml" as shown in the following example.</span></span> 
  
```XML
<xsd:element name="your_node_name"> 
    <xsd:complexType mixed="true"> 
        <xsd:sequence> 
            <xsd:any namespace="http://www.w3.org/1999/xhtml"  
                minOccurs="0" maxOccurs="unbounded"/> 
        </xsd:sequence> 
    </xsd:complexType> 
</xsd:element> 

```

## <a name="conclusion"></a><span data-ttu-id="e430a-297">Заключение</span><span class="sxs-lookup"><span data-stu-id="e430a-297">Conclusion</span></span>

<span data-ttu-id="e430a-p145">Благодаря поддержке InfoPath при разработке форм XML, основанных на созданных во внешней среде файлах схемы XML (XSD), можно создать шаблон формы, работающий с отраслевой или пользовательской схемой, сформированной в организации. Представленные в этой статье сведения полезны при создании файлов настраиваемой схемы XSD, совместимых с InfoPath; кроме того, вы сможете устранить общие неполадки, возникающие при загрузке созданных во внешней среде файлов XSD в среду разработки InfoPath.</span><span class="sxs-lookup"><span data-stu-id="e430a-p145">By taking advantage of InfoPath support for designing XML form solutions that are based on externally authored XML Schema (.xsd) files, you can create a form template that works with an industry-standard schema or custom schema created by your company or organization. By using the information in this article, you can create custom XSD schema files that are compatible with InfoPath, and you can troubleshoot common issues that you may encounter when you load externally authored XSD files into the InfoPath design environment.</span></span>
  
## <a name="see-also"></a><span data-ttu-id="e430a-300">См. также</span><span class="sxs-lookup"><span data-stu-id="e430a-300">See also</span></span>

- [<span data-ttu-id="e430a-301">W3C XML Schema</span><span class="sxs-lookup"><span data-stu-id="e430a-301">W3C XML Schema</span></span>](http://www.w3.org/XML/Schema)
- [<span data-ttu-id="e430a-302">XML Schema W3C. Основные сведения</span><span class="sxs-lookup"><span data-stu-id="e430a-302">W3C XML Schema Primer</span></span>](http://www.w3.org/TR/xmlschema-0/)
- [<span data-ttu-id="e430a-303">Справочник по структурам XML Schema W3C</span><span class="sxs-lookup"><span data-stu-id="e430a-303">W3C XML Schema Structures Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/structuresref.mdl)
- [<span data-ttu-id="e430a-304">Справочник по типам данных XML Schema W3C</span><span class="sxs-lookup"><span data-stu-id="e430a-304">W3C XML Schema Datatypes Reference</span></span>](http://www.xml.com/pub/a/2000/11/29/schemas/dataref.mdl)
- [<span data-ttu-id="e430a-305">Учебное пособие по XML Schema</span><span class="sxs-lookup"><span data-stu-id="e430a-305">XML Schema Tutorial</span></span>](http://www.w3schools.com/schema/default.asp)
- [<span data-ttu-id="e430a-306">Центр разработчиков XML</span><span class="sxs-lookup"><span data-stu-id="e430a-306">XML Developer Center</span></span>](http://msdn.microsoft.com/ru-RU/xml/default.aspx)

