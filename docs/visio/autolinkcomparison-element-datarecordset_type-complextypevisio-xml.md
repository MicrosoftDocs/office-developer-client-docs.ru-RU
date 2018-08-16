---
title: Элемент AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Задает правило, которое представлено сравнение столбцов в родительском элементе записей данных с помощью элемента данных фигуры из последней успешной автоматического связывания действия, выполняемые в пользовательском интерфейсе.
ms.openlocfilehash: 38970a84676f769c36c9bdc3f8334652f7d9ec21
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813177"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Элемент AutoLinkComparison (DataRecordSet_Type complexType) ('Visio XML»)

Задает правило, которое представлено сравнение столбцов в родительском элементе **записей данных** с помощью элемента данных фигуры из последней успешной автоматического связывания действия, выполняемые в пользовательском интерфейсе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
<xs:element name="AutoLinkComparison" type="AutoLinkComparison_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Записей данных](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Задает набор записей и привязки данных между этого набора записей и фигур в страницы документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD:String  <br/> |Обязательный  <br/> |Соответствует имени столбца в записей ADO.  <br/> |Значения типа xsd:string.  <br/> |
|ContextType  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Задает свойства группы или фигуры, используется для сравнения. В следующей таблице показаны возможные значения.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ContextTypeLabel  <br/> |XSD:String  <br/> |необязательный  <br/> |Если значение ContextType 2 или 3, этот атрибут требуется для определения сравнение. ContextType = 2, ContextTypeLabel должна быть метка элемента данных фигуры и если **ContextType** = 3, ContextTypeLabel должно быть имя локального строки.  <br/> |Значения типа xsd:string.  <br/> |
   
