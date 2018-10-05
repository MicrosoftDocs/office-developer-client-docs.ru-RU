---
title: Элемент записей данных (DataRecordSets_Type complexType) ('Visio XML»)
manager: soliver
ms.date: 03/09/2015
ms.audience: Developer
ms.topic: reference
localization_priority: Normal
ms.assetid: aa182f04-0899-ee0e-79e1-b74832933e83
description: Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.
ms.openlocfilehash: e2baaeed38318f35d4bd4ce4269f71b6304b148f
ms.sourcegitcommit: ef717c65d8dd41ababffb01eafc443c79950aed4
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 10/04/2018
ms.locfileid: "25387288"
---
# <a name="datarecordset-element-datarecordsetstype-complextype-visio-xml"></a>Элемент записей данных (DataRecordSets_Type complexType) ('Visio XML»)

Сохранение, форматы, обновляет и предоставляет доступ к данным из базы данных в Microsoft Visio.
  
## <a name="element-information"></a>Сведения об элементе

|||
|:-----|:-----|
|**Тип элемента** <br/> |[DataRecordSet_Type](datarecordset_type-complextypevisio-xml.md) <br/> |
|**Пространство имен** <br/> |https://schemas.microsoft.com/office/visio/2012/main  <br/> |
|**Файл схемы** <br/> |VisioSchema15.xsd  <br/> |
|**Части документа** <br/> |recordsets.XML  <br/> |
   
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
|[DataRecordSets](datarecordsets-elementvisio-xml.md) <br/> |[DataRecordSets_Type](datarecordsets_type-complextypevisio-xml.md) <br/> |Содержит все элементы **записей данных** в документе.  <br/> |
   
### <a name="child-elements"></a>Дочерние элементы

|**Элемент**|**Тип**|**Описание**|
|:-----|:-----|:-----|
|[ADOData](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[ADOData_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Содержит XML, который соответствует ADO классический XML-схему для набора записей ADO и с описанием данных в записей данных.  <br/> |
|[AutoLinkComparison](autolinkcomparison-element-datarecordset_type-complextypevisio-xml.md) <br/> |[AutoLinkComparison_Type](autolinkcomparison_type-complextypevisio-xml.md) <br/> |Задает правило, которое представлено сравнение столбцов в родительском элементе **записей данных** с помощью элемента данных фигуры из последней успешной автоматического связывания действия, выполняемые в пользовательском интерфейсе.  <br/> |
|[DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Определяет, как столбец данных отображается в окне **Внешних данных** в пользовательском интерфейсе Visio и определяет данные в столбце путем определения его типа данных и форматирования.  <br/> |
|[Объектам DataColumn](datacolumns-element-datarecordset_type-complextypevisio-xml.md) <br/> |[DataColumns_Type](datacolumns_type-complextypevisio-xml.md) <br/> |Содержит все элементы **DataColumn** в записей данных.  <br/> |
|[PrimaryKey](primarykey-element-datarecordset_type-complextypevisio-xml.md) <br/> |[PrimaryKey_Type](primarykey_type-complextypevisio-xml.md) <br/> |Определяет один или несколько столбцы первичных ключей в записей данных.  <br/> |
|[RefreshConflict](refreshconflict-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RefreshConflict_Type](refreshconflict_type-complextypevisio-xml.md) <br/> |Указывает строку в записей данных, связанных с фигурой, который находится в конфликт после обновления набора записей данных.  <br/> |
|[RowMap](rowmap-element-datarecordset_type-complextypevisio-xml.md) <br/> |[RowMap_Type](rowmap_type-complextypevisio-xml.md) <br/> |Сопоставление строк набора записей данных фигуры.  <br/> |
   
### <a name="attributes"></a>Атрибуты

|**Атрибут**|**Тип**|**Обязательный**|**Описание**|**Возможные значения**|
|:-----|:-----|:-----|:-----|:-----|
|Контрольная сумма  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Значение контрольной суммой, созданных функцией Visio и на основе набора записей данных свойств. Значение в этом attirbute 0; Visio пересчитывает это значение во время выполнения.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Команда  <br/> |XSD:String  <br/> |необязательный  <br/> |Командную строку, используемую для запроса данных из источника данных.  <br/> |Значения типа xsd:string.  <br/> |
|ConnectionID содержит  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |ИД подключения для связанного объекта **подключение данных** . Не существует для источников данных XML.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|ID  <br/> |XSD:unsignedInt  <br/> |Обязательный  <br/> |Данные набора записей, уникальный идентификатор в документе.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Имя  <br/> |XSD:String  <br/> |необязательный  <br/> |Отображение (или «понятное») имя набора данных.  <br/> |Значения типа xsd:string.  <br/> |
|NextRowID  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Далее доступные Visio идентификатор строки.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|Options  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Параметры, применяемые к записей данных. Возможные значения может быть любое сочетание одного или нескольких пользователей, приведенные в следующей таблице.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RefreshInterval  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Как часто (в минутах) Visio автоматически обновляется записей данных. Это значение должно быть 1 или больше.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RefreshNoReconciliationUI  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Должны быть отключены Выверка данных пользовательского интерфейса. Имеет значение true (1) для отключения пользовательского интерфейса (UI). Значение false (0), чтобы включить пользовательский Интерфейс.  <br/> |Значения типа xsd:boolean.  <br/> |
|RefreshOverwriteAll  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |При обновлении записей данных, следует ли перезаписывать пользователем изменений в элементы данных фигуры в фигурах связанная с данными.  <br/> |Значения типа xsd:boolean.  <br/> |
|ReplaceLinks  <br/> |XSD:unsignedInt  <br/> |необязательный  <br/> |Определяет порядок обработки данных фигуры ссылки при копировании или вырезать фигур. 1, чтобы заменить существующие связи в конечную фигуру. 0, чтобы сохранить существующий ссылки в конечную фигуру.  <br/> |Значения типа xsd:unsignedInt.  <br/> |
|RowOrder  <br/> |XSD:Boolean  <br/> |необязательный  <br/> |Следует ли использовать порядок строк в записей данных как первичный ключ. Если идентификатор строки определяется порядок строк имеет значение true (1). False (0), если идентификаторы строки определяются значения в столбцы первичного ключа из набора данных.  <br/> |Значения типа xsd:boolean.  <br/> |
|TimeRefreshed  <br/> |XSD: DateTime  <br/> |необязательный  <br/> |Дата и время последнего обновления записей данных.  <br/> |Значения типа XSD: DateTime.  <br/> |
   

