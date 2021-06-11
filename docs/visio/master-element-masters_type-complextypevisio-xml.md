---
title: Элемент Master (Masters_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: c102fd71-c621-2bde-9fbb-8e9203fdf31e
description: Содержит элементы, определяющие мастер документа.
ms.openlocfilehash: 83727b89eaf44aae5dddecacff1f05f369ee0bf0
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34538048"
---
# <a name="master-element-masters_type-complextype-visio-xml"></a>Элемент Master (Masters_Type ComplexType) (Visio XML)

Содержит элементы, определяющие мастер документа.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Master_Type](master_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |masters.xml  <br/> |
   
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
|[Masters](masters-elementvisio-xml.md) <br/> |[Masters_Type](masters_type-complextypevisio-xml.md) <br/> |Содержит **основные** элементы документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Connects](connects-element-pagecontents_type-complextypevisio-xml.md) <br/> |[Connects_Type](connects_type-complextypevisio-xml.md) <br/> |Содержит элемент **Подключение** для каждого подключения между двумя фигурами в рисунке.  <br/> |
|[Icon](icon-element-master_type-complextypevisio-xml.md) <br/> |[Icon_Type](icon_type-complextypevisio-xml.md) <br/> |Указывает кодированный двоичный значок MIME (Multipurpose Internet Mail Extensions) (в формате .ico) для элемента **Master** или **MasterShortcut** в документе.  <br/> |
|[PageSheet](pagesheet-element-master_type-complextypevisio-xml.md) <br/> |[PageSheet_Type](pagesheet_type-complextypevisio-xml.md) <br/> |Содержит элементы, определяющие лист страницы для **элемента Page** или **Master.**  <br/> |
|Фигуры  <br/> |Shapes_Type  <br/> |Содержит коллекцию **элементов Shape.**  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|AlignName  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Указывает, выравнивается ли текст мастера в окне трафарета слева, справа или в центре.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|BaseID  <br/> |xsd:string  <br/> |необязательный  <br/> |GUID (глобальный уникальный идентификатор), который определяет мастер по документам.  <br/> |Значения типа xsd:string.  <br/> |
|Hidden  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, скрыт ли мастер в пользовательском интерфейсе.  <br/> |Значения типа xsd:boolean.  <br/> |
|IconSize  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Размер значка элемента.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|IconUpdate  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, создается ли значок автоматически из самого мастера.  <br/> |Значения типа xsd:boolean.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный ID элемента в родительском элементе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|MatchByName  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Определяет, как корпорация Майкрософт Visio, если мастер документа уже присутствует при отброшении экземпляра мастера на страницу рисования.  <br/> |Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|NameU  <br/> |xsd:string  <br/> |необязательный  <br/> |Универсальное имя элемента.  <br/> |Значения типа xsd:string.  <br/> |
|PatternFlags  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Определяет, ведет ли мастер себя как настраиваемый шаблон.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Prompt  <br/> |xsd:string  <br/> |необязательный  <br/> |Подсказка панели состояния и подсказки инструмента для элемента.  <br/> |Значения типа xsd:string.  <br/> |
|UniqueID  <br/> |xsd:string  <br/> |необязательный  <br/> |GUID, идентифицирует мастера в документе.  <br/> |Значения типа xsd:string.  <br/> |
   

