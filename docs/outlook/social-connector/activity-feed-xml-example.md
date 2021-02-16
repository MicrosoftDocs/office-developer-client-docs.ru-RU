---
title: Пример XML-канала активности
manager: soliver
ms.date: 11/16/2014
ms.audience: Developer
ms.topic: overview
ms.prod: office-online-server
localization_priority: Normal
ms.assetid: aa50ca36-8d01-4770-9d9c-30a5baa146ff
description: XML-пример в этом разделе — это XML-строка веб-канала активности, которая возвращается в Outlook Social Connector (OSC) после вызова метода ISocialSession2::GetActivitiesEx для социальной сети.
ms.openlocfilehash: bb8af45f25d8ee2897a3a01e2863466aeacec4e8
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538328"
---
# <a name="activity-feed-xml-example"></a>Пример XML-канала активности

XML-пример в этом разделе — это XML-строка веб-канала активности, которая возвращается в Outlook Social Connector (OSC) после вызова метода [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для социальной сети. 
  
В примере показан **XML-элемент activityFeed,** содержащий следующие четыре действия, каждое из которых состоит из элемента **activityDetails** и соответствует шаблону в целях отображения: 
  
- Обновление изображения профиля Юрисы Macbeth, чей **ownerID** в социальной сети — 4667647. Это действие указывает три переменные шаблона типов **publisherVariable,** **listVariable** и **pictureVariable** (которые заключены **в listVariable).** Эти переменные указывают человека, опубликовавшего элемент веб-канала активности, а также сведения об обновляемом рисунке (с использованием **имени,** **значения,** **altText** и **href-элементов** **pictureVariable).**
    
- Обновление изображения профиля Майкла Affronti, чей **ownerID** в социальной сети — 5015012. Аналогично последнему действию, это действие указывает три переменные шаблона типа **publisherVariable,** **listVariable** и **pictureVariable**. Эти переменные указывают человека, опубликовавшего элемент веб-канала активности, и сведения об обновляемом рисунке.
    
- Обновление состояния Майкла Affronti с тем же **ownerID** 5015012, что и последнее действие. Это действие указывает две переменные шаблона типа **publisherVariable** и **textVariable.** **publisherVariable** указывает человека, который опубликовал элемент веб-канала активности, а  **textVariable** включает значение строки состояния`is hiking on Mount Rainier this weekend!`
    
- Запись блога Майкла Affronti с тем же **ownerID** 5015012, что и последние два действия. Это действие указывает две переменные шаблона типа **publisherVariable** и **linkVariable.** **publisherVariable** указывает человека, опубликовавшего элемент веб-канала активности, а **linkVariable** включает дополнительные сведения (указанные по **имени,** тексту и значению элементов **linkVariable)** о записи блога. 
    
Каждое из четырех действий указывает значение **templateID,** которое соответствует одному из трех шаблонов, указанных элементом **шаблонов.** Каждый шаблон находится в отдельном элементе **activityTemplateContainer,** который определен значением **templateID,** которое также используется для отображения действия с тем же **значением templateID.** 
  
Подробное описание элементов XML, используемых в примере, см. в следующих темах: 
  
- [Обзор XML для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)
    
- [Элемент activityDetails](activitydetails-element.md)
    
- [Элемент activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
## <a name="xml-example"></a>Пример XML

В следующем примере показан **XML-xML activityFeed** из четырех действий: два обновления изображений профиля, обновление состояния и запись блога. XML также указывает три шаблона отображения действий для отображения соответствующих действий. 
  
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

## <a name="see-also"></a>См. также

- [XML-примеры поставщика OSC](osc-provider-xml-examples.md)  
- [XML для действий](xml-for-activities.md) 
- [XML-пример возможностей](capabilities-xml-example.md)  
- [Пример XML-разных друзей](friends-xml-example.md)
- [XML-схема поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

