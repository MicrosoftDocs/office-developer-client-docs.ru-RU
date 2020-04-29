---
title: Элемент Аутолинккомпарисон (DataRecordSet_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: af5eb7fd-89c6-49bf-4e45-431b63d6cd6a
description: Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры с элементом данных фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе.
ms.openlocfilehash: 7d25d12844fe33ec1f1abb66984c5be40c4995c3
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34537873"
---
# <a name="autolinkcomparison-element-datarecordset_type-complextype-visio-xml"></a>Элемент Аутолинккомпарисон (DataRecordSet_Type complexType) (XML для Visio)

Определяет правило, которое сравнивает столбец в родительском элементе данных фигуры **с элементом данных** фигуры из последнего успешного действия автоматического связывания, выполняемого в пользовательском интерфейсе. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
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
|[DataRecordSet](datarecordset-element-datarecordsets_type-complextypevisio-xml.md) <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |Задает набор записей и привязку данных между этим набором записей и фигурами на страницах документа.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|ColumnName  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Соответствует имени столбца в наборе записей ADO.  <br/> |Значения типа String: XSD.  <br/> |
|контексттипе  <br/> |XSD: Унсигнединт  <br/> |Обязательный  <br/> |Задает свойства группы или фигуры, которые необходимо использовать для сравнения. Возможные значения показаны в приведенной ниже таблице.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|контексттипелабел  <br/> |XSD: строка  <br/> |необязательный  <br/> |Если значение Контексттипе равно 2 или 3, этот атрибут является обязательным для определения сравнения. Для Контексттипе = 2 Контексттипелабел должен быть меткой элемента данных Shape, а если **контексттипе** = 3, контексттипелабел должно быть именем локальной строки.  <br/> |Значения типа String: XSD.  <br/> |
   

