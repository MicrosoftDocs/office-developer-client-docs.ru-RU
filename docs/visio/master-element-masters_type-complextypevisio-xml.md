---
title: Элемент Master (Masters_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Содержит элементы, определяющие основные элементы для документа.
ms.openlocfilehash: 83727b89eaf44aae5dddecacff1f05f369ee0bf0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538048"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Элемент Master (Masters_Type complexType) (Visio XML)

Содержит элементы, определяющие основные элементы для документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |masters.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="Master" type="Master_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Содержит элементы **Master** для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **Connect** для каждого подключения между двумя фигурами в документе.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Указывает двоичный значок MIME (multipurpose Internet Mail Extensions) в формате ICO для элемента **Master** или **MasterShortcut** в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие лист страницы для **элемента Page** или **Master.**  <br/> |
|Фигуры  <br/> |Shapes_Type  <br/> |Содержит коллекцию **элементов Shape.**  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выравнивается ли текст хозяина в окне трафарета влево, вправо или по центру.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |необязательный  <br/> |GUID (глобальный уникальный идентификатор), который идентифицирует хозяина в документах.  <br/> |Значения типа xsd:string.  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, скрыт ли хозяин в пользовательском интерфейсе.  <br/> |Значения типа xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, создается ли значок автоматически из самого хозяина.  <br/> |Значения типа xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ИД элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Определяет, как Microsoft Visio определяет, присутствует ли уже хозяин документа при отброшении экземпляра хозяина на страницу документа.  <br/> |Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, ведет ли образец поведение в качестве пользовательского шаблона.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |необязательный  <br/> |Подсказка о состоянии и подсказка для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |GUID, идентифицирует хозяина в документе.  <br/> |Значения типа xsd:string.  <br/> |
   

