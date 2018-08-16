---
title: Элемент DataColumn (DataColumns_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Определяет, как столбец данных отображается в окне внешних данных в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования.
ms.openlocfilehash: f74061b9f3b8f4b93d8aa0e97e4e7c1e45131cbd
ms.sourcegitcommit: 9d60cd82b5413446e5bc8ace2cd689f683fb41a7
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 06/11/2018
ms.locfileid: "19813557"
---
# <a name="datacolumn-element-datacolumnstype-complextype-visio-xml"></a>Элемент DataColumn (DataColumns_Type complexType) ('Visio XML»)

Определяет, как столбец данных отображается в окне **Внешних данных** в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataColumn" type="DataColumn_Type" minOccurs="1" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если схема определяет специальные требования, такие как **последовательность**, **minOccurs**, **maxOccurs**и **выбора**, обратитесь к разделу определение. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[Объектам DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Содержит все элементы **DataColumn** в записей данных.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательное**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Календарь  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Идентификатор календаря столбец данных.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|ColumnNameID  <br/> |XSD:String  <br/> |Обязательный  <br/> |Внешнее имя столбца данных. Отображается в заголовке окна **Внешних данных** и в метки в связанных с данными.  <br/> |Значения типа xsd:string.  <br/> |
|Денежный  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Идентификатор валюты столбец данных.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|DataType  <br/> |XSD:unsignedShort  <br/> |необязательный  <br/> |Тип данных в столбце.  <br/> |Значения типа xsd:unsignedShort.  <br/> |
|Степень  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Задает степень единиц измерения, например квадрат или кубе (power). Значение по умолчанию (атрибут отсутствует) — 1.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DisplayOrder  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Определяет положение столбец данных в окно **Внешних данных** из самый левый столбец (0) до правого столбца (наибольшее значение).  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|DisplayWidth  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Ширина столбца данных в окно **Внешних данных** .  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Гиперссылка  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Является ли столбец данных создает гиперссылки в фигуры при фигуры, связанная с данными.  <br/> |Значения типа xsd:boolean.  <br/> |
|Метка  <br/> |XSD:String  <br/> |Обязательный  <br/> |Заголовок столбца данных.  <br/> |Значения типа xsd:string.  <br/> |
|LangID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Идентификатор языка столбец данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Сопоставленные  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Указывает, видима ли столбец в окно **Внешних данных** . Значение true (1) для столбца должна быть видна; False (0) для столбца не должен быть виден. Значение по умолчанию (атрибут отсутствует) — для столбца должна быть видна.  <br/> |Значения типа xsd:boolean.  <br/> |
|Имя  <br/> |XSD:String  <br/> |Обязательный  <br/> |Внутреннее имя столбца данных. Используется в качестве имя строки для элемента данных фигуры (настраиваемое свойство), добавить фигуры, если фигуры является связана со строкой данных.  <br/> |Значения типа xsd:string.  <br/> |
|OrigLabel  <br/> |XSD:String  <br/> |необязательный  <br/> |Названия столбцов, возвращаемых основной интерфейс ADO для Visio.  <br/> |Значения типа xsd:string.  <br/> |
|UnitType  <br/> |XSD:String  <br/> |необязательный  <br/> |Тип данных в столбце единицы.  <br/> |Значения типа xsd:string.  <br/> |
   
