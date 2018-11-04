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
ms.openlocfilehash: df7533376bf6f6d3c5387173a90c7d5e1a5013cd
ms.sourcegitcommit: 980a96cf444882d3d34cecb5faac8f8a7b7c4b57
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 11/03/2018
ms.locfileid: "25950050"
---
# <a name="dbenginecompactdatabase-method-dao"></a>Метод DBEngine.CompactDatabase (DAO)

**Применимо к**: Access 2013 | 2016 доступа

Копирует и сжимает закрытой базы данных и позволяет изменить его версию, сортировки порядок и шифрования. (Microsoft Access рабочие области только).

> [!NOTE]
> При использовании зашифрованные связанные таблицы для действия, обновления и запросы SQL [например инструкции SQL UPDATE (CurrentDb.Execute «Обновить...»)], необходимо указать ключ шифрования. Кроме того связанные таблицы настроено ограничение 19-значный ключ шифрования. В конце этого раздела в разделе **Encrypted связанные таблицы** .

## <a name="syntax"></a>Синтаксис

*выражение* . CompactDatabase (***SrcName***, ***DstName***, ***DstLocale***, ***Параметры***, ***пароль***)

*выражение* Выражение, возвращающее объект **DBEngine** .

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
<th><p>Обязательный или необязательный</p></th>
<th><p>Тип данных</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><em>SrcName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Определяет базу данных существующей, закрытой. Это может быть полный путь и имя файла, такие как &quot;C:\db1.mdb&quot;. Если расширение имени файла, необходимо указать его. Если сеть поддерживает его, можно также указать сетевой путь, таких как &quot; \\server1\share1\dir1\db1.mdb&quot;</p></td>
</tr>
<tr class="even">
<td><p><em>DstName</em></p></td>
<td><p>Обязательный</p></td>
<td><p><strong>Строка</strong></p></td>
<td><p>Имя файла (и путь) сжатии базы данных, который вы создаете. Можно также указать сетевой путь. Чтобы указать один и тот же файл базы данных в качестве SrcName нельзя использовать этот аргумент.</p></td>
</tr>
<tr class="odd">
<td><p><em>DstLocale</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строковое выражение, которое определяет порядок сортировки при создании DstName, как указано в примечания.</p>
<ul>
<li><p>Если опустить аргумент языковой стандарт DstName совпадает с SrcName.</p></li>
<li><p>Также можно создать пароль для DstName, объединив Строка пароля (начиная с &quot;; pwd =&quot;) с константой в аргументе DstLocale следующим образом: dbLangSpanish &amp; &quot;; pwd = Новый_пароль&quot;.</p></li>
<li><p>Если вы хотите использовать же DstLocale в качестве SrcName (значение по умолчанию), но указать новый пароль, просто введите строку пароль для DstLocale: &quot;; pwd = Новый_пароль&quot;</p></li>
</ul></td>
</tr>
<tr class="even">
<td><p><em>Варианты</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Необязательно указывать. Константа или сочетание констант, которое указывает один или несколько параметров, как указано в примечания. Параметры можно использовать суммируются соответствующий констант.</p></td>
</tr>
<tr class="odd">
<td><p><em>password</em></p></td>
<td><p>Необязательный</p></td>
<td><p><strong>Variant</strong></p></td>
<td><p>Строковое выражение, содержащий ключ шифрования, если база данных зашифрована. Строка &quot;; pwd =&quot; должны предшествовать текущий пароль. Этот параметр игнорируется, если включить параметр password в DstLocale.</p><p><strong>Примечание</strong>: это не рекомендуемые для использования параметра, не поддерживается в. Формат ACCDB. Для шифрования. ACCDB-файлу, используйте «pwd =» параметр string. Используйте надежные пароли, содержащие верхний и строчные буквы, числа и символы. Ненадежные пароли не смешивайте этих элементов. Надежный пароль: Y6dh! et5. Ненадежный пароль: House27. Используйте надежный пароль, который вы можете запомнить, чтобы записать его не нужно.</p>
</td>
</tr>
</tbody>
</table>


## <a name="remarks"></a>Примечания

Допустимы следующие константы для аргумента DstLocale можно использовать для указания свойство **CollatingOrder** для сравнения строк текста.

<table>
<colgroup>
<col style="width: 50%" />
<col style="width: 50%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Constant</p></th>
<th><p>Порядок сортировки</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>dbLangGeneral</strong></p></td>
<td><p>Английский, немецкий, французский, португальский, итальянский и современных испанский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangArabic</strong></p></td>
<td><p>арабский;</p></td>
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
<td><p>русский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangCzech</strong></p></td>
<td><p>чешский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangDutch</strong></p></td>
<td><p>голландский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangGreek</strong></p></td>
<td><p>греческий;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangHebrew</strong></p></td>
<td><p>иврит;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangHungarian</strong></p></td>
<td><p>венгерский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangIcelandic</strong></p></td>
<td><p>Исландский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangJapanese</strong></p></td>
<td><p>японский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangKorean</strong></p></td>
<td><p>корейский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangNordic</strong></p></td>
<td><p>Скандинавские языки (ядра Microsoft Jet базы данных версии 1.0 только)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangNorwDan</strong></p></td>
<td><p>Датский и норвежский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangPolish</strong></p></td>
<td><p>польский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSlovenian</strong></p></td>
<td><p>словенский;</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangSpanish</strong></p></td>
<td><p>Испанский (традиционный)</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangSwedFin</strong></p></td>
<td><p>Финский и шведский</p></td>
</tr>
<tr class="even">
<td><p><strong>dbLangThai</strong></p></td>
<td><p>тайский;</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbLangTurkish</strong></p></td>
<td><p>турецкий;</p></td>
</tr>
</tbody>
</table>

