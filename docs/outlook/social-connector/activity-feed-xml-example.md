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
# <a name="activity-feed-xml-example"></a>Пример XML-канала активности

Пример XML в этом разделе — это строка XML веб-канала активности, возвращаемая Outlook Social Connector (OSC) после вызова метода [ISocialSession2:: жетактивитиесекс](isocialsession2-getactivitiesex.md) для социальной сети. 
  
В этом примере показан XML-код **activityFeed** , который содержит следующие четыре действия, разделенных элементом **activityDetails** и сопоставленный с шаблоном для целей отображения: 
  
- Изображение профиля обновляется с помощью Мелисса Макбес, **овнерид** в социальной сети — 4667647. Это действие указывает три переменные шаблона типа **публишервариабле**, **листвариабле**и **пиктуревариабле** (которая заключена в **листвариабле**). В этих переменных указывается пользователь, который опубликовал элемент веб-канала активности, и сведения для обновляемого изображения (с помощью дочерних элементов **Name**, **value**, **алттекст**и **href** объекта **пиктуревариабле**).
    
- Фотография профиля обновляется Майкла Аффронти, чьи **овнерид** в социальной сети — 5015012. Как и при последнем действии, это действие указывает три переменные шаблона типа **публишервариабле**, **листвариабле**и **пиктуревариабле**. В этих переменных указывается пользователь, который опубликовал элемент веб-канала активности и сведения для обновляемого изображения.
    
- В результате обновления состояния Майкл Аффронти отображается то же самое **овнерид** , что и в последнем действии 5015012. Это действие задает две переменные шаблона типа **публишервариабле** и **текствариабле**. **публишервариабле** указывает пользователя, опубликовавшего элемент веб-канала активности, и **текствариабле** содержит **значение** строки состояния`is hiking on Mount Rainier this weekend!`
    
- Запись блога Майкла Аффронти, в которой показано одно и то же **овнерид** в 5015012 как два последних действия. Это действие задает две переменные шаблона типа **публишервариабле** и **линквариабле**. **публишервариабле** указывает пользователя, который опубликовал элемент веб-канала активности, и **линквариабле** содержит дополнительные сведения (задаются с помощью дочерних элементов " **имя**", " **текст**" и " **значение** " в **линквариабле**) о записи блога.
    
Каждое из четырех действий указывает значение **templateID** , которое соответствует одному из трех шаблонов, указанных в элементе Templates **** . Каждый шаблон находится в отдельном элементе **activityTemplateContainer** , определяемом значением **templateID** , который также используется для отображения действия с тем же значением **templateID** . 
  
Подробное описание элементов XML, используемых в примере, представлено в следующих разделах: 
  
- [Обзор XML-файла для элемента веб-канала активности](overview-of-xml-for-an-activity-feed-item.md)
    
- [Элемент activityDetails](activitydetails-element.md)
    
- [Элемент activityTemplateContainer](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
## <a name="xml-example"></a>Пример XML

В следующем примере показан XML-файл **activityFeed** из четырех действий: два обновления изображения профиля, обновление состояния и запись блога. В XML-коде также задаются три шаблона отображения действий для отображения соответствующих действий. 
  
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

- [Примеры XML-кода поставщика OSC](osc-provider-xml-examples.md)  
- [XML для действий](xml-for-activities.md) 
- [Пример XML-кода возможностей](capabilities-xml-example.md)  
- [Пример XML-кода друзей](friends-xml-example.md)
- [Схема XML поставщика социальных соединителей Outlook](outlook-social-connector-provider-xml-schema.md)

