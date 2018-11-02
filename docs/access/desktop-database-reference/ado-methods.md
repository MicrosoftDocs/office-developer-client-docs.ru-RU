---
title: Методы ActiveX Data Objects (ADO)
TOCTitle: ADO methods
ms:assetid: 1fd965a0-711c-e199-822c-b9575c5034bd
ms:mtpsurl: https://msdn.microsoft.com/library/JJ248984(v=office.15)
ms:contentKeyID: 48543651
ms.date: 09/18/2015
mtps_version: v=office.15
ms.openlocfilehash: 3649a7146c0d6ab70bc5f785404f03269df1540b
ms.sourcegitcommit: 48bfe5ab15b11105f4f52937b886c92bdc26525a
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/02/2018
ms.locfileid: "25910805"
---
# <a name="ado-methods"></a>Методы ADO

**Применимо к**: Access 2013, Office 2013

<br/>

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<tbody>
<tr class="even">
<th>Метод</th>
<th>Описание</th>
</tr>
<tr class="odd">
<td><p><a href="addnew-method-ado.md">AddNew</a></p></td>
<td><p>Создает новую запись для обновляемых объекта <strong>набора записей</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="append-method-ado.md">Добавление</a></p></td>
<td><p>Добавляет объект в коллекцию. Если семейство <strong>полей</strong>, могут быть созданы новый объект <strong>поля</strong> перед добавлением в коллекцию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="appendchunk-method-ado.md">AppendChunk</a></p></td>
<td><p>Добавляет данные большого текстового или двоичных данных <strong>поля</strong>или к объекту <strong>параметра</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="begintrans-committrans-and-rollbacktrans-methods-ado.md">BeginTrans CommitTrans и RollbackTrans</a></p></td>
<td><p>Управляет транзакций обработка объект <strong>подключения</strong> следующим образом:<br/><br/><strong>BeginTrans</strong> — начало новой транзакции.<br/><br/>
<strong>CommitTrans</strong> — сохраняет все изменения и заканчивающейся текущей операции. Он также может начать новую операцию.<br/><br/>
<strong>RollbackTrans</strong> — показано, как отменить все изменения и заканчивающейся текущей операции. Он также может начать новую операцию.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancel-method-ado.md">Отмена</a></p></td>
<td><p>Отменяет выполнение ожидающих асинхронного вызова метода.</p></td>
</tr>
<tr class="even">
<td><p><a href="cancelbatch-method-ado.md">CancelBatch</a></p></td>
<td><p>Показано, как отменить ожидающие пакетного обновления.</p></td>
</tr>
<tr class="odd">
<td><p><a href="cancelupdate-method-ado.md">CancelUpdate</a></p></td>
<td><p>Отменяет все изменения, внесенные в строку текущей или новый объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> , прежде чем вызывать метод <strong>Update</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="clear-method-ado.md">Очистить</a></p></td>
<td><p>Удаляет все объекты <strong>ошибок</strong> из семейства <strong>Errors</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="clone-method-ado.md">Копия</a></p></td>
<td><p>Создает объект повторяющихся <strong>записей</strong> из существующего объекта <strong>набора записей</strong> . При необходимости указывает копию только для чтения.</p></td>
</tr>
<tr class="even">
<td><p><a href="close-method-ado.md">Закрыть</a></p></td>
<td><p>Закрывает открытый объект и любые зависящие объекты.</p></td>
</tr>
<tr class="odd">
<td><p><a href="comparebookmarks-method-ado.md">CompareBookmarks</a></p></td>
<td><p>Сравнение двух закладки и возвращает сведения об их значения.</p></td>
</tr>
<tr class="even">
<td><p><a href="copyrecord-method-ado.md">CopyRecord</a></p></td>
<td><p>Копирует файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="copyto-method-ado.md">CopyTo</a></p></td>
<td><p>Копирует указанного числа символов или байтов (в зависимости от <strong>типа</strong>) в <strong>потоке</strong> другой объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="createparameter-method-ado.md">CreateParameter</a></p></td>
<td><p>Создает новый объект <strong>параметр</strong> с указанными свойствами.</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-parameters-collection.md">Удаление (коллекции параметров ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>параметров</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="delete-method-ado-fields-collection.md">Удаление (коллекции полей ADO)</a></p></td>
<td><p>Удаляет объект из коллекции <strong>полей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="delete-method-ado-recordset.md">Удаление (записей ADO)</a></p></td>
<td><p>Удаление текущей записи или группы записей.</p></td>
</tr>
<tr class="even">
<td><p><a href="deleterecord-method-ado.md">DeleteRecord</a></p></td>
<td><p>Удаляет файл или каталог и все его подкаталоги.</p></td>
</tr>
<tr class="odd">
<td><p><a href="https://msdn.microsoft.com/library/jj248785(v=office.15)">Воспользуйтесь командой (ADO)</a></p></td>
<td><p>Выполняет запрос, инструкции SQL или хранимую процедуру, указанных в свойстве <strong>CommandText</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="https://msdn.microsoft.com/library/jj249832(v=office.15)">Выполнение (ADO-подключение)</a></p></td>
<td><p>Выполняет указанному запросу, оператор SQL, хранимую процедуру или текст от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><a href="find-method-ado.md">Найти</a></p></td>
<td><p>Выполняет поиск <strong>записей</strong> для строки, которая должна удовлетворять определенным условиям.</p></td>
</tr>
<tr class="even">
<td><p><a href="flush-method-ado.md">Очистка</a></p></td>
<td><p>Принудительно содержимое <strong>потока</strong> , оставшихся в буфер ADO для базового объекта, с которым связано <strong>потока</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="getchildren-method-ado.md">GetChildren</a></p></td>
<td><p>Возвращает <strong>набор записей</strong> , строки представляют файлы и вложенные папки в каталоге, представленный этой <strong>записи</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="getchunk-method-ado.md">Методы GetChunk</a></p></td>
<td><p>Возвращает все или части, содержимое большого текстового или объекта <strong>поля</strong> двоичных данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="getrows-method-ado.md">Получение строк</a></p></td>
<td><p>Извлекает нескольких записей объекта <strong>набора записей</strong> в массив.</p></td>
</tr>
<tr class="even">
<td><p><a href="getstring-method-ado.md">GetString</a></p></td>
<td><p>Возвращает <strong>набор записей</strong> в виде строки.</p></td>
</tr>
<tr class="odd">
<td><p><a href="loadfromfile-method-ado.md">LoadFromFile</a></p></td>
<td><p>Загружает содержимое существующего файла в <strong>поток</strong>.</p></td>
</tr>
<tr class="even">
<td><p><a href="move-method-ado.md">Перемещение</a></p></td>
<td><p>Перемещает положение текущей записи в объекте <strong>набора записей</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst, MoveLast, MoveNext и MovePrevious</a></p></td>
<td><p>Перемещает имя, Фамилия следующий или предыдущий записи в указанном объекте <strong>набора записей</strong> и делает, запишите текущей записи.</p></td>
</tr>
<tr class="even">
<td><p><a href="moverecord-method-ado.md">MoveRecord</a></p></td>
<td><p>Перемещает файл или каталог и его содержимое в другое расположение.</p></td>
</tr>
<tr class="odd">
<td><p><a href="nextrecordset-method-ado.md">NextRecordset</a></p></td>
<td><p>Удаляет текущий объект <strong>набора записей</strong> и возвращает следующего <strong>набора записей</strong> путем перемещения через последовательность команд.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-connection.md">Откройте (ADO-подключение)</a></p></td>
<td><p>Открывает подключение к источнику данных.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-record.md">Откройте (ADO запись)</a></p></td>
<td><p>Открывает существующий объект <strong>записи</strong> или создает новый файл или каталог.</p></td>
</tr>
<tr class="even">
<td><p><a href="open-method-ado-recordset.md">Откройте (записей ADO)</a></p></td>
<td><p>Открывается курсор.</p></td>
</tr>
<tr class="odd">
<td><p><a href="open-method-ado-stream.md">Открыть (поток ADO)</a></p></td>
<td><p>Открывает объект <strong>Stream</strong> для работы с потоки данных двоичный или текст.</p></td>
</tr>
<tr class="even">
<td><p><a href="openschema-method-ado.md">OpenSchema</a></p></td>
<td><p>Получает сведения о схеме базы данных от поставщика.</p></td>
</tr>
<tr class="odd">
<td><p><a href="read-method-ado.md">Read</a></p></td>
<td><p>Считывает указанное число байтов из объекта <strong>потока</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="readtext-method-ado.md">ReadText</a></p></td>
<td><p>Считывает указанное количество символов из объекта <strong>потока</strong> текста.</p></td>
</tr>
<tr class="odd">
<td><p><a href="refresh-method-ado.md">Обновление</a></p></td>
<td><p>Обновление объектов в коллекции объектов, доступных из и относящиеся к поставщику.</p></td>
</tr>
<tr class="even">
<td><p><a href="requery-method-ado.md">Обновление</a></p></td>
<td><p>Обновляет данные в объект <strong>набора записей</strong> , повторное выполнение запросов, на котором основан объект.</p></td>
</tr>
<tr class="odd">
<td><p><a href="resync-method-ado.md">Выполнить повторную синхронизацию</a></p></td>
<td><p>Обновляет данные в текущий объект <strong>набора записей</strong> или коллекции <strong>полей</strong> объекта <strong>записи</strong> из базы данных.</p></td>
</tr>
<tr class="even">
<td><p><a href="save-method-ado.md">Save</a></p></td>
<td><p>Сохранение <strong>набора записей</strong> в файл или объект <strong>Stream</strong> .</p></td>
</tr>
<tr class="odd">
<td><p><a href="savetofile-method-ado.md">SaveToFile</a></p></td>
<td><p>Сохраняет двоичные содержимое <strong>потока</strong> в файл.</p></td>
</tr>
<tr class="even">
<td><p><a href="seek-method-ado.md">Поиск</a></p></td>
<td><p>Выполняет поиск индекса <strong>набора записей</strong> для быстрого поиска строку, в которой совпадает с указанными значениями и изменяет текущее положение строки на эту строку.</p></td>
</tr>
<tr class="odd">
<td><p><a href="seteos-method-ado.md">SetEOS</a></p></td>
<td><p>Задает позицию за конец потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="skipline-method-ado.md">SkipLine</a></p></td>
<td><p>Пропускает одну всю строку при чтении текстовый поток.</p></td>
</tr>
<tr class="odd">
<td><p><a href="stat-method-ado.md">Статистика</a></p></td>
<td><p>Получает статистические сведения об open потока.</p></td>
</tr>
<tr class="even">
<td><p><a href="supports-method-ado.md">Поддерживает</a></p></td>
<td><p>Определяет, поддерживает ли указанный объект <strong>набора записей</strong> определенного типа функциональные возможности.</p></td>
</tr>
<tr class="odd">
<td><p><a href="update-method-ado.md">обновление</a>.</p></td>
<td><p>Сохраняет все изменения, внесенные в текущей строки <strong>набора записей</strong> объекта или коллекции <strong>полей</strong> объекта <strong>записи</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="updatebatch-method-ado.md">UpdateBatch</a></p></td>
<td><p>Записывает все ожидающие пакета обновления на диск.</p></td>
</tr>
<tr class="odd">
<td><p><a href="write-method-ado.md">Write</a></p></td>
<td><p>Записывает двоичные данные в объект <strong>потока</strong> .</p></td>
</tr>
<tr class="even">
<td><p><a href="writetext-method-ado.md">WriteText</a></p></td>
<td><p>Записывает строку, указанный текст в объект <strong>потока</strong> .</p></td>
</tr>
</tbody>
</table>

<br/>