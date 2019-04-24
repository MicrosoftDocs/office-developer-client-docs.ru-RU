---
title: Курсороптионенум (Справочник по базам данных Access на компьютере)
TOCTitle: CursorOptionEnum
ms:assetid: 3c118c08-02f2-5290-1cef-29e97c35fddc
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249155(v=office.15)
ms:contentKeyID: 48544303
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: 7443e0cb29954fae9dfc193ffc6aa8dee9886089
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32295200"
---
# <a name="cursoroptionenum"></a>CursorOptionEnum

**Область применения**: Access 2013, Office 2013

Определяет, для каких функциональных возможностей метод [поддерживает](supports-method-ado.md) проверку.

<br/>

<table>
<colgroup>
<col style="width: 33%" />
<col style="width: 33%" />
<col style="width: 33%" />
</colgroup>
<thead>
<tr class="header">
<th><p>Константа</p></th>
<th><p>Значение</p></th>
<th><p>Описание</p></th>
</tr>
</thead>
<tbody>
<tr class="odd">
<td><p><strong>Ададднев</strong></p></td>
<td><p>0x1000400</p></td>
<td><p>Поддерживает метод <a href="addnew-method-ado.md">AddNew</a> для добавления новых записей.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адаппрокспоситион</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Поддерживает свойства <a href="absoluteposition-property-ado.md">AbsolutePosition</a> и <a href="absolutepage-property-ado.md">AbsolutePage</a> .</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адбукмарк</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Поддерживает свойство <a href="bookmark-property-ado.md">Bookmark</a> для получения доступа к определенным записям.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адделете</strong></p></td>
<td><p>0x1000800</p></td>
<td><p>Поддерживает метод <a href="delete-method-ado-recordset.md">Delete</a> для удаления записей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адфинд</strong></p></td>
<td><p>0x80000</p></td>
<td><p>Поддерживает метод <a href="find-method-ado.md">Find</a> , чтобы найти строку в наборе <a href="recordset-object-ado.md">записей</a>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адхолдрекордс</strong></p></td>
<td><p>0x100</p></td>
<td><p>Получает дополнительные записи или изменяет следующее положение без фиксации всех ожидающих изменений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адиндекс</strong></p></td>
<td><p>0x100000</p></td>
<td><p>Поддерживает свойство <a href="index-property-ado.md">index</a> для именования индекса.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адмовепревиаус</strong></p></td>
<td><p>0x200</p></td>
<td><p>Поддерживает методы <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MoveFirst</a> и <a href="movefirst-movelast-movenext-and-moveprevious-methods-ado.md">MovePrevious</a> , а также методы <a href="move-method-ado.md">Move</a> и <a href="getrows-method-ado.md">GetRows</a> для перемещения текущей позиции записи назад без использования закладок.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Аднотифи</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что базовый поставщик данных поддерживает уведомления (что определяет, поддерживаются ли события <strong>Recordset</strong> ).</p></td>
</tr>
<tr class="even">
<td><p><strong>Адресинк</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Поддерживает метод <a href="resync-method-ado.md">Resync</a> для обновления курсора с использованием данных, которые отображаются в основной базе данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адсик</strong></p></td>
<td><p>0x200000</p></td>
<td><p>Поддерживает метод <a href="seek-method-ado.md">Seek</a> , чтобы найти строку в наборе <strong>записей</strong>.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адупдате</strong></p></td>
<td><p>0x1008000</p></td>
<td><p>Поддерживает метод <a href="update-method-ado.md">Update</a> для изменения существующих данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адупдатебатч</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Поддерживает пакетное обновление (методы<a href="updatebatch-method-ado.md">UpdateBatch</a> и <a href="cancelbatch-method-ado.md">CancelBatch</a> ) для передачи групп изменений поставщику.</p></td>
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
<td><p>Адоенумс. Курсороптион. ADDNEW</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. АППРОКСПОСИТИОН</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. BOOKMARK</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. DELETE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. FIND</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. ХОЛДРЕКОРДС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. INDEX</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. MOVEPREVIOUS</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. NOTIFY</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. reSYNC</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. SEEK</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Курсороптион. UPDATE</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Курсороптион. UPDATEBATCH</p></td>
</tr>
</tbody>
</table>

