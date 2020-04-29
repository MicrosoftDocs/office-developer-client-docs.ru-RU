---
title: Элемент DataColumn (DataColumns_Type complexType) (XML для Visio)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: 92469c2f-f809-dff2-d0ee-b3b8f75083d2
description: Определяет, как столбец данных отображается в окне "внешние данные" в пользовательском интерфейсе Visio, и определяет данные в столбце, определяя тип данных и форматирование.
ms.openlocfilehash: 021e7ffd154f1e124b9eb163acc27260b90c23eb
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34541227"
---
# <a name="datacolumn-element-datacolumns_type-complextype-visio-xml"></a>Элемент DataColumn (DataColumns_Type complexType) (XML для Visio)

Определяет, как столбец данных отображается в окне " **Внешние данные** " в пользовательском интерфейсе Visio, и определяет данные в столбце, определяя тип данных и форматирование. 
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataColumn_Type](datacolumn_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15. xsd  <br/> |
|**Части документа** <br/> |Recordset. XML  <br/> |
   
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
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Содержит все элементы **DataColumn** в наборе данных данных.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

Нет.
  
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Календарь  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |ИДЕНТИФИКАТОР календаря для столбца данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|колумннамеид  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Внешнее имя столбца данных. Отображается в заголовках окна " **Внешние данные** " и "метки в рисунках данных".  <br/> |Значения типа String: XSD.  <br/> |
|Денежный  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |ИДЕНТИФИКАТОР валюты столбца данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|DataType  <br/> |xsd:unsignedShort  <br/> |необязательный  <br/> |Тип данных в столбце данных.  <br/> |Значения для типа xsd:unsignedShort.  <br/> |
|Degree  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Задает степень (степень) единиц измерения (например, квадрат или куб). Значение по умолчанию (Attribute отсутствует) равно 1.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|дисплайордер  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Определяет позицию отображения столбца данных в окне **Внешние данные** от левого столбца (0) до крайнего правого столбца (наибольшее значение).  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|дисплайвидс  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Ширина столбца данных в окне " **Внешние данные** ".  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Hyperlink  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Создает ли столбец данных гиперссылку в фигуре, когда фигура связана с данными.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Label  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Метка столбца данных.  <br/> |Значения типа String: XSD.  <br/> |
|LangID  <br/> |XSD: Унсигнединт  <br/> |необязательный  <br/> |Идентификатор языка столбца данных.  <br/> |Значения типа XSD: Унсигнединт.  <br/> |
|Распределен  <br/> |XSD: Boolean  <br/> |необязательный  <br/> |Указывает, отображается ли столбец в окне " **Внешние данные** ". Значение true (1), если столбец должен быть видимым; Значение false (0), чтобы столбец не отображался. Значение по умолчанию (атрибут отсутствует) предназначено для отображения столбца.  <br/> |Значения типа XSD: Boolean.  <br/> |
|Имя  <br/> |XSD: строка  <br/> |Обязательный  <br/> |Внутреннее имя столбца данных. Используется в качестве имени строки для элемента данных Shape (настраиваемое свойство), добавленного к фигуре, когда фигура связана со строкой данных.  <br/> |Значения типа String: XSD.  <br/> |
|ориглабел  <br/> |XSD: строка  <br/> |необязательный  <br/> |Метка столбца, возвращаемая в Visio базовым интерфейсом ADO.  <br/> |Значения типа String: XSD.  <br/> |
|униттипе  <br/> |XSD: строка  <br/> |необязательный  <br/> |Тип единицы данных в столбце данных.  <br/> |Значения типа String: XSD.  <br/> |
   

