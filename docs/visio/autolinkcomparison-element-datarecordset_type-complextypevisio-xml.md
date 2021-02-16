---
title: Элемент AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе DataRecordset с элементом данных фигуры из последнего успешного действия автоматического связывания, выполненного в пользовательском интерфейсе.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537873"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>Элемент AutoLinkComparison (DataRecordSet_Type complexType) (Visio XML)

Определяет правило, которое сравнивает столбец в родительском элементе **DataRecordset** с элементом данных фигуры из последнего успешного действия автоматического связывания, выполненного в пользовательском интерфейсе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Указывает набор записей и привязку данных между этим набором записей и фигурами на страницах рисования.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |xsd:string  <br/> |Обязательный  <br/> |Соответствует имени столбца в наборе записей ADO.  <br/> |Значения типа xsd:string.  <br/> |
|ContextType  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Указывает свойства группы или фигуры, которые необходимо использовать для сравнения. Возможные значения показаны в следующей таблице.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |xsd:string  <br/> |необязательный  <br/> |Если значение ContextType — 2 или 3, этот атрибут необходим для определения сравнения. Для ContextType = 2 ContextTypeLabel должен быть меткой элемента данных фигуры, а если **ContextType** = 3, ContextTypeLabel должен быть локальным именем строки.  <br/> |Значения типа xsd:string.  <br/> |
   

