---
title: RecordStatusEnum (Справочник по базам данных Access на компьютере)
TOCTitle: RecordStatusEnum
ms:assetid: 302915b8-494d-0be2-6dce-eaf91a0ea8ae
ms:mtpsurl: https://msdn.microsoft.com/library/JJ249080(v=office.15)
ms:contentKeyID: 48544022
ms.date: 10/18/2018
mtps_version: v=office.15
localization_priority: Normal
ms.openlocfilehash: a83de7730224c5ecd5080c795d38cf2e9a3305a9
ms.sourcegitcommit: 8fe462c32b91c87911942c188f3445e85a54137c
ms.translationtype: MT
ms.contentlocale: ru-RU
ms.lasthandoff: 04/23/2019
ms.locfileid: "32309382"
---
# <a name="recordstatusenum"></a>RecordStatusEnum

**Область применения**: Access 2013, Office 2013

Указывает состояние записи по отношению к пакетным обновлениям и другим массовым операциям.

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
<td><p><strong>Адрекканцелед</strong></p></td>
<td><p>0x100</p></td>
<td><p>Указывает, что запись не была сохранена, так как операция была отменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адреккантрелеасе</strong></p></td>
<td><p>0x400</p></td>
<td><p>Указывает, что новая запись не была сохранена, так как существующая запись заблокирована.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекконкурренцивиолатион</strong></p></td>
<td><p>0x800</p></td>
<td><p>Указывает, что запись не была сохранена из-за использования оптимистичного параллелизма.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекдбделетед</strong></p></td>
<td><p>0x40000</p></td>
<td><p>Указывает, что запись уже была удалена из источника данных.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекделетед</strong></p></td>
<td><p>0x4</p></td>
<td><p>Указывает, что запись была удалена.</p></td>
</tr>
<tr class="even">
<td><p><strong>АдреЦинтегритивиолатион</strong></p></td>
<td><p>0x1000</p></td>
<td><p>Указывает, что запись не была сохранена, так как пользователь нарушил ограничения целостности.</p></td>
</tr>
<tr class="odd">
<td><p><strong>АдреЦинвалид</strong></p></td>
<td><p>0x10</p></td>
<td><p>Указывает, что запись не была сохранена, так как ее Закладка является недопустимой.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекмаксчанжесексцеедед</strong></p></td>
<td><p>0x2000</p></td>
<td><p>Указывает, что запись не была сохранена из-за слишком большого количества ожидающих изменений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекмодифиед</strong></p></td>
<td><p>0x2</p></td>
<td><p>Указывает, что запись была изменена.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекмултиплечанжес</strong></p></td>
<td><p>0x40</p></td>
<td><p>Указывает, что запись не была сохранена, так как она бы затронула несколько записей.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекнев</strong></p></td>
<td><p>0x1</p></td>
<td><p>Указывает, что запись является новой.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекобжектопен</strong></p></td>
<td><p>0x4000</p></td>
<td><p>Указывает, что запись не была сохранена из-за конфликта с открытым объектом хранилища.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекок</strong></p></td>
<td><p>нуль</p></td>
<td><p>Указывает, что запись успешно обновлена.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекаутофмемори</strong></p></td>
<td><p>0x8000</p></td>
<td><p>Указывает, что запись не была сохранена из-за нехватки памяти.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрекпендингчанжес</strong></p></td>
<td><p>0x80</p></td>
<td><p>Указывает, что запись не была сохранена, так как она относится к ожидающей вставке.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекпермиссиондениед</strong></p></td>
<td><p>0x10000</p></td>
<td><p>Указывает, что запись не была сохранена, так как у пользователя недостаточно разрешений.</p></td>
</tr>
<tr class="odd">
<td><p><strong>Адрексчемавиолатион</strong></p></td>
<td><p>0x20000</p></td>
<td><p>Указывает, что запись не была сохранена, так как она нарушает структуру основной базы данных.</p></td>
</tr>
<tr class="even">
<td><p><strong>Адрекунмодифиед</strong></p></td>
<td><p>0x8</p></td>
<td><p>Указывает, что запись не была изменена.</p></td>
</tr>
</tbody>
</table>


### <a name="adowfc-equivalent"></a>Эквивалент ADO/WFC

Адоенумс. Рекордстатус.

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
<td><p>Адоенумс. Рекордстатус. CANCELed</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. КАНТРЕЛЕАСЕ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. КОНКУРРЕНЦИВИОЛАТИОН</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. ДБДЕЛЕТЕД</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. DELETEd</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. ИНТЕГРИТИВИОЛАТИОН</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. INVALID</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. МАКСЧАНЖЕСЕКСЦЕЕДЕД</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. MODIFIED</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. МУЛТИПЛЕЧАНЖЕС</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. NEW</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. ОБЖЕКТОПЕН</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. ОК</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. АУТОФМЕМОРИ</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. ПЕНДИНГЧАНЖЕС</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. ПЕРМИССИОНДЕНИЕД</p></td>
</tr>
<tr class="odd">
<td><p>Адоенумс. Рекордстатус. СЧЕМАВИОЛАТИОН</p></td>
</tr>
<tr class="even">
<td><p>Адоенумс. Рекордстатус. unMODIFIED</p></td>
</tr>
</tbody>
</table>

