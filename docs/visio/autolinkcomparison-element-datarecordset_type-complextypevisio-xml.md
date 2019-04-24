---
title: Элемент Аутолинккомпарисон (Датарекордсет_типе complexType) (' Visio XML ')
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.
ms.openlocfilehash: 474acc4c1d259621881ea498decfeaf18b69809e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32338320"
---
# <a name="autolinkcomparison-element-datarecordsettype-complextype-visio-xml"></a>Элемент Аутолинккомпарисон (Датарекордсет_типе complexType) (' Visio XML ')

Определяет правило, которое сравнивает столбец в родительском элементе данных **** фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[Аутолинккомпарисон_типе](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[Датарекордсет_типе](datarecordset_type-complextypevisio-xml.md) <br/> |Задает набор записей и привязку данных между этим набором записей и фигурами на страницах документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Соответствует имени столбца в наборе записей ADO.  <br/> |Значения типа String: XSD.  <br/> |
|Контексттипе  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает свойства группы или фигуры, которые необходимо использовать для сравнения. Возможные значения показаны в приведенной ниже таблице.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Контексттипелабел  <br/> |XSD: строка  <br/> |необязательный  <br/> |Если значение Контексттипе равно 2 или 3, этот атрибут является обязательным для определения сравнения. Для Контексттипе = 2 Контексттипелабел должен быть меткой элемента данных Shape, а если **контексттипе** = 3, контексттипелабел должно быть именем локальной строки.  <br/> |Значения типа String: XSD.  <br/> |
   

