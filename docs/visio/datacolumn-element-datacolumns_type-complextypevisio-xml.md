---
title: Элемент DataColumn (DataColumns_Type ComplexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Определяет, как столбец данных отображается в окне внешних данных в пользовательском интерфейсе Visio и квалифицирует данные в столбце, определяя его тип данных и форматирование.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541227"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>Элемент DataColumn (DataColumns_Type ComplexType) (Visio XML)

Определяет, как столбец данных  отображается в окне внешних данных в пользовательском интерфейсе Visio и квалифицирует данные в столбце, определяя его тип данных и форматирование. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документов** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Содержит все **элементы DataColumn** в наборе данных.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Календарь  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |ID календаря столбца данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |xsd:string  <br/> |Обязательный  <br/> |Внешнее имя столбца данных. Отображается в заголовках в окне **Внешние** данные и на метки в графике данных.  <br/> |Значения типа xsd:string.  <br/> |
|Денежный  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Currency ID столбца данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Тип данных в столбце данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Degree  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Указывает степень (мощность) единиц, например квадратную или кубовую. Значение по умолчанию (атрибут отсутствует) — 1.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Определяет положение столбца данных в окне **Внешние** данные от левого столбца (0) до столбца правой части (наибольшее значение).  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Ширина столбца данных в **окне Внешние** данные.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Hyperlink  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Создает ли столбец данных гиперссылку в форме, когда фигура связана с данными.  <br/> |Значения типа xsd:boolean.  <br/> |
|Выбор метки  <br/> |xsd:string  <br/> |Обязательный  <br/> |Метка столбца данных.  <br/> |Значения типа xsd:string.  <br/> |
|LangID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Языковой ID столбца данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Mapped  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Указывает, отображается ли столбец в окне **Внешние данные.** True (1) для видимого столбца; False (0), чтобы столбец не был виден. По умолчанию (отсутствующий атрибут) столбец должен быть видимым.  <br/> |Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |xsd:string  <br/> |Обязательный  <br/> |Внутреннее имя столбца данных. Используется в качестве имени строки для элемента shape-data (настраиваемого свойства), добавленного в форму, когда фигура связана с строкой данных.  <br/> |Значения типа xsd:string.  <br/> |
|OrigLabel  <br/> |xsd:string  <br/> |необязательный  <br/> |Метка столбцов возвращается Visio с помощью интерфейса ADO.  <br/> |Значения типа xsd:string.  <br/> |
|UnitType  <br/> |xsd:string  <br/> |необязательный  <br/> |Тип блока данных в столбце данных.  <br/> |Значения типа xsd:string.  <br/> |
   

