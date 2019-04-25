---
title: Метод DBEngine.CompactDatabase (DAO)
TOCTitle: CompactDatabase Method
ms:assetid: 03f3a156-005a-4b71-81b0-598f326f7d42
ms:mtpsurl: https://msdn.microsoft.com/library/Ff844821(v=office.15)
ms:contentKeyID: 48542997
ms.date: 10/24/2016
mtps_version: v=office.15
f1_keywords:
- dao360.chm1052936
f1_categories:
- Office.Version=v15
localization_priority: Priority
ms.openlocfilehash: b50cb0453df1fa357fbd0b089af2e74fdd4b4c1e
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: HT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32294339"
---
# <a name="dbenginecompactdatabase-method-dao"></a>Метод DBEngine.CompactDatabase (DAO)

**Область применения**: Access 2013 | Access 2016

Копирует и сжимает закрытую базу данных, предоставляя возможность изменить ее версию, порядок сортировки и шифрование. (Только для рабочих областей Microsoft Access.)

> [!NOTE]
> Если используются зашифрованные связанные таблицы для действия, обновления и запросов SQL [например, оператор SQL UPDATE (CurrentDb.Execute "UPDATE...")], необходимо указать ключ шифрования. Кроме того, в связанных таблицах установлено ограничение в 19 знаков для ключа шифрования. См. раздел **Зашифрованные связанные таблицы** в конце этой статьи.

## <a name="syntax"></a>Синтаксис

*выражение* .CompactDatabase(***SrcName***, ***DstName***, ***DstLocale***, ***Options***, ***password***)

*выражение*: выражение, возвращающее объект **DBEngine**.

## <a name="parameters"></a>Параметры

<table>
<colgroup>
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
<col style="width: 25%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Имя</p></th>
<th><p>Обязательный/необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Определяет существующую закрытую базу данных. Это может быть полный путь и имя файла, например &quot;C:\db1.mdb&quot;. Если имя файла содержит расширение, необходимо его указать. Если в сети поддерживается эта возможность, также можно указать сетевой путь, например &quot;\\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>String</strong></p></td>
<td><p>Имя файла (и путь) сжатой базы данных, которую вы создаете. Также можно указать сетевой путь. С помощью этого аргумента нельзя указать тот же файл базы данных, что и в аргументе SrcName.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строковое выражение, указывающее порядок сортировки для создания DstName, как указанно в примечаниях.</p>
<ul>
<li><p>Если этот аргумент опущен, языковой стандарт DstName совпадает с SrcName.</p></li>
<li><p>Вы также можете создать пароль для DstName, объединив строку пароля (начиная с &quot;;pwd=&quot;) с константой в аргументе DstLocale следующим образом: dbLangSpanish &amp; &quot;;pwd=NewPassword&quot;.</p></li>
<li><p>Если вы хотите использовать такой же аргумент DstLocale, как в SrcName (значение по умолчанию), но указать новый пароль, просто введите строку пароля для DstLocale: &quot;;pwd=NewPassword&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Options</em></p></td>
<td><p>Необязательно</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Необязательно. Константа или сочетание констант, определяющих один или несколько параметров, как указано в примечаниях. Вы можете объединить параметры, сложив соответствующие константы.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строковое выражение, содержащее ключ шифрования, если база данных зашифрована. Перед фактическим паролем должна находиться строка &quot;;pwd=&quot;. Если параметр пароля добавлен в DstLocale, этот параметр игнорируется.</p><p><strong>ПРИМЕЧАНИЕ</strong>. Это устаревший параметр, который не поддерживается в формате ACCDB. Чтобы зашифровать ACCDB-файл, используйте строку параметра "pwd=". Используйте надежные пароли, содержащие строчные и прописные буквы, цифры и знаки. В ненадежных паролях не используются сочетания таких элементов. Надежный пароль: Y6dh!et5. Слабый пароль: House27. Используйте надежный пароль, который можно запомнить, чтобы не пришлось его записывать.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Можно использовать одну из следующих констант для аргумента DstLocale, чтобы задать свойство **CollatingOrder** для сравнения строк текста.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Порядок сортировки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Английский, немецкий, французский, португальский, итальянский и современный испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>Арабский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangChineseSimplified</strong></p></td>
<td><p>Китайский (упрощенное письмо)</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangChineseTraditional</strong></p></td>
<td><p>Китайский (традиционное письмо)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangCyrillic</strong></p></td>
<td><p>Русский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>Чешский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>Голландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>Греческий</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>Иврит</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>Венгерский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>Японский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>Корейский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Скандинавские языки (только ядро СУБД Microsoft Jet версии 1.0)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Норвежский и датский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>Польский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>Словенский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Традиционный испанский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Шведский и финский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>Тайский</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>Турецкий</p></td>
</tr>
</tbody>
</table>

<br/>

Можно использовать одну из следующих констант в аргументе Options, чтобы указать необходимость шифрования или расшифровки базы данных при сжатии.

> [!NOTE]
> Константы dbEncrypt и dbDecrypt являются устаревшими и не поддерживаются в форматах файлов ACCDB.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbEncrypt</strong></p></td>
<td><p>Шифрование базы данных при сжатии.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>Расшифровка базы данных при сжатии.</p></td>
</tr>
</tbody>
</table>

