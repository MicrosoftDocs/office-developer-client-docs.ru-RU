---
title: Элемент Page (Pages_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 6e4ac41f-3855-05d8-e659-02c265b8750c
description: Содержит элементы, определяющие страницу в документе.
ms.openlocfilehash: f32cf3ed7bbf1e68ddca3fc8f5a1c50ce45fe73e
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538027"
---
# <a name="page-element-pages_type-complextype-visio-xml"></a>Элемент Page (Pages_Type complexType) (Visio XML)

Содержит элементы, определяющие страницу в документе.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Page_Type](page_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |pages.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Page" type="Page_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Pages](pages-elementvisio-xml.md) <br/> |[Pages_Type](pages_type-complextypevisio-xml.md) <br/> |Содержит элементы **Page** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[PageSheet](pagesheet-element-page_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие лист страницы для **элемента Page.**  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Общие сведения  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Флаг, указывающий, является ли страница фоновой.  <br/> |Значения типа xsd:boolean.  <br/> |
|BackPage  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД фоновой страницы этой страницы.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ИД элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|IsCustomName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, было ли имя настроено пользователем.  <br/> |Значения типа xsd:Boolean.  <br/> |
|IsCustomNameU  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, настроено ли пользователем универсальное имя.  <br/> |Значения типа xsd:Boolean.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|ReviewerID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД проверяемого, связанного с наложением разметки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ViewCenterX  <br/> |xsd:double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** указывают центр на странице, которая предполагается новым представлением (окном) при его первоначальном просмотре.  <br/> |Значения типа xsd:double.  <br/> |
|ViewCenterY  <br/> |xsd:double  <br/> |необязательный  <br/> |**ViewCenterX** и **ViewCenterY** указывают центр на странице, которая предполагается новым представлением (окном) при его первоначальном просмотре.  <br/> |Значения типа xsd:double.  <br/> |
|ViewScale  <br/> |xsd:double  <br/> |необязательный  <br/> |Коэффициент увеличения по умолчанию, который используется при открытом новом представлении (окне) страницы. Например, 1 = 100%; 1,5 = 150 % и так далее.  <br/> |Значения типа xsd:double.  <br/> |
   

