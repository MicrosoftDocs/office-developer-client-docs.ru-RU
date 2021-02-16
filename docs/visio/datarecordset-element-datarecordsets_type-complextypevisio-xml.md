---
title: Элемент DataRecordSet (DataRecordSets_Type complexType) (Visio XML)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Хранит, форматирует, обновляет и предоставляет данные, запрашиваемые из базы данных в Microsoft Visio.
ms.openlocfilehash: e478593f370968db5fe9a65329cb1928c0f7c6ea
ms.sourcegitcommit: e7b38e37a9d79becfd679e10420a19890165606d
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 05/29/2019
ms.locfileid: "34539679"
---
# <a name="datarecordset-element-datarecordsets_type-complextype-visio-xml"></a>Элемент DataRecordSet (DataRecordSets_Type complexType) (Visio XML)

Хранит, форматирует, обновляет и предоставляет данные, запрашиваемые из базы данных в Microsoft Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |http://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.xml  <br/> |
   
## <a name="definition"></a>Определение

```XML
< xs:element name="DataRecordSet" type="DataRecordSet_Type" minOccurs="0" maxOccurs="unbounded" >
</xs:element >
```

## <a name="elements-and-attributes"></a>Элементы и атрибуты

Если в схеме определяются конкретные требования, например **sequence**, **minOccurs**, **maxOccurs** и **choice**, см. раздел определений. 
  
### <a name="parent-elements"></a>Родительские элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Содержит все **элементы DataRecordset** в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Содержит XML,соответствующий классической схеме XML ADO для наборов записей ADO и описывая данные в наборе записей данных.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Определяет правило, которое сравнивает столбец в родительском элементе **DataRecordset** с элементом данных фигуры из последнего успешного действия автоматического связывания, выполненного в пользовательском интерфейсе.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Определяет, как столбец данных  отображается в окне внешних данных в пользовательском интерфейсе Visio, и квалификаторирует данные в столбце, определяя его тип данных и форматирование.  <br/> |
|[DataColumns](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Содержит все **элементы DataColumn** в наборе записей данных.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Определяет один или несколько столбцов первичного ключа в наборе записей данных.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Указывает строку в наборе записей данных, связанную с фигурой, которая находится в конфликте после обновления наборов записей данных.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Сопописывая строка наборов данных с фигурой.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Контрольная сумма  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Значение контрольной суммы, сгенерированное Visio и основанное на свойствах наборов записей данных. Установите для этого attirbute 0; Visio пересчитает это значение во время работы.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Команда  <br/> |xsd:string  <br/> |необязательный  <br/> |Строка команды, используемая для запроса данных из источника данных.  <br/> |Значения типа xsd:string.  <br/> |
|ConnectionID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |ИД подключения для связанного **объекта DataConnection.** Не существует для источников данных XML.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |xsd:unsignedInt  <br/> |Обязательный  <br/> |Уникальный в документе ИД наборов записей данных.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |xsd:string  <br/> |необязательный  <br/> |Отображаемого (или "удобного") имени для наборов записей данных.  <br/> |Значения типа xsd:string.  <br/> |
|NextRowID  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Следующий доступный ИД строки Visio.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Параметры  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Параметры для применения к набору записей данных. Возможные значения могут быть любым сочетанием одного или нескольких из них, показанных в следующей таблице.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Как часто (в минутах) Visio автоматически обновляет набор записей данных. Это значение должно быть 1 или больше.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Следует ли отключить пользовательский интерфейс выверки данных. True (1) для отключения пользовательского интерфейса. False (0), чтобы включить пользовательский интерфейс.  <br/> |Значения типа xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Следует ли переописывать изменения пользователя для элементов данных фигур в фигурах, связанных с данными при обновлении наборов записей данных.  <br/> |Значения типа xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |xsd:unsignedInt  <br/> |необязательный  <br/> |Определяет, как ссылки на данные фигур обрабатываются при копировании или вырезании фигур. 1 для замены существующих ссылок в целевой фигуре. 0 для сохранения существующих ссылок в целевой фигуре.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |xsd:boolean  <br/> |необязательный  <br/> |Следует ли использовать порядок строк в наборе записей данных в качестве первичного ключа. True (1), если ИД строки определяются порядком строки. Значение False (0), если ИД строки определяются значениями в столбцах первичного ключа в наборе записей данных.  <br/> |Значения типа xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |xsd:dateTime  <br/> |необязательный  <br/> |Дата и время последнего обновления наборов записей данных.  <br/> |Значения типа xsd:dateTime.  <br/> |
   