<br/>

Одна из следующих констант можно использовать в аргументе параметры для укажите, нужно ли для шифрования и расшифровки базы данных во время его сжатия.

> [!NOTE]
> Константы dbEncrypt и dbDecrypt устаревшие и не поддерживается в. Форматы файлов ACCDB.

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
<td><p>Зашифруйте базу данных и сжатие.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbDecrypt</strong></p></td>
<td><p>При сжатии расшифровывать базу данных.</p></td>
</tr>
</tbody>
</table>

<br/>

Если опустить константой шифрования или включить **dbDecrypt** и **dbEncrypt**, DstName будут иметь такое же шифрование как SrcName.

Одна из следующих констант можно использовать в качестве аргумента параметры указывается версия формат данных для сжатии базы данных. Это константа влияет на версию формат данных DstName и не влияет на версии объектов любого Microsoft определенные доступа, например форм и отчетов.

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
<td><p>Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 1.0 при сжатии.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion11</strong></p></td>
<td><p>Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 1.1 при сжатии.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion20</strong></p></td>
<td><p>Создает базу данных, который использует формат файла базы данных ядра Microsoft Jet версии 2.0 при сжатии.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion30</strong></p></td>
<td><p>Создает базу данных, которая использует формат файла версии 3.0 ядра базы данных Microsoft Jet (совместимый с версией 3.5) при сжатии.</p></td>
</tr>
<tr class="odd">
<td><p><strong>dbVersion40</strong></p></td>
<td><p>Создает базу данных, которая использует формат файла базы данных ядра Microsoft Jet версии 4.0 при сжатии.</p></td>
</tr>
<tr class="even">
<td><p><strong>dbVersion120</strong></p></td>
<td><p>Создает базу данных, которая использует формат файла базы данных модуля Microsoft Access версии 12.0 при сжатии.</p></td>
</tr>
</tbody>
</table>

<br/>

Можно указать только одна константа версии. Если опустить константа версии DstName будут иметь те же версии как SrcName. Можно сжать DstName только к версии, такой же или более поздней версии, чем SrcName.

При изменении данных в базе данных, файл базы данных могут стать фрагментированными и используйте больше дискового пространства не требуется. Периодически можно использовать метод **CompactDatabase** сжатие базы данных для дефрагментации файла базы данных. Сжатии базы данных обычно меньше и обычно выполняется быстрее. Можно также изменить порядок сортировки, шифрование или версии формат данных во время копировать и сжатия базы данных.

Перед его сжатии необходимо закрыть SrcName. В многопользовательской среде другие пользователи не могут иметь SrcName открыть, когда вы сжатие. Если SrcName не закрывается или недоступен в монопольном режиме, возникает ошибка.

Так как **CompactDatabase** создает копии базы данных, необходимо иметь достаточно места для исходной и повторяющихся баз данных. Compact операция заканчивается с ошибкой, если нет места на диске. База данных повторяющиеся DstName не должен находиться на том же диске SrcName. После успешного сжатия базы данных, можно удалить файл SrcName и переименуйте сжатого файла DstName в исходное имя файла.

Метод **CompactDatabase** копирует все данные и параметры разрешений безопасности из базы данных, указанный для базы данных, указанной с DstName SrcName.

> [!NOTE]
> Так как метод **CompactDatabase** не преобразования объектов Microsoft Access, не следует использовать **CompactDatabase** для преобразования база данных, содержащая такие объекты.

## <a name="encrypted-linked-tables"></a>Зашифрованные связанные таблицы

Зашифрованные пароли, зависят от формата файла базы данных, которое используется. При использовании Access 2003 (.mdb) или более ранних базы данных будут иметь один пароль для защиты базы данных и отдельные пароль для базы данных. Для Access 2007 (.accdb) и более поздней версии (.mdb) единственно возможный вариант — для шифрования и защиты базы данных с использованием одного пароля как параметр, чтобы два отдельных пароля был удален.

> [!NOTE]
> Для баз данных Access 2007 (.accdb) пароль — это ключ шифрования

Можно использовать следующий пример кода VBA для кнопки команды:

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

В следующем примере кода показано, как использовать CompactDatabase паролем (ключ шифрования) и затем ссылка на таблицу в сжатии базы данных. Обратите внимание на то, что необходимо указать пароль.

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
