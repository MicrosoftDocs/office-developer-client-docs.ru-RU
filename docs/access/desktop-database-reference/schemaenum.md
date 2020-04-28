---
title: Счемаенум (Справочник по базам данных Access на компьютере)
TOCTitle: SchemaEnum
ms:assetid: 6147b682-3c4f-ea91-fff6-ac73107d206d
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249359(v=office.15)
ms:contentKeyID: 48545208
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: aa70f275de164716b5b3975b56588e9dc4aec1a5
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32308865"
---
# <a name="schemaenum"></a>SchemaEnum

**Область применения**: Access 2013, Office 2013

Указывает тип **набора записей** схемы, извлекаемый методом [OpenSchema](openschema-method-ado.md) .

## <a name="remarks"></a>Примечания

Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO, можно найти в разделах, посвященных приложению б *справочника по программированию для программистов OLE DB*. Имя каждого раздела указано в скобках в разделе Описание следующей таблицы.

Дополнительные сведения о функции и столбцах, возвращаемых для каждой константы ADO MD, можно найти в разделах Chapter 23 документации по *OLE DB для OLAP* . Имя каждого раздела указано в круглых скобках и помечено звездочкой (\*) в столбце Описание следующей таблицы.

Переведите типы данных столбцов в документации OLE DB на типы данных ADO, обратившись к столбцу Description раздела ADO [DataTypeEnum](datatypeenum.md) . Например, тип данных OLE DB для **\_DbType встр** эквивалентен типу данных ADO **адвчар**.

ADO создает аналогичные схеме результаты для констант, **адсчемадбинфокэйвордс** и **адсчемадбинфолитералс**. ADO создает объект **Recordset**, а затем заполняет каждую строку значениями, возвращаемыми соответственно с помощью методов **идбинфо::** и **идбинфо:: жетлитералинфо** . Дополнительные сведения об этих методах можно найти в разделе Идбинфо *справки программиста OLE DB*.

