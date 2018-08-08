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
ms.openlocfilehash: ab27ddfad5044994a19bb32759994a0e98c39ae6
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19812701"
---
# <a name="activity-feed-xml-example"></a>Пример XML веб-канала активности

В примере XML в этом разделе приведен XML строки, возвращаемой в Outlook Social Connector (OSC) после его вызывает метод [ISocialSession2::GetActivitiesEx](isocialsession2-getactivitiesex.md) для социальных сетей веб-канала активности. 
  
В примере показано **activityFeed** XML, который содержит следующие четыре действия, каждый отделяются элемент **activityDetails** и соответствующий шаблон для отображения в целях: 
  
- Изображение профиля обновление с Melissa Macbeth, чьи **ownerID** социальные сети — это 4667647. Это действие задает три переменные шаблона типа **publisherVariable**, **listVariable**и **pictureVariable** (заключенное в **listVariable**). Эти переменные укажите человека, который публикации веб-канал элемента и сведения о изображение, чтобы обновить (с помощью дочерние элементы **pictureVariable** **имя**, **значение**, **altText**и **href** ) активности.
    
- Изображение профиля обновить, Майкл Affronti, чьи **ownerID** социальные сети — это 5015012. Как и последнее действие, это действие задает три переменные шаблона типа **publisherVariable**, **listVariable**и **pictureVariable**. Эти переменные укажите человека, который публикации веб-канал элемента и данные рисунка, который требуется обновить активности.
    
- Обновление состояния, Майкл Affronti, отражающая же **ownerID** из 5015012 как последнего действия. Это действие задает две переменные шаблона типа **publisherVariable** и **textVariable**. **publisherVariable** указывает человека, который публикации веб-канал элементов активности и **textVariable** содержит **значение** из строки состояния`is hiking on Mount Rainier this weekend!`
    
- Публикация в блоге, Майкл Affronti, отражающая же **ownerID** из 5015012 как последние два действия. Это действие задает две переменные шаблона типа **publisherVariable** и **linkVariable**. **publisherVariable** указывает человека, который опубликовано действия элемента веб-канала и **linkVariable** Дополнительные сведения (указывается **имя**, **текст**и **значение** дочерние элементы **linkVariable**) о записи блога.
    
Каждое из четырех действий указывает **идентификатор шаблона** , которое соответствует одной из трех шаблонов, заданный элементом **шаблонов** . В каждый шаблон находится в свой собственный элемент **activityTemplateContainer** , определяемый значение **идентификатор шаблона** , также используется для отображения на действие, которое имеет то же значение **идентификатор шаблона** . 
  
Подробное описание элементов XML, используемые в этом примере в следующих разделах: 
  
- [Общие сведения о XML-код для действия элемента веб-канала](overview-of-xml-for-an-activity-feed-item.md)
    
- [activityDetails элемент](activitydetails-element.md)
    
- [activityTemplateContainer элемент](activitytemplatecontainer-element.md)
    
- [Переменные шаблона](template-variables.md)
    
## <a name="xml-example"></a>Пример XML-файла

В следующем примере показано **activityFeed** XML четыре действия: два профиля обновления изображения, обновление состояния и запись блога. XML-код также приведены три активности шаблоны отображения для отображения соответствующими действиями. 
  
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</value>
              <altText>Melissa Macbeth</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103873861033</href>
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="listVariable">
          <name>ProfilePhoto</name>
          <listItems>
            <simpleTemplateVariable type="pictureVariable">
              <name>Photo</name>
              <value>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</value>
              <altText>Michael Affronti</altText>
              <href>http://office.microsoft.com/global/images/default.aspx?assetid=ZA103895491033</href>
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
          <profileUrl>http://www.contoso.com</profileUrl>
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
          <profileUrl>http://www.contoso.com/</profileUrl>
        </templateVariable>
        <templateVariable type="linkVariable">
          <name>blogPost</name>
          <text>Connect your Inbox to Facebook and Windows Live with the Outlook Social Connector</text>
          <value>http://blogs.office.com/b/office_blog/archive/2010/07/13/connect-to-facebook-and-windows-live-with-the-outlook-social-connector.aspx</value>
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
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>2</templateID>
      <activityTemplate>
        <type>Status Update</type>
        <title>{publisher:Publisher}: {text:statusText}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
    <activityTemplateContainer>
      <applicationID>2</applicationID>
      <templateID>3</templateID>
      <activityTemplate>
        <type>Other</type>
        <title>{publisher:Publisher} wrote a new blog post {link:blogPost}</title>
                <data></data>
        <icon>http://www.microsoft.com/about/images/rss_button.gif</icon>
      </activityTemplate>
    </activityTemplateContainer>
  </templates>
</activityFeed>

```

## <a name="see-also"></a>См. также

- [Примеры XML поставщика OSC](osc-provider-xml-examples.md)  
- [XML-код для действия](xml-for-activities.md) 
- [Пример возможности XML](capabilities-xml-example.md)  
- [Пример XML друзей](friends-xml-example.md)
- [Схема XML поставщика Outlook Social Connector](outlook-social-connector-provider-xml-schema.md)

