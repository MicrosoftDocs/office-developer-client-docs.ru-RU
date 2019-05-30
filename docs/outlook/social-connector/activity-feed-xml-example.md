---
title: Пример XML-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: 'Пример XML в этом разделе — это строка XML веб-канала активности, возвращаемая Outlook Social Connector (OSC) после вызова метода ISocialSession2:: Жетактивитиесекс для социальной сети.'
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538328"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="d4fe4-103">Пример XML-канала активности</span><span class="sxs-lookup"><span data-stu-id="d4fe4-103">Activity Feed XML Example</span></span>

<span data-ttu-id="d4fe4-104">Пример XML в этом разделе — это строка XML веб-канала активности, возвращаемая Outlook Social Connector (OSC) после вызова метода [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) для социальной сети.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="d4fe4-105">В этом примере показан XML-код **activityFeed** , который содержит следующие четыре действия, разделенных элементом **activityDetails** и сопоставленный с шаблоном для целей отображения:</span><span class="sxs-lookup"><span data-stu-id="d4fe4-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="d4fe4-106">Изображение профиля обновляется с помощью Мелисса Макбес, **овнерид** в социальной сети — 4667647.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="d4fe4-107">Это действие указывает три переменные шаблона типа **публишервариабле**, **листвариабле**и **пиктуревариабле** (которая заключена в **листвариабле**).</span><span class="sxs-lookup"><span data-stu-id="d4fe4-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="d4fe4-108">В этих переменных указывается пользователь, который опубликовал элемент веб-канала активности, и сведения для обновляемого изображения (с помощью дочерних элементов **Name**, **value**, **алттекст**и **href** объекта **пиктуревариабле**).</span><span class="sxs-lookup"><span data-stu-id="d4fe4-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="d4fe4-109">Фотография профиля обновляется Майкла Аффронти, чьи **овнерид** в социальной сети — 5015012.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="d4fe4-110">Как и при последнем действии, это действие указывает три переменные шаблона типа **публишервариабле**, **листвариабле**и **пиктуревариабле**.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="d4fe4-111">В этих переменных указывается пользователь, который опубликовал элемент веб-канала активности и сведения для обновляемого изображения.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="d4fe4-112">В результате обновления состояния Майкл Аффронти отображается то же самое **овнерид** , что и в последнем действии 5015012.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="d4fe4-113">Это действие задает две переменные шаблона типа **публишервариабле** и **текствариабле**.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="d4fe4-114">**публишервариабле** указывает пользователя, опубликовавшего элемент веб-канала активности, и **текствариабле** содержит **значение** строки состояния`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="d4fe4-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="d4fe4-115">Запись блога Майкла Аффронти, в которой показано одно и то же **овнерид** в 5015012 как два последних действия.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="d4fe4-116">Это действие задает две переменные шаблона типа **публишервариабле** и **линквариабле**.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="d4fe4-117">**публишервариабле** указывает пользователя, который опубликовал элемент веб-канала активности, и **линквариабле** содержит дополнительные сведения (задаются с помощью дочерних элементов " **имя**", " **текст**" и " **значение** " в **линквариабле**) о записи блога.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="d4fe4-118">Каждое из четырех действий указывает значение **templateID** , которое соответствует одному из трех шаблонов, указанных в элементе Templates \*\*\*\* .</span><span class="sxs-lookup"><span data-stu-id="d4fe4-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="d4fe4-119">Каждый шаблон находится в отдельном элементе **activityTemplateContainer** , определяемом значением **templateID** , который также используется для отображения действия с тем же значением **templateID** .</span><span class="sxs-lookup"><span data-stu-id="d4fe4-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="d4fe4-120">Подробное описание элементов XML, используемых в примере, представлено в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="d4fe4-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="d4fe4-121">Обзор XML-файла для элемента веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="d4fe4-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="d4fe4-122">Элемент activityDetails</span><span class="sxs-lookup"><span data-stu-id="d4fe4-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="d4fe4-123">Элемент activityTemplateContainer</span><span class="sxs-lookup"><span data-stu-id="d4fe4-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="d4fe4-124">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="d4fe4-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="d4fe4-125">Пример XML</span><span class="sxs-lookup"><span data-stu-id="d4fe4-125">XML example</span></span>

<span data-ttu-id="d4fe4-126">В следующем примере показан XML-файл **activityFeed** из четырех действий: два обновления изображения профиля, обновление состояния и запись блога.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="d4fe4-127">В XML-коде также задаются три шаблона отображения действий для отображения соответствующих действий.</span><span class="sxs-lookup"><span data-stu-id="d4fe4-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="http://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
  <network>Contoso</network>
  <activities>
    <activityDetails>
      <ownerID>4667647</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a31</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-05T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>4667647</id>
          <nameHint>Melissa Macbeth</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a32</objectID>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <publishDate>2010-03-08T17:19:57</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>https://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
            </simpleTemplateVariable>
          </listItems>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a38</objectID>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <publishDate>2010-03-08T18:30:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com</profileUrl>
        </templateVariable>
        <templateVariable type="textVariable">
          <name>statusText</name>
          <value>is hiking on Mount Rainier this weekend!</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
    <activityDetails>
      <ownerID>5015012</ownerID>
      <objectID>9d2b5e6360894a21d56d7d0b5969d23cf4034a39</objectID>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <publishDate>2010-03-04T15:00:00</publishDate>
      <templateVariables>
        <templateVariable type="publisherVariable">
          <name>Publisher</name>
          <id>5015012</id>
          <nameHint>Michael Affronti</nameHint>
          <profileUrl>https://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>https://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
        </templateVariable>
      </templateVariables>
    </activityDetails>
  </activities>
  <templates>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>1</templateID>
      <activityTemplate>
        <type>Photo</type>
        <title>{publisher:Publisher} has a new profile photo: </title>
        <data>{list:ProfilePhoto({picture:Photo})}</data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>https://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a><span data-ttu-id="d4fe4-128">См. также</span><span class="sxs-lookup"><span data-stu-id="d4fe4-128">See also</span></span>

- [<span data-ttu-id="d4fe4-129">Примеры XML-кода поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="d4fe4-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="d4fe4-130">XML для действий</span><span class="sxs-lookup"><span data-stu-id="d4fe4-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="d4fe4-131">Пример XML-кода возможностей</span><span class="sxs-lookup"><span data-stu-id="d4fe4-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="d4fe4-132">Пример XML-кода друзей</span><span class="sxs-lookup"><span data-stu-id="d4fe4-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="d4fe4-133">Схема XML поставщика социальных соединителей Outlook</span><span class="sxs-lookup"><span data-stu-id="d4fe4-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

