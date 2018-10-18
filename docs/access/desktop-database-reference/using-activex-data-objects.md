---
<<<<<<< Название HEAD: с помощью TOCTitle объекты данных ActiveX: ms:assetid с помощью ActiveX Data Objects: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: 48545279 ms.date: 09/18/2015 === название: использование ActiveX TOCTitle объектов данных: Описание использования ActiveX Data Objects: Microsoft Access предоставляет три объектной модели для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.
MS:AssetId: 64055c45-7a27-2296-468a-015362898329 ms:mtpsurl: https://msdn.microsoft.com/library/Ff194969(v=office.15) ms:contentKeyID: 48545279 ms.date: 10/16/2018
>>>>>>> главные mtps_version: v=office.15 f1_keywords:
- vbaac10.chm5285627 f1_categories:
- Office.Version=v15
---

<<<<<<< HEAD
# <a name="using-activex-data-objects"></a>Using ActiveX Data Objects


**Применимо к**: Access 2013 | Office 2013

<a name="microsoft-access-provides-three-object-models-to-use-in-the-creation-maintaining-and-managing-of-your-access-databases-and-their-related-data-by-using-visual-basic"></a>Microsoft Access предоставляет три объектных моделей для использования в создании, поддержке и управлению баз данных Access и их данных, связанных с ними с помощью Visual Basic.
=======
# <a name="use-activex-data-objects"></a>Используйте объекты данных ActiveX

**Применимо к**: Access 2013 | Office 2013

Microsoft Access предоставляет три объектных моделей для использования в создании, обслуживания и управления баз данных Access и их данных, связанных с использованием Visual Basic.
>>>>>>> master

## <a name="microsoft-activex-data-objects-ado"></a>Microsoft ActiveX Data Objects (ADO)

ADO содержит объекты, необходимые для создания, обслуживания и удаления записей в заданном источнике данных.

<<<<<<< HEAD
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Внешний Microsoft ADO для DDL и безопасности (ADOX)

ADOX предоставляет Language(DDL) определения данных объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.

**Библиотека объектов 2.5 репликации (JRO) и Microsoft Jet**

<a name="since-ado-objects-were-designed-to-work-with-many-databases-in-addition-to-microsoft-jet-databases-functionality-specific-to-jet-was-broken-out-into-the-jro-library"></a>Поскольку объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.
=======
## <a name="microsoft-ado-ext-for-ddl-and-security-adox"></a>Внешний Microsoft ADO для DDL и безопасности (ADOX)

ADOX предоставляет язык описания данных (DDL) объекты, необходимые для создания новой базы данных и ее вложенные объекты, помимо объекты, необходимые для управления безопасностью.

### <a name="microsoft-jet-and-replication-objects-25-library-jro"></a>Библиотека Microsoft Jet и репликации объектов 2.5 (JRO)

Так как объекты ADO были предназначена для работы с использованием многих баз данных, кроме баз данных Microsoft Jet, функциональные возможности, относящиеся к Jet был разбиваются на библиотеку JRO.
>>>>>>> master

В следующей таблице перечислены функциональные возможности, предоставляемые каждым по сравнению с DAO.

<table>
<colgroup>
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
<col style="width: 20%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Функциональность</p></th>
<th><p>DAO</p></th>
<th><p>ADO1</p></th>
<th><p>ADOX2</p></th>
<th><p>JRO<br />
<<<<<<< HEAD (MDB's только)</p></th>
=== (MDB)</p></th>
>>>>>>> master
</tr>
</thead>
<tbody>
<tr class="odd">
<<<<<<< HEAD
<td><p>Создание наборов записей</p></td>
=======
<td><p>Создание наборов записей.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение параметров запуска</p></td>
=======
<td><p>Изменение параметров запуска.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p>X **</p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Поддержка ANSI92 SQL ***</p></td>
=======
<td><p>Поддержка ANSI92 SQL.* **</p></td>
>>>>>>>Образец
<td><p></p></td>
<td><p>X </p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Создание таблиц</p></td>
=======
<td><p>Создание таблиц.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Создание новой базы данных</p></td>
=======
<td><p>Создание новой базы данных.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение свойств существующей таблицы</p></td>
=======
<td><p>Изменение свойств существующей таблицы.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Создание связи между таблицами</p></td>
=======
<td><p>Создание связи между таблицами.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение параметров безопасности</p></td>
=======
<td><p>Изменение параметров безопасности.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Поддержка сжатия для столбцы данных.</p></td>
=======
<td><p>Поддержка сжатия для столбца данных.</p></td>
>>>>>>>Образец
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение сохраненных, основных SQL-запросов или представлений</p></td>
=======
<td><p>Измените хранимые, основные запросы SQL или представления.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<td><p>Создайте постоянные запросов, которые доступны только с помощью кода.</p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X *</p></td>
<td><p></p></td>
</tr>
<tr class="even">
<td><p>Создание запросов через контейнер базы данных и пользовательского интерфейса и кода.</p></td>
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Сжать/кодирование базы данных</p></td>
=======
<td><p>Сжать/шифрование базы данных.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X4</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Обновление кэша</p></td>
=======
<td><p>Обновление кэша.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X </p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Сделать реплицированной базы данных</p></td>
=======
<td><p>Сделать реплицированной базы данных.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Сделать репликами баз данных</p></td>
=======
<td><p>Сделайте репликами баз данных.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Синхронизации реплик</p></td>
=======
<td><p>Синхронизации реплик.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p>X3</p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение свойств базы данных</p></td>
=======
<td><p>Изменение свойств базы данных.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="odd">
<<<<<<< HEAD
<td><p>Создание настраиваемой базы данных свойств</p></td>
=======
<td><p>Создание настраиваемой базы данных свойств.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
<tr class="even">
<<<<<<< HEAD
<td><p>Изменение свойств столбца в таблице</p></td>
=======
<td><p>Изменение свойств столбца в таблице.</p></td>
>>>>>>>Образец
<td><p>X </p></td>
<td><p></p></td>
<td><p></p></td>
<td><p></p></td>
</tr>
</tbody>
</table>


\*Доступно только при работе с базами данных Microsoft Access. В будущих версиях поставщика SQL можно указать эту функцию в проектах Microsoft Access (файлы с расширением ADP).

\*\*Доступно только при работе с проектами Access.

<<<<<<< HEAD \* \* \* на то, что ядро СУБД Access поддерживают некоторые ANSI SQL-92 его еще не полностью ANSI92 спецификации.

Объект 1 использует **подключения** для обращения к базе данных

2 использует **каталога** объектов для базы данных ссылок

3 объект использует **реплики** для базы данных ссылок

4 объекта использует **JetEngine** для базы данных ссылок


> [!NOTE]
> <a name="punlike-dao-ado-and-adox-objects-can-perform-the-marked-actions-in-databases-other-then-jet-as-long-as-the-provider-for-those-databases-supports-that-actionp"></a><P>В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных других затем Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.</P>
=======
\*\*\*Несмотря на то, что ядро СУБД Access поддерживают некоторые ANSI SQL-92, она еще не полностью спецификации ANSI92.

1 объект использует **подключение** к базе данных ссылок.

Объект 2 использует **каталога** для базы данных ссылок.

3 объект использует **реплику** базы данных ссылок.

4 использует **JetEngine** объект базы данных ссылок.


> [!NOTE]
> В отличие от DAO ADO и ADOX объекты можно выполнить помеченные действия в базах данных, отличный от Jet до тех пор, пока поставщик для этих баз данных поддерживает это действие.
>>>>>>> master