<br/>

Если опустить константу шифрования или указать как **dbDecrypt**, так и **dbEncrypt**, для DstName будет применяться такое же шифрование, как для SrcName.

Можно использовать одну из следующих констант в аргументе Options, чтобы указать версию формата данных сжатой базы данных. Эта константа влияет только на версию формата данных DstName и не влияет на версию объектов, определяемых в Microsoft Access, таких как формы и отчеты.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbVersion10</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 1.0.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 1.1.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 2.0.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 3.0 (совместимый с версией 3.5).</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Jet версии 4.0.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Создает базу данных, использующую при сжатии формат файлов ядра СУБД Microsoft Access версии 12.0.</p></td>
</tr>
</tbody>
</table>

<br/>

Можно указать константу только одной версии. Если опустить константу версии, версия DstName будет совпадать с SrcName. Можно сжать DstName только до версии, совпадающей с версией SrcName или более поздней.

Когда вы изменяете данные в базе данных, файл базы данных может фрагментироваться и будет занимать больше места на диске, чем требуется. Периодически для сжатия базы данных можно использовать метод **CompactDatabase**, чтобы дефрагментировать файл базы данных. Сжатая база данных обычно меньше и часто работает быстрее. Вы также можете изменить порядок сортировки, шифрование или версию формата данных при копировании и сжатии базы данных.

Необходимо закрыть файл SrcName перед его сжатием. В многопользовательской среде другие пользователи не могут держать SrcName в открытом состоянии при его сжатии. Если SrcName не закрыт или недоступен для монопольного использования, возникает ошибка.

Так как метод **CompactDatabase** создает копию базы данных, необходимо располагать достаточным местом как для исходной базы данных, так и для копии. Операция сжатия завершается сбоем, если отсутствует достаточное место на диске. Дублированную базу данных DstName не обязательно располагать на том же диске, что и SrcName. После успешного сжатия базы данных можно удалить файл SrcName и присвоить сжатому файлу DstName исходное имя файла.

Метод **CompactDatabase** копирует все данные и параметры разрешений системы безопасности из базы данных, определяемой SrcName, в базу данных, определяемую DstName.

> [!NOTE]
> Так как метод **CompactDatabase** не преобразует объекты Microsoft Access, не следует использовать **CompactDatabase** для преобразования базы данных, содержащей такие объекты.

## <a name="encrypted-linked-tables"></a>Зашифрованные связанные таблицы

Зашифрованные пароли зависят от используемого формата файла базы данных. Если вы используете Access 2003 (.mdb) или базу данных более ранней версии, у вас есть один пароль для защиты базы данных и другой пароль для шифрования базы данных. В Access 2007 (.accdb) или базах данных более поздних версий (.mdb) зашифровать и защитить базу данных можно только с помощью одного пароля, так как возможность использования двух разных паролей была удалена.

> [!NOTE]
> Для баз данных Access 2007 (.accdb) пароль является ключом шифрования

Вы можете использовать следующий пример кода VBA для кнопки:

```vb
    Private Sub Command0_Click()
    
    Dim strSourcePath As String
    Dim strDestPath As String
    
    strSourcePath = "<path>\sourceDb.accdb"
    strDestPath = "<path>\destDb.accdb"
    
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
    
    Set CurrentDatabase = CurrentDb
    Set LinkedTableDef = CurrentDatabase.CreateTableDef 
    ("My Linked Table")
    LinkedTableDef.Connect = "MS Access;pwd=Access";database=" & strDestPath
    LinkedTableDef.RefreshLink
    
    
    MsgBox "Finished"
    
    End Sub 
```

<br/>

В следующем примере кода показано, как использовать CompactDatabase с паролем (ключом шифрования) и затем сослаться на таблицу в этой сжатой базе данных. Обратите внимание, что нужно указать пароль.

```vb
    Private Sub CompactAndLink_Click() 
     
    Dim strSourcePath As String
    Dim strDestPath As String
    Dim strSourceTableName As String
    Dim strDestTableName As String
    Dim tdf As TableDef
     
    strSourcePath = "<path>\<database>.accdb"
    strDestPath = "<path>\<database>.accdb"
    strSourceTableName = "<table name in destination database>"
    strDestTableName = "<linked table name>"
     
    ' Compact source database into new destination database with encrypted password
    DBEngine.CompactDatabase strSourcePath, strDestPath, dbLangGeneral & ";pwd=Access", dbVersion120, ";pwd=Access"
     
    ' Link to one of the tables in the destination database
    ' Password must be provided in the Connect property
     
    Set CurrentDatabase = CurrentDb
    Set tdf = CurrentDatabase.CreateTableDef(strDestTableName)
       
        With tdf
            .Connect = ";pwd=Access" & ";DATABASE=" & strDestPath
            .SourceTableName = strSourceTableName
        End With
        
    CurrentDatabase.TableDefs.Append tdf
     
    MsgBox "Database compacted and encrypted password applied. Link to table also completed."
     
    End Sub
```
