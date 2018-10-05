---
title: Пример XML веб-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: Пример XML в этом разделе — XML строки, возвращаемой в Outlook Social Connector (OSC) после его вызывает метод ISocialSession2::GetActivitiesEx для социальных сетей веб-канала активности.
ms.openlocfilehash: 6370b559c5160bfa48d32afa77715e9a7c126aab
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25390466"
---
# <a name="activity-feed-xml-example"></a><span data-ttu-id="7d173-103">Пример XML веб-канала активности</span><span class="sxs-lookup"><span data-stu-id="7d173-103">Activity Feed XML Example</span></span>

<span data-ttu-id="7d173-104">В примере XML в этом разделе приведен XML строки, возвращаемой в Outlook Social Connector (OSC) после его вызывает метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для социальных сетей веб-канала активности.</span><span class="sxs-lookup"><span data-stu-id="7d173-104">The XML example in this topic is an activity feed XML string returned to the Outlook Social Connector (OSC) after it calls the [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) method for a social network.</span></span> 
  
<span data-ttu-id="7d173-105">В примере показано **activityFeed** XML, который содержит следующие четыре действия, каждый отделяются элемент **activityDetails** и соответствующий шаблон для отображения в целях:</span><span class="sxs-lookup"><span data-stu-id="7d173-105">The example shows the **activityFeed** XML that contains the following four activities, each delimited by the **activityDetails** element and matching a template for display purposes:</span></span> 
  
- <span data-ttu-id="7d173-106">Изображение профиля обновление с Melissa Macbeth, чьи **ownerID** социальные сети — это 4667647.</span><span class="sxs-lookup"><span data-stu-id="7d173-106">A profile picture update by Melissa Macbeth, whose **ownerID** on the social network is 4667647.</span></span> <span data-ttu-id="7d173-107">Это действие задает три переменные шаблона типа **publisherVariable**, **listVariable**и **pictureVariable** (заключенное в **listVariable**).</span><span class="sxs-lookup"><span data-stu-id="7d173-107">This activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable** (which is enclosed in **listVariable**).</span></span> <span data-ttu-id="7d173-108">Эти переменные укажите человека, который публикации веб-канал элемента и сведения о изображение, чтобы обновить (с помощью дочерние элементы **pictureVariable** **имя**, **значение**, **altText**и **href** ) активности.</span><span class="sxs-lookup"><span data-stu-id="7d173-108">These variables specify the person who published the activity feed item, and information for the picture to be updated (by using the **name**, **value**, **altText**, and **href** child elements of **pictureVariable**).</span></span>
    
- <span data-ttu-id="7d173-109">Изображение профиля обновить, Майкл Affronti, чьи **ownerID** социальные сети — это 5015012.</span><span class="sxs-lookup"><span data-stu-id="7d173-109">A profile picture update by Michael Affronti whose **ownerID** on the social network is 5015012.</span></span> <span data-ttu-id="7d173-110">Как и последнее действие, это действие задает три переменные шаблона типа **publisherVariable**, **listVariable**и **pictureVariable**.</span><span class="sxs-lookup"><span data-stu-id="7d173-110">Similar to the last activity, this activity specifies three template variables of type **publisherVariable**, **listVariable**, and **pictureVariable**.</span></span> <span data-ttu-id="7d173-111">Эти переменные укажите человека, который публикации веб-канал элемента и данные рисунка, который требуется обновить активности.</span><span class="sxs-lookup"><span data-stu-id="7d173-111">These variables specify the person who published the activity feed item and information for the picture to be updated.</span></span>
    
- <span data-ttu-id="7d173-112">Обновление состояния, Майкл Affronti, отражающая же **ownerID** из 5015012 как последнего действия.</span><span class="sxs-lookup"><span data-stu-id="7d173-112">A status update by Michael Affronti, showing the same **ownerID** of 5015012 as the last activity.</span></span> <span data-ttu-id="7d173-113">Это действие задает две переменные шаблона типа **publisherVariable** и **textVariable**.</span><span class="sxs-lookup"><span data-stu-id="7d173-113">This activity specifies two template variables of type **publisherVariable** and **textVariable**.</span></span> <span data-ttu-id="7d173-114">**publisherVariable** указывает человека, который публикации веб-канал элементов активности и **textVariable** содержит **значение** из строки состояния`is hiking on Mount Rainier this weekend!`</span><span class="sxs-lookup"><span data-stu-id="7d173-114">**publisherVariable** specifies the person who published the activity feed item, and **textVariable** includes a **value** of the status line  `is hiking on Mount Rainier this weekend!`</span></span>
    