<br/>

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
<th><p>Столбцы ограничений</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>адсчемаассертс</strong></p></td>
<td><p>нуль</p></td>
<td><p>Возвращает утверждения, определенные в каталоге и принадлежащие указанному пользователю. (Набор строк УТВЕРЖДЕНий)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемакаталогс</strong></p></td>
<td><p>1,1</p></td>
<td><p>Возвращает физические атрибуты, связанные с каталогами, доступными из СУБД. (Набор строк для каталога)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемачарактерсетс</strong></p></td>
<td><p>2</p></td>
<td><p>Возвращает наборы символов, определенные в каталоге и доступные определенному пользователю. (CHARACTER_SETS набор строк)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемачеккконстраинтс</strong></p></td>
<td><p>5 </p></td>
<td><p>Возвращает проверочные ограничения, определенные в каталоге и принадлежащие указанному пользователю. (CHECK_CONSTRAINTS набор строк)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемаколлатионс</strong></p></td>
<td><p>4</p></td>
<td><p>Возвращает параметры сортировки символов, определенные в каталоге и доступные определенному пользователю. (Набор строк для параметров сортировки)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемаколумнпривилежес</strong></p></td>
<td><p>13</p></td>
<td><p>Возвращает привилегии для столбцов таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им. (COLUMN_PRIVILEGES набор строк)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME<br />
ПРЕДОСТАВЛЕНИЕИЛИ<br />
ПРАВА</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемаколумнс</strong></p></td>
<td><p>4 </p></td>
<td><p>Возвращает столбцы таблиц (в том числе представлений), определенных в каталоге и доступных определенному пользователю. (Набор строк COLUMNs)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемаколумнсдомаинусаже</strong></p></td>
<td><p>11 </p></td>
<td><p>Возвращает столбцы, определенные в каталоге, зависящие от домена, определенного в каталоге и принадлежащего указанному пользователю. (COLUMN_DOMAIN_USAGE набор строк)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
DOMAIN_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемаконстраинтколумнусаже</strong></p></td>
<td><p>6 </p></td>
<td><p>Возвращает столбцы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими заданному пользователю. (CONSTRAINT_COLUMN_USAGE набор строк)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемаконстраинттаблеусаже</strong></p></td>
<td><p>7 </p></td>
<td><p>Возвращает таблицы, используемые ссылочными ограничениями, уникальными ограничениями, проверочными ограничениями и утверждениями, определенными в каталоге и принадлежащими определенному пользователю. (CONSTRAINT_TABLE_USAGE набор строк)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемакубес</strong></p></td>
<td><p>32</p></td>
<td><p>Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы). (Набор строк для КУБОВ *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемадбинфокэйвордс</strong></p></td>
<td><p>более</p></td>
<td><p>Возвращает список ключевых слов, относящихся к поставщику. (Идбинфо:: зарезервированные слова *)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемадбинфолитералс</strong></p></td>
<td><p>длиной</p></td>
<td><p>Возвращает список литералов, характерных для каждого поставщика, используемых в текстовых командах. (Идбинфо:: Жетлитералинфо *)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемадименсионс</strong></p></td>
<td><p>33</p></td>
<td><p>Возвращает сведения об измерениях в заданном кубе. Он содержит по одной строке для каждого измерения. (Набор строк измерений *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемафореигнкэйс</strong></p></td>
<td><p>27</p></td>
<td><p>Возвращает столбцы внешнего ключа, определенные в каталоге конкретным пользователем. (FOREIGN_KEYS набор строк)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемахиерарчиес</strong></p></td>
<td><p>34</p></td>
<td><p>Возвращает сведения о иерархиях, доступных в измерении. (Набор строк "ИЕРАРХИИ" *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемаиндексес</strong></p></td>
<td><p>12 </p></td>
<td><p>Возвращает индексы, определенные в каталоге и принадлежащие указанному пользователю. (Набор строк INDEXES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
Тип<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемакэйколумнусаже</strong></p></td>
<td><p>8 </p></td>
<td><p>Возвращает столбцы, определенные в каталоге и ограниченные ключами определенного пользователя. (KEY_COLUMN_USAGE набор строк)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемалевелс</strong></p></td>
<td><p>35</p></td>
<td><p>Возвращает сведения об уровнях, доступных в измерении. (Набор строк "уровни" *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемамеасурес</strong></p></td>
<td><p>36</p></td>
<td><p>Возвращает сведения о доступных показателях. (Набор "меры" *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемамемберс</strong></p></td>
<td><p>38</p></td>
<td><p>Возвращает сведения о доступных членах. (Набор строк "элементы" *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
LEVEL_NUMBER<br />
MEMBER_NAME<br />
MEMBER_UNIQUE_NAME<br />
MEMBER_CAPTION<br />
MEMBER_TYPE<br />
Оператор Tree (Дополнительные сведения см. в документации по OLE DB for OLAP.)</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемапримарикэйс</strong></p></td>
<td><p>8</p></td>
<td><p>Возвращает столбцы первичного ключа, определенные в каталоге указанным пользователем. (PRIMARY_KEYS набор строк)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемапроцедуреколумнс</strong></p></td>
<td><p>суммируемых</p></td>
<td><p>Возвращает сведения о столбцах наборов строк, возвращаемых процедурами. (PROCEDURE_COLUMNS набор строк)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемапроцедурепараметерс</strong></p></td>
<td><p>26</p></td>
<td><p>Возвращает сведения о параметрах и кодах возврата процедур. (PROCEDURE_PARAMETERS набор строк)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемапроцедурес</strong></p></td>
<td><p>16 </p></td>
<td><p>Возвращает процедуры, определенные в каталоге и принадлежащие указанному пользователю. (Набор строк процедур)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемапропертиес</strong></p></td>
<td><p>37</p></td>
<td><p>Возвращает сведения о доступных свойствах для каждого уровня измерения. (Набор строк "Свойства" *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_UNIQUE_NAME<br />
MEMBER_UNIQUE_NAME<br />
PROPERTY_TYPE<br />
PROPERTY_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемапровидерспеЦифик</strong></p></td>
<td><p>–1</p></td>
<td><p>Используется, если поставщик определяет собственные нестандартные запросы схемы.</p></td>
<td><p>&lt;Характерные для поставщика&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемапровидертипес</strong></p></td>
<td><p>22</p></td>
<td><p>Возвращает (базовые) типы данных, поддерживаемые поставщиком данных. (PROVIDER_TYPES набор строк)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемареферентиалконстраинтс</strong></p></td>
<td><p>9 </p></td>
<td><p>Возвращает ссылочные ограничения, определенные в каталоге и принадлежащие указанному пользователю. (REFERENTIAL_CONSTRAINTS набор строк)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемасчемата</strong></p></td>
<td><p>17 </p></td>
<td><p>Возвращает схемы (объекты базы данных), принадлежащие указанному пользователю. (Набор строк СЧЕМАТА)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемаскллангуажес</strong></p></td>
<td><p>18 </p></td>
<td><p>Возвращает уровни соответствия, параметры и диалекты, поддерживаемые данными обработки SQL, определенными в каталоге. (SQL_LANGUAGES набор строк)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемастатистикс</strong></p></td>
<td><p>19</p></td>
<td><p>Возвращает статистику, определенную в каталоге, принадлежащем указанному пользователю. (Набор строк статистики)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчематаблеконстраинтс</strong></p></td>
<td><p>10 </p></td>
<td><p>Возвращает ограничения таблицы, определенные в каталоге и принадлежащие указанному пользователю. (TABLE_CONSTRAINTS набор строк)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчематаблепривилежес</strong></p></td>
<td><p>14 </p></td>
<td><p>Возвращает привилегии для таблиц, определенных в каталоге и доступных определенному пользователю или предоставленных им. (TABLE_PRIVILEGES набор строк)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
ПРЕДОСТАВЛЕНИЕИЛИ<br />
ПРАВА</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчематаблес</strong></p></td>
<td><p>двадцать</p></td>
<td><p>Возвращает таблицы (в том числе представления), определенные в каталоге и доступные определенному пользователю. (Набор строк таблицы)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчематранслатионс</strong></p></td>
<td><p>21</p></td>
<td><p>Возвращает преобразования символов, определенные в каталоге и доступные указанному пользователю. (Набор строк преобразования)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчематрустис</strong></p></td>
<td><p>39</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемаусажепривилежес</strong></p></td>
<td><p>15 </p></td>
<td><p>Возвращает привилегии на использование объектов, определенных в каталоге и доступных определенному пользователю или предоставленных им. (USAGE_PRIVILEGES набор строк)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
ПРЕДОСТАВЛЕНИЕИЛИ<br />
ПРАВА</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемавиевколумнусаже</strong></p></td>
<td><p>открыт</p></td>
<td><p>Возвращает столбцы, от которых зависят просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю. (VIEW_COLUMN_USAGE набор строк)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>адсчемавиевс</strong></p></td>
<td><p>23</p></td>
<td><p>Возвращает представления, определенные в каталоге и доступные указанному пользователю. (Набор строк представления)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>адсчемавиевтаблеусаже</strong></p></td>
<td><p>25</p></td>
<td><p>Возвращает таблицы, в которых все просмотренные таблицы, определенные в каталоге и принадлежащие определенному пользователю, зависят от них. (VIEW_TABLE_USAGE набор строк)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com. MS. WFC. Data**

<table>
<colgroup>
<col style="width: 100%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p>Адоенумс. Schema. ASSERTs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. CATALOGs</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ЧАРАКТЕРСЕТС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ЧЕКККОНСТРАИНТС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. Collation</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. КОЛУМНПРИВИЛЕЖЕС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. COLUMNs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. КОЛУМНСДОМАИНУСАЖЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. КОНСТРАИНТКОЛУМНУСАЖЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. КОНСТРАИНТТАБЛЕУСАЖЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. CUBEs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ДБИНФОКЭЙВОРДС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ДБИНФОЛИТЕРАЛС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. DIMENSIONs</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ФОРЕИГНКЭЙС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ИЕРАРХИИ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. INDEXES</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. КЭЙКОЛУМНУСАЖЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. LEVELs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. MEASUREs</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. MEMBERs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ПРИМАРИКЭЙС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ПРОЦЕДУРЕКОЛУМНС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ПРОЦЕДУРЕПАРАМЕТЕРС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. процедуры</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ПРОВИДЕРСПЕЦИФИК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ПРОВИДЕРТИПЕС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. РЕФЕРЕНТИАЛКОНТРАИНТС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. СЧЕМАТА</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. СКЛЛАНГУАЖЕС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. STATISTICS</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ТАБЛЕКОНСТРАИНТС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. ТАБЛЕПРИВИЛЕЖЕС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. TABLEs</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. translation</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ДОВЕРЕНные лица</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. УСАЖЕПРИВИЛЕЖЕС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ВИЕВКОЛУМНУСАЖЕ</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Schema. VIEWs</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Schema. ВИЕВТАБЛЕУСАЖЕ</p></td>
</tr>
</tbody>
</table>

