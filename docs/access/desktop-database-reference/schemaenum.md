---
title: SchemaEnum (справочник по базам данных Access для настольных ПК)
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

Указывает тип наборов **записей** схемы, извлекаемого [методом OpenSchema.](openschema-method-ado.md)

## <a name="remarks"></a>Заметки

Дополнительные сведения о функции и столбцах, возвращаемой для каждой константы ADO, можно найти в статьях приложения Б справочника по *программистам OLE DB.* Имя каждого раздела перечислены в скобки в разделе "Описание" следующей таблицы.

Дополнительные сведения о функции и столбцах, возвращаемой для каждой константы ADO MD, можно найти в разделах главы 23 документации *OLE DB для OLAP.* Имя каждого раздела перечислены в скобки и помечены звездочкой ( ) в столбце \* "Описание" следующей таблицы.

Перевод типов данных столбцов в документации OLE DB в типы данных ADO, ссылаясь на столбец "Описание" статьи ADO [DataTypeEnum.](datatypeenum.md) Например, тип данных OLE DB **типа DBTYPE \_ WSTR** эквивалентен типу данных ADO **adWChar.**

ADO создает результаты, похожие на схему, для констант **adSchemaDBInfoKeywords** и **adSchemaDBInfoLiterals.** ADO создает набор записей, а затем заполняет каждую строку значениями, возвращенными соответственно методами **IDBInfo::GetKeywords** и **IDBInfo::GetLiteralInfo.** Дополнительные сведения об этих методах можно найти в разделе IDBInfo справочника *по OLE DB Programmer.*

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
<th><p>Столбцы ограничения</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>adSchemaAsserts</strong></p></td>
<td><p>0</p></td>
<td><p>Возвращает утверждения, определенные в каталоге, которые принадлежат определенному пользователю. (ASSERTIONS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCatalogs</strong></p></td>
<td><p>1 </p></td>
<td><p>Возвращает физические атрибуты, связанные с каталогами, доступными из DBMS. (Набор строк CATALOGS)</p></td>
<td><p>CATALOG_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCharacterSets</strong></p></td>
<td><p>2 </p></td>
<td><p>Возвращает наборы символов, определенные в каталоге, доступные определенному пользователю. (CHARACTER_SETS Rowset)</p></td>
<td><p>CHARACTER_SET_CATALOG<br />
CHARACTER_SET_SCHEMA<br />
CHARACTER_SET_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaCheckConstraints</strong></p></td>
<td><p>5 </p></td>
<td><p>Возвращает ограничения проверки, определенные в каталоге, которые принадлежат определенному пользователю. (CHECK_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCollations</strong></p></td>
<td><p>3 </p></td>
<td><p>Возвращает знаки, определенные в каталоге, доступные для определенного пользователя. (COLLATIONS Rowset)</p></td>
<td><p>COLLATION_CATALOG<br />
COLLATION_SCHEMA<br />
COLLATION_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnPrivileges</strong></p></td>
<td><p>13 </p></td>
<td><p>Возвращает привилегии для столбцов таблиц, определенных в каталоге, доступных или предоставленных определенным пользователем. (COLUMN_PRIVILEGES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME<br />
GRANTOR<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaColumns</strong></p></td>
<td><p>4 </p></td>
<td><p>Возвращает столбцы таблиц (включая представления), определенные в каталоге, доступные определенному пользователю. (Набор строк COLUMNS)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaColumnsDomainUsage</strong></p></td>
<td><p>11</p></td>
<td><p>Возвращает столбцы, определенные в каталоге, которые зависят от домена, определенного в каталоге и принадлежат определенному пользователю. (COLUMN_DOMAIN_USAGE Rowset)</p></td>
<td><p>DOMAIN_CATALOG<br />
DOMAIN_SCHEMA<br />
DOMAIN_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaConstraintColumnUsage</strong></p></td>
<td><p>6 </p></td>
<td><p>Возвращает столбцы, используемые ограничениями, уникальными ограничениями, ограничениями проверки и утверждениями, определенными в каталоге и принадлежат определенному пользователю. (CONSTRAINT_COLUMN_USAGE Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaConstraintTableUsage</strong></p></td>
<td><p>7 </p></td>
<td><p>Возвращает таблицы, используемые в ссылающихся ограничениях, уникальных ограничениях, ограничениях проверки и утверждениях, определенных в каталоге и владельцем определенного пользователя. (CONSTRAINT_TABLE_USAGE Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaCubes</strong></p></td>
<td><p>32</p></td>
<td><p>Возвращает сведения о доступных кубах в схеме (или каталоге, если поставщик не поддерживает схемы). (КУБS Rowset*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDBInfoKeywords</strong></p></td>
<td><p>30</p></td>
<td><p>Возвращает список ключевых слов для конкретного поставщика. (IDBInfo::GetKeywords *)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaDBInfoLiterals</strong></p></td>
<td><p>31</p></td>
<td><p>Возвращает список специальных литералов, используемых в текстовых командах. (IDBInfo::GetLiteralInfo *)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaDimensions</strong></p></td>
<td><p>33</p></td>
<td><p>Возвращает сведения о измерениях в заданном кубе. У него есть одна строка для каждого измерения. (DIMENSIONS Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_NAME<br />
DIMENSION_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaForeignKeys</strong></p></td>
<td><p>27</p></td>
<td><p>Возвращает столбцы внешнего ключа, определенные в каталоге определенным пользователем. (FOREIGN_KEYS Rowset)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME<br />
FK_TABLE_CATALOG<br />
FK_TABLE_SCHEMA<br />
FK_TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaHierarchies</strong></p></td>
<td><p>34</p></td>
<td><p>Возвращает сведения об иерархиях, доступных в измерении. (HIERARCHIES Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_NAME<br />
HIERARCHY_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaIndexes</strong></p></td>
<td><p>12 </p></td>
<td><p>Возвращает индексы, определенные в каталоге, которые принадлежат определенному пользователю. (НАБОР строк INDEXES)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
INDEX_NAME<br />
TYPE<br />
TABLE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaKeyColumnUsage</strong></p></td>
<td><p>8 </p></td>
<td><p>Возвращает столбцы, определенные в каталоге и ограниченные в качестве ключей определенным пользователем. (KEY_COLUMN_USAGE Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaLevels</strong></p></td>
<td><p>35</p></td>
<td><p>Возвращает сведения об уровнях, доступных в измерении. (LEVELS Rowset*)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
DIMENSION_UNIQUE_NAME<br />
HIERARCHY_UNIQUE_NAME<br />
LEVEL_NAME<br />
LEVEL_UNIQUE_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaMeasures</strong></p></td>
<td><p>36</p></td>
<td><p>Возвращает сведения о доступных мерах. (MEASURES Rowset *)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
CUBE_NAME<br />
MEASURE_NAME<br />
MEASURE_UNIQUE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaMembers</strong></p></td>
<td><p>38</p></td>
<td><p>Возвращает сведения о доступных членах. (MEMBERS Rowset *)</p></td>
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
Оператор дерева (дополнительные сведения см. в документации OLE DB для OLAP.)</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaPrimaryKeys</strong></p></td>
<td><p>28</p></td>
<td><p>Возвращает столбцы первичного ключа, определенные в каталоге определенным пользователем. (PRIMARY_KEYS Rowset)</p></td>
<td><p>PK_TABLE_CATALOG<br />
PK_TABLE_SCHEMA<br />
PK_TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedureColumns</strong></p></td>
<td><p>29</p></td>
<td><p>Возвращает сведения о столбцах строк, возвращаемой процедурами. (PROCEDURE_COLUMNS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
COLUMN_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProcedureParameters</strong></p></td>
<td><p>26</p></td>
<td><p>Возвращает сведения о параметрах и кодах возврата процедур. (PROCEDURE_PARAMETERS Rowset)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PARAMETER_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaProcedures</strong></p></td>
<td><p>16 </p></td>
<td><p>Возвращает процедуры, определенные в каталоге, которые принадлежат определенному пользователю. (НАБОР строк PROCEDURES)</p></td>
<td><p>PROCEDURE_CATALOG<br />
PROCEDURE_SCHEMA<br />
PROCEDURE_NAME<br />
PROCEDURE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProperties</strong></p></td>
<td><p>37</p></td>
<td><p>Возвращает сведения о доступных свойствах для каждого уровня измерения. (PROPERTIES Rowset *)</p></td>
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
<td><p><strong>adSchemaProviderSpecific</strong></p></td>
<td><p>–1</p></td>
<td><p>Используется, если поставщик определяет собственные нестандартные запросы схемы.</p></td>
<td><p>&lt;Конкретный поставщик&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaProviderTypes</strong></p></td>
<td><p>22</p></td>
<td><p>Возвращает (базовые) типы данных, поддерживаемые поставщиком данных. (PROVIDER_TYPES Rowset)</p></td>
<td><p>DATA_TYPE<br />
BEST_MATCH</p></td>
</tr>
<tr class="odd">
<td><p><strong>AdSchemaReferentialConstraints</strong></p></td>
<td><p>9 </p></td>
<td><p>Возвращает ограничения, определенные в каталоге, которые принадлежат определенному пользователю. (REFERENTIAL_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaSchemata</strong></p></td>
<td><p>17 </p></td>
<td><p>Возвращает схемы (объекты базы данных), которые принадлежат заданным пользователем. (Набор строк SCHEMATA)</p></td>
<td><p>CATALOG_NAME<br />
SCHEMA_NAME<br />
SCHEMA_OWNER</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaSQLLanguages</strong></p></td>
<td><p>18 </p></td>
<td><p>Возвращает уровни соответствия, параметры и диалекты, поддерживаемые SQL данных обработки, определенных в каталоге. (SQL_LANGUAGES Rowset)</p></td>
<td><p>&lt;Нет&gt;</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaStatistics</strong></p></td>
<td><p>19</p></td>
<td><p>Возвращает статистику, заданную в каталоге, которая принадлежит определенному пользователю. (НАБОР строк СТАТИСТИКИ)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTableConstraints</strong></p></td>
<td><p>10 </p></td>
<td><p>Возвращает ограничения таблицы, определенные в каталоге, которые принадлежат определенному пользователю. (TABLE_CONSTRAINTS Rowset)</p></td>
<td><p>CONSTRAINT_CATALOG<br />
CONSTRAINT_SCHEMA<br />
CONSTRAINT_NAME<br />
TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
CONSTRAINT_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTablePrivileges</strong></p></td>
<td><p>14 </p></td>
<td><p>Возвращает привилегии в таблицах, определенных в каталоге, доступных или предоставленных определенным пользователем. (TABLE_PRIVILEGES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
GRANTOR<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTables</strong></p></td>
<td><p>20</p></td>
<td><p>Возвращает таблицы (включая представления), определенные в каталоге, доступные определенному пользователю. (TABLES Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME<br />
TABLE_TYPE</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaTranslations</strong></p></td>
<td><p>21</p></td>
<td><p>Возвращает переводы символов, определенные в каталоге, доступные определенному пользователю. (НАБОР строк TRANSLATIONS)</p></td>
<td><p>TRANSLATION_CATALOG<br />
TRANSLATION_SCHEMA<br />
TRANSLATION_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaTrustees</strong></p></td>
<td><p>39</p></td>
<td><p>Зарезервировано для последующего использования.</p></td>
<td><p><br />
</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaUsagePrivileges</strong></p></td>
<td><p>15 </p></td>
<td><p>Возвращает привилегии ИСПОЛЬЗОВАНИЯ для объектов, определенных в каталоге, доступных или предоставленных определенным пользователем. (USAGE_PRIVILEGES Rowset)</p></td>
<td><p>OBJECT_CATALOG<br />
OBJECT_SCHEMA<br />
OBJECT_NAME<br />
OBJECT_TYPE<br />
GRANTOR<br />
GRANTEE</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewColumnUsage</strong></p></td>
<td><p>24</p></td>
<td><p>Возвращает столбцы, от которых зависят просматриваемые таблицы, определенные в каталоге и принадлежат определенному пользователю. (VIEW_COLUMN_USAGE Rowset)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
<tr class="even">
<td><p><strong>adSchemaViews</strong></p></td>
<td><p>23</p></td>
<td><p>Возвращает представления, определенные в каталоге, доступные определенному пользователю. (VIEWS Rowset)</p></td>
<td><p>TABLE_CATALOG<br />
TABLE_SCHEMA<br />
TABLE_NAME</p></td>
</tr>
<tr class="odd">
<td><p><strong>adSchemaViewTableUsage</strong></p></td>
<td><p>25</p></td>
<td><p>Возвращает таблицы, в которых просматриваются таблицы, определенные в каталоге и принадлежат определенному пользователю. (VIEW_TABLE_USAGE Rowset)</p></td>
<td><p>VIEW_CATALOG<br />
VIEW_SCHEMA<br />
VIEW_NAME</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Пакет: **com.ms.wfc.data**

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
<td><p>AdoEnums.Schema.ASSERTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CATALOGS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CHARACTERSETS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CHECKCONSTRAINTS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLLATIONS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.COLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.COLUMNSDOMAINUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CONSTRAINTCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.CONSTRAINTTABLEUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.CUBES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DBINFOKEYWORDS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.DBINFOLITERALS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.DIMENSIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.FOREIGNKEYS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.HIERARCHIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.INDEXES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.KEYCOLUMNUSAGE</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.LEVELS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.MEASURES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.MEMBERS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PRIMARYKEYS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURECOLUMNS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROCEDUREPARAMETERS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROCEDURES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROPERTIES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.PROVIDERSPECIFIC</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.PROVIDERTYPES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.REFERENTIALCONTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.SCHEMATA</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.SQLLANGUAGES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.STATISTICS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLECONSTRAINTS</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TABLEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TABLES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.TRANSLATIONS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.TRUSTEES</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.USAGEPRIVILEGES</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWCOLUMNUSAGE</p></td>
</tr>
<tr class="even">
<td><p>AdoEnums.Schema.VIEWS</p></td>
</tr>
<tr class="odd">
<td><p>AdoEnums.Schema.VIEWTABLEUSAGE</p></td>
</tr>
</tbody>
</table>