- <span data-ttu-id="7d173-115">Публикация в блоге, Майкл Affronti, отражающая же **ownerID** из 5015012 как последние два действия.</span><span class="sxs-lookup"><span data-stu-id="7d173-115">A blog post by Michael Affronti, showing the same **ownerID** of 5015012 as the last two activities.</span></span> <span data-ttu-id="7d173-116">Это действие задает две переменные шаблона типа **publisherVariable** и **linkVariable**.</span><span class="sxs-lookup"><span data-stu-id="7d173-116">This activity specifies two template variables of type **publisherVariable** and **linkVariable**.</span></span> <span data-ttu-id="7d173-117">**publisherVariable** указывает человека, который опубликовано действия элемента веб-канала и **linkVariable** Дополнительные сведения (указывается **имя**, **текст**и **значение** дочерние элементы **linkVariable**) о записи блога.</span><span class="sxs-lookup"><span data-stu-id="7d173-117">**publisherVariable** specifies the person who published the activity feed item, and **linkVariable** includes further information (specified by the **name**, **text**, and **value** child elements of **linkVariable**) about the blog post.</span></span>
    
<span data-ttu-id="7d173-118">Каждое из четырех действий указывает **идентификатор шаблона** , которое соответствует одной из трех шаблонов, заданный элементом **шаблонов** .</span><span class="sxs-lookup"><span data-stu-id="7d173-118">Each of the four activities specifies a **templateID** value, which matches one of the three templates specified by the **templates** element.</span></span> <span data-ttu-id="7d173-119">В каждый шаблон находится в свой собственный элемент **activityTemplateContainer** , определяемый значение **идентификатор шаблона** , также используется для отображения на действие, которое имеет то же значение **идентификатор шаблона** .</span><span class="sxs-lookup"><span data-stu-id="7d173-119">Each template is in its own **activityTemplateContainer** element, identified by a **templateID** value that is also used to display an activity that has the same **templateID** value.</span></span> 
  
<span data-ttu-id="7d173-120">Подробное описание элементов XML, используемые в этом примере в следующих разделах:</span><span class="sxs-lookup"><span data-stu-id="7d173-120">For a detailed description of the XML elements used in the example, see the following topics:</span></span> 
  
- [<span data-ttu-id="7d173-121">Общие сведения о XML-код для действия элемента веб-канала</span><span class="sxs-lookup"><span data-stu-id="7d173-121">Overview of XML for an Activity Feed Item</span></span>](overview-of-xml-for-an-activity-feed-item.md)
    
- [<span data-ttu-id="7d173-122">activityDetails элемент</span><span class="sxs-lookup"><span data-stu-id="7d173-122">activityDetails Element</span></span>](activitydetails-element.md)
    
- [<span data-ttu-id="7d173-123">activityTemplateContainer элемент</span><span class="sxs-lookup"><span data-stu-id="7d173-123">activityTemplateContainer Element</span></span>](activitytemplatecontainer-element.md)
    
- [<span data-ttu-id="7d173-124">Переменные шаблона</span><span class="sxs-lookup"><span data-stu-id="7d173-124">Template Variables</span></span>](template-variables.md)
    
## <a name="xml-example"></a><span data-ttu-id="7d173-125">Пример XML-файла</span><span class="sxs-lookup"><span data-stu-id="7d173-125">XML example</span></span>

<span data-ttu-id="7d173-126">В следующем примере показано **activityFeed** XML четыре действия: два профиля обновления изображения, обновление состояния и запись блога.</span><span class="sxs-lookup"><span data-stu-id="7d173-126">The following example shows the **activityFeed** XML of four activities: two profile picture updates, a status update, and a blog post.</span></span> <span data-ttu-id="7d173-127">XML-код также приведены три активности шаблоны отображения для отображения соответствующими действиями.</span><span class="sxs-lookup"><span data-stu-id="7d173-127">The XML also specifies three activity display templates for displaying the corresponding activities.</span></span> 
  
```XML
<?xml version="1.0" encoding="utf-8"?>
<activityFeed xmlns="https://schemas.microsoft.com/office/outlook/2010/06/socialprovider.xsd">
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

## <a name="see-also"></a><span data-ttu-id="7d173-128">См. также</span><span class="sxs-lookup"><span data-stu-id="7d173-128">See also</span></span>

- [<span data-ttu-id="7d173-129">Примеры XML поставщика OSC</span><span class="sxs-lookup"><span data-stu-id="7d173-129">OSC Provider XML Examples</span></span>](osc-provider-xml-examples.md)  
- [<span data-ttu-id="7d173-130">XML-код для действия</span><span class="sxs-lookup"><span data-stu-id="7d173-130">XML for Activities</span></span>](xml-for-activities.md) 
- [<span data-ttu-id="7d173-131">Пример возможности XML</span><span class="sxs-lookup"><span data-stu-id="7d173-131">Capabilities XML Example</span></span>](capabilities-xml-example.md)  
- [<span data-ttu-id="7d173-132">Пример XML друзей</span><span class="sxs-lookup"><span data-stu-id="7d173-132">Friends XML Example</span></span>](friends-xml-example.md)
- [<span data-ttu-id="7d173-133">Схема XML поставщика Outlook Social Connector</span><span class="sxs-lookup"><span data-stu-id="7d173-133">Outlook Social Connector Provider XML Schema</span></span>](outlook-social-connector-provider-xml-schema.md)

