---
title: Основной элемент (Masters_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Содержит элементы, определяющие шаблона для документа.
ms.openlocfilehash: f6effa521b7c5ea69d41b6770ee2dbef61af097c
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25400490"
---
# <a name="master-element-masterstype-complextype-visio-xml"></a>Основной элемент (Masters_Type complexType) ('Visio XML»)

Содержит элементы, определяющие шаблона для документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |Masters.XML  <br/> |
   
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
|[Образцы](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Содержит **главные** элементы для документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Осуществляет подключение](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **подключение** для каждого подключения между двумя фигурами в документе.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Указывает, что кодировке MIME (Multipurpose Internet Mail Extensions) двоичные значок (в формате .ico) для **главной** или **MasterShortcut** элемент в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие таблице страницы для **страницы** или **шаблона** элемента.  <br/> |
|Фигуры  <br/> |Shapes_Type  <br/> |Содержит коллекцию элементов **фигуры** .  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выравнивается по левой, правой, основной текст в окне набор элементов или центра обработки.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|BaseID  <br/> |XSD:String  <br/> |необязательный  <br/> |GUID (глобальный уникальный идентификатор), который определяет основной для документов.  <br/> |Значения типа xsd:string.  <br/> |
|Hidden  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, скрыто ли основной в пользовательском интерфейсе.  <br/> |Значения типа xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, создается ли автоматически значок из сам образец.  <br/> |Значения типа xsd:boolean.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Уникальный идентификатор элемента в рамках родительского элемента.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Определяет, как Microsoft Visio решает, если главный документ не указан при создании экземпляра главный удаленной на странице документа.  <br/> |Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |XSD:String  <br/> |необязательный  <br/> |Универсальные имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, будет ли шаблон ведет себя как пользовательский шаблон.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Запрос  <br/> |XSD:String  <br/> |необязательный  <br/> |Строка состояния и средство запроса подсказки для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|Уникальный идентификатор  <br/> |XSD:String  <br/> |необязательный  <br/> |Идентификатор GUID, определяющий образец в документе.  <br/> |Значения типа xsd:string.  <br/> |
   

